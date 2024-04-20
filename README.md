# Modelling

# CHANGELOG
21/4:
Added quality NN
NOTE: 
Since physicochemical parameters are being used to predict a measurement (quality) that is NOT measured through physical means (based on ratings given by testers). This is a largely subjective measurement; we could have two wines with similar parameters, but with different qualities; since the model is being trained on this, the final result will be a split between the two results (assuming 1 result for quality = n, and another for n-1). Since quality are discrete integer values and the final prediction is rounded, then in a way the validation method of checking accuracy may be a bit ‘harsh’
- What do I mean by this? A wine may be predicted as ~6.7, which would round up to 7. However, that specific entry (row) may be a 7. Since wine quality is a subjective measurement, in practice this prediction is not so bad, but in the accuracy statement it will be shown as a FALSE.
- It may be more insightful to show the range between predictions and actual qualities (for ex, are predicitons within +-1 of the true value, and if so, then the model may not be as bad as initially thought.
- CUrrent model has ~50% accuracy, but 98% of predicted qualities are only +-1 from the actual quality

4/3:
Added ANN file
Currently not working, need to verify with Gobi

# DRIVE MOUNTING
Default path is set to
    '/content/drive/MyDrive/ColabNotebooks/Datasets/R_W_Wine_quality.csv')

You will need to mount your drive and set a path specific to where you have stored the dataset.

Instructions
1. Download dataset and save to your drive
2. Run code to initially mount drive. There will be an error related to not being able to locate the import.
3. Click on the files icon (Left menu on google colab, folder icon).
4. Navigate to drive/MyDrive
5. Locate the downloaded dataset, right click --> copy path
6. Use this path for the import
