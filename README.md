# cs-269-SLG
Com Sci 269 Subject Line Generation Project

# Files:

Note: all of our notebooks are originlated in running in Google Collab, we made modifications to them for local run. If you found problems, feel free to use the codes here: https://drive.google.com/drive/folders/1j4LOAUlgVcJa8QpYkr3FTm9HgepoFNSN?usp=sharing

`BART_training.ipynb`: the notebook that train the BART model using training data

`t5_training.ipynb`: the notebook that train the T5 model using training data

`load_T5_model_and_generate_pred.ipynb`: the notebook to load the model generated by `t5_training` and generate subject lines on test set.(final generation is a csv file)

`load_BART_model_and_generate_pred.ipynb`: the notebook to load the model generated by `BART_training` and generate subject lines on test set.(final generation is a csv file)

`testing_csv_uploaded.ipynb` : the notebook to run ROUGE and METEOR on the result of `load_T5_model_and_generate_pred.ipynb` OR `load_BART_model_and_generate_pred.ipynb`

`train.csv`: the training set, parsed from the training data used by Zhang et al( https://github.com/ryanzhumich/AESLC)

`new_test.csv`: the test set, parsed from the testing data used by Zhang et al (https://github.com/ryanzhumich/AESLC) and removed all the human annotations inside. Only keep the original email subject lines.

`Lead_2_geneartion.ipynb`: The code for generating lead_2 benchmark result csv

 `lead_2.csv`: The generated lead_2 csv file. As an example to be feeded into `testing_csv_uploaded.ipynb` to get ROUGE and METEOR score.

# Whole process:
Run one of the training notebooks and generate a model--> Load the model into correspoding notebooks start with "load"--> Test the csv file generated using`testing_csv_uploaded.ipynb` remember to change the file name for models (for those notebooks start with "load") or genearted csv (for `testing_csv_uploaded.ipynb`)


# Two example trained models
You can download two of our models trained by `BART_training.ipynb` and `t5_training.ipynb` to generate predictions using `load_T5_model_and_generate_pred.ipynb` or `load_BART_model_and_generate_pred.ipynb`

`BART_epoch5.pth`: The BART model tuned with epoch=5. Link: https://drive.google.com/file/d/1ZdOtS9i-6jVL0GRmjvcUtYBIzuk3-oEJ/view?usp=sharing

`t5_epoch5.pth`: The T5 model tuned with epoch=5. Link: https://drive.google.com/file/d/1mEFoUPGyS8678fhjvNhNCb2KYWs1v3KW/view?usp=sharing


# Reference
Rui Zhang and Joel Tetreault. 2019.  This email could save your life: Introducing the task of email subject line generation.
