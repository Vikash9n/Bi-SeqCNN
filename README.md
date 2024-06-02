# Bi-SeqCNN+

This reprository is for Bi-SeqCNN+.

To run the python script, follow **the code example given in the folder Example**.


This has following main python files.


  1. Evaluate.py - This python file contains the code for the evaluation metrics used.
  2. Bi_SeqCNN_encoder.py - This contains the code for the construction of the posterior probability (output).
  3. Bi_SeqCNN_plus.py - This contains the code for the ensemble model.
  4. Segmentation.py - This python file contains the code for segmentation of the protein sequences used for training the segment encoder.


Experimental Setups:-->

Step 1:--> Creating a segmented dataset

        This will allow creating a fixed-sized segments for the protein sequence. Execute function segmentation 
        from the Segmenation.py with parameter (segmentSize, Overlapping) as (300, 250).
        
Step 2:--> Training the sequence segment encoder

        This is two steps:-
        
        (i) Creating a tokenized segments (i.e., a string of n-mers)
        
        (ii) Train the Bi-directional CNN-based architecture.
        
        For this, execute the Bi_SeqCNN_encoder.py.

This trained segmented encoder is later used with the Bi-SeqCNN+.


Implementing Bi-SeqCNN+ :-->


      This is an ensemble PFP framework based on multiple segment-size i.e., (150,300,450).

      The steps are as follows:

      (1) Train segment encoder with the different segment size i.e., (150,300,450).
      (2) Evaluate the model by executing the Bi_SeqCNN_plus.py for final evaluation.


The dataset are available at gdrive: https://bit.ly/3EMJhLx

Please cite as:

Vikash Kumar, Akshay Deepak, Ashish Ranjan, and Aravind Prakash. "Bi-SeqCNN: A Novel Light-weight Bi-directional CNN Architecture for Protein Function Prediction." IEEE/ACM Transactions on Computational Biology and Bioinformatics (Under Revision).


![Bi-SeqCNNArchitecture](https://github.com/Vikash9n/Bi-SeqCNN/assets/85949447/f75736ca-7847-4481-a212-98a2697129f2)



