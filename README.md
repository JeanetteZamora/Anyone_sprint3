# Sprint3
-Credit Risk Analysis-

## Objectives of the project

In this project, you will tackle one of the most common problems businesses use ML to solve: Credit Risk Analysis.

## Install

You can use `Docker` to easily install all the needed packages and libraries:

```bash
$ docker build -t sprint3 -f Dockerfile .
```

### Run Docker 

```bash
$ docker run --rm -it -p 8888:8888 -v $(pwd):/home/app/src sprint3 bash 
```

## Run Project

It doesn't matter if you are inside or outside a Docker container, in order to execute the project you need to launch a Jupyter notebook server running:

```bash
$ jupyter notebook --ip 0.0.0.0 --port 8888 --allow-root
```

Then, inside the file use the API Kaggle. Then go to the 'Account' tab of your user profile (https://www.kaggle.com/<username>/account) and select 'Create API Token'. You can also choose to export your Kaggle username and token to the environment:

`export KAGGLE_USERNAME=datadinosaur`
`export KAGGLE_KEY=xxxxxxxxxxxxxx`

In the page the competition copy the API command:

`kaggle competitions download -c home-credit-default-risk`

With the `zipinfo` command you can see what the zip file contains:

                Archive:  home-credit-default-risk.zip
                Zip file size: 721616255 bytes, number of entries: 10
                -rw----     5.1 fat    37383 bx defN 19-Dec-11 02:58 HomeCredit_columns_description.csv
                -rw----     5.1 fat 392703158 bx defN 19-Dec-11 02:58 POS_CASH_balance.csv
                -rw----     5.1 fat 26567651 bx defN 19-Dec-11 02:58 application_test.csv
                -rw----     5.1 fat 166133370 bx defN 19-Dec-11 02:59 application_train.csv
                -rw----     5.1 fat 170016717 bx defN 19-Dec-11 02:59 bureau.csv
                -rw----     5.1 fat 375592889 bx defN 19-Dec-11 02:59 bureau_balance.csv
                -rw----     5.1 fat 424582605 bx defN 19-Dec-11 03:00 credit_card_balance.csv
                -rw----     5.1 fat 723118349 bx defN 19-Dec-11 03:00 installments_payments.csv
                -rw----     5.1 fat 404973293 bx defN 19-Dec-11 03:02 previous_application.csv
                -rw----     5.1 fat   536202 bx defN 19-Dec-11 03:02 sample_submission.csv
                10 files, 2684261617 bytes uncompressed, 721614641 bytes compressed:  73.1%

In this project we will use two files:

        application_test.csv
        application_train.csv

With the `unzip`  commands obtains the CSV files. 


Finally, inside the file `AnyoneAI_Project3.ipynb`, you can see the project statement, description and also which parts of the code you must complete in order to solve it.

To check your results train use this command:

`kaggle competitions submit -c home-credit-default-risk -f submission.csv -m "Message"`