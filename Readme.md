# COMP0036 Group Assignment: BEAT THE BOOKIE
## Group N
We have been assigned to build model(s) that predict the FTR value, which can be Home Win (H), Draw (D) and Away Win (A). The general steps we will be taking to build the model(s) begins with finding a suitable dataset and performing feature engineering on the selected features to be used in the model. This entails creating functions or classes to convert the raw data and transforms it into a format where every match has that historic feature. Then, we perform feature selection to filter out unimportant features, and use the selected features in model(s), and then compare and decide the best performing model. Finally, improve models to get the best accuracy.

## Structure of the project folder
- Group Coursework Brief-20221106 - `Project Brief`
- past_notebooks(discarded) - `Past notebook files`
- pdf_notebook - `pdf version of notebooks (Contains results at different checkpoints)`
- pics - `picture resources used in the final notebook`
- savd_data - `Contains saved PCA and AutoEncoder models`
- saved_dataframes - `Contains saved final dataframe to be used in the notebook`
- saved_models - `Contains neural network models from different featuresets`
- sub_work - `Notebooks of sub tasks.`
- __`submit(TODO)`__ - Contains the files that needs to be submitted 

Tree path of whole project
```
.
├── Group Coursework Brief-20221106
│   ├── AssignmentGroup_COMP0036.pdf
│   ├── AssignmentGroup_Marking_COMP0036.pdf
│   ├── Data_Files
│   │   ├── epl-full-training.csv
│   │   ├── epl-manager-data.csv
│   │   ├── epl-manager-data-V2.csv
│   │   ├── epl-manager-data-V3.csv
│   │   ├── EPL Standings 2000-2022.csv
│   │   ├── epl-test.csv
│   │   ├── epl-training.csv
│   │   └── sample-submission.csv
│   └── LaTeX_Files
│       ├── arxiv.sty
│       └── sample.tex
├── Group_N_Final_x4.ipynb
├── manager.png
├── past_notebooks(discarded)
│   ├── Features On Past Data WITH Weighted Avg.ipynb
│   ├── Features On Past Data With Weights From Sigmoid.ipynb
│   ├── Filo.ipynb
│   ├── Generate Features Based On Past Data.ipynb
│   ├── Group_N_draft.ipynb
│   ├── Group_N_Final_FInal.ipynb
│   ├── Team Ratings & Expected Goals Model 2.ipynb
│   ├── Team Ratings & Expected Goals Model 3.ipynb
│   └── Testing Features & Basic Models.ipynb
├── pdf_notebook
│   ├── Group_N_Final_FInal(8.Dec.2022)).pdf
│   ├── Group_N_Final_x3(14.Dec.2022).pdf
│   └── Group_N_Final_x3(18.Dec.2022).pdf
├── pics
│   ├── average_of_clfs.png
│   ├── copmare_all_featuresets.png
│   └── rfe_featureset
│       ├── featureset_rfe_CV_sumary.png
│       ├── featureset_rfe_NN_classification_report.png
│       ├── featureset_rfe_NN_confusion_matrix.png
│       └── featureset_rfe_NN_CV.png
├── Readme.md
├── requirements.txt
├── results.csv
├── saved_data
│   ├── backup
│   │   ├── compare_feature_set_dict.pkl
│   │   ├── feature_set_AE16
│   │   │   ├── fingerprint.pb
│   │   │   ├── keras_metadata.pb
│   │   │   ├── saved_model.pb
│   │   │   └── variables
│   │   │       ├── variables.data-00000-of-00001
│   │   │       └── variables.index
│   │   ├── feature_set_AE30
│   │   │   ├── fingerprint.pb
│   │   │   ├── keras_metadata.pb
│   │   │   ├── saved_model.pb
│   │   │   └── variables
│   │   │       ├── variables.data-00000-of-00001
│   │   │       └── variables.index
│   │   ├── feature_set_AE4
│   │   │   ├── fingerprint.pb
│   │   │   ├── keras_metadata.pb
│   │   │   ├── saved_model.pb
│   │   │   └── variables
│   │   │       ├── variables.data-00000-of-00001
│   │   │       └── variables.index
│   │   ├── feature_set_PCA20.h5
│   │   └── feature_set_PCA30.h5
│   ├── compare_feature_set_dict.pkl
│   ├── feature_set_AE16
│   │   ├── assets
│   │   ├── fingerprint.pb
│   │   ├── keras_metadata.pb
│   │   ├── saved_model.pb
│   │   └── variables
│   │       ├── variables.data-00000-of-00001
│   │       └── variables.index
│   ├── feature_set_AE30
│   │   ├── assets
│   │   ├── fingerprint.pb
│   │   ├── keras_metadata.pb
│   │   ├── saved_model.pb
│   │   └── variables
│   │       ├── variables.data-00000-of-00001
│   │       └── variables.index
│   ├── feature_set_AE4
│   │   ├── assets
│   │   ├── fingerprint.pb
│   │   ├── keras_metadata.pb
│   │   ├── saved_model.pb
│   │   └── variables
│   │       ├── variables.data-00000-of-00001
│   │       └── variables.index
│   ├── feature_set_PCA20.h5
│   └── feature_set_PCA30.h5
├── saved_dataframes
│   ├── backup
│   │   ├── epl_for_final_eval.pkl
│   │   └── past_data_with_features.pkl
│   ├── epl_for_final_eval.pkl
│   └── past_data_with_features.pkl
├── saved_models
│   ├── backup
│   │   ├── feature_set5.h5
│   │   ├── feature_set5.pkl
│   │   ├── feature_set_AE16.h5
│   │   ├── feature_set_AE16.pkl
│   │   ├── feature_set_AE30.h5
│   │   ├── feature_set_AE30.pkl
│   │   ├── feature_set_AE4.h5
│   │   ├── feature_set_AE4.pkl
│   │   ├── feature_set_PCA20.h5
│   │   ├── feature_set_PCA20.pkl
│   │   ├── feature_set_PCA30.h5
│   │   ├── feature_set_PCA30.pkl
│   │   ├── feature_set_rfe.h5
│   │   ├── feature_set_rfe.pkl
│   │   ├── feature_set_select_model_L1.h5
│   │   ├── feature_set_select_model_L1.pkl
│   │   ├── feature_set_select_model_tree.h5
│   │   ├── feature_set_select_model_tree.pkl
│   │   ├── feature_set_sfs.h5
│   │   ├── feature_set_sfs.pkl
│   │   ├── feature_set_skb.h5
│   │   └── feature_set_skb.pkl
│   ├── feature_set5.h5
│   ├── feature_set5.pkl
│   ├── feature_set_AE16.h5
│   ├── feature_set_AE16.pkl
│   ├── feature_set_AE30.h5
│   ├── feature_set_AE30.pkl
│   ├── feature_set_AE4.h5
│   ├── feature_set_AE4.pkl
│   ├── feature_set_PCA20.h5
│   ├── feature_set_PCA20.pkl
│   ├── feature_set_PCA30.h5
│   ├── feature_set_PCA30.pkl
│   ├── feature_set_rfe.h5
│   ├── feature_set_rfe.pkl
│   ├── feature_set_select_model_L1.h5
│   ├── feature_set_select_model_L1.pkl
│   ├── feature_set_select_model_tree.h5
│   ├── feature_set_select_model_tree.pkl
│   ├── feature_set_sfs.h5
│   ├── feature_set_sfs.pkl
│   ├── feature_set_skb.h5
│   └── feature_set_skb.pkl
├── sub_work
│   ├── auto_model_selection.ipynb
│   └── Further_explore_NN.ipynb
└── to_submit
    ├── Group_N_Final_x4.ipynb
    ├── pics
    │   ├── average_of_clfs.png
    │   ├── copmare_all_featuresets.png
    │   └── rfe_featureset
    │       ├── featureset_rfe_CV_sumary.png
    │       ├── featureset_rfe_NN_classification_report.png
    │       ├── featureset_rfe_NN_confusion_matrix.png
    │       └── featureset_rfe_NN_CV.png
    ├── results.csv
    ├── saved_data
    │   ├── backup
    │   │   ├── compare_feature_set_dict.pkl
    │   │   ├── feature_set_AE16
    │   │   │   ├── fingerprint.pb
    │   │   │   ├── keras_metadata.pb
    │   │   │   ├── saved_model.pb
    │   │   │   └── variables
    │   │   │       ├── variables.data-00000-of-00001
    │   │   │       └── variables.index
    │   │   ├── feature_set_AE30
    │   │   │   ├── fingerprint.pb
    │   │   │   ├── keras_metadata.pb
    │   │   │   ├── saved_model.pb
    │   │   │   └── variables
    │   │   │       ├── variables.data-00000-of-00001
    │   │   │       └── variables.index
    │   │   ├── feature_set_AE4
    │   │   │   ├── fingerprint.pb
    │   │   │   ├── keras_metadata.pb
    │   │   │   ├── saved_model.pb
    │   │   │   └── variables
    │   │   │       ├── variables.data-00000-of-00001
    │   │   │       └── variables.index
    │   │   ├── feature_set_PCA20.h5
    │   │   └── feature_set_PCA30.h5
    │   ├── compare_feature_set_dict.pkl
    │   ├── feature_set_AE16
    │   │   ├── assets
    │   │   ├── fingerprint.pb
    │   │   ├── keras_metadata.pb
    │   │   ├── saved_model.pb
    │   │   └── variables
    │   │       ├── variables.data-00000-of-00001
    │   │       └── variables.index
    │   ├── feature_set_AE30
    │   │   ├── assets
    │   │   ├── fingerprint.pb
    │   │   ├── keras_metadata.pb
    │   │   ├── saved_model.pb
    │   │   └── variables
    │   │       ├── variables.data-00000-of-00001
    │   │       └── variables.index
    │   ├── feature_set_AE4
    │   │   ├── assets
    │   │   ├── fingerprint.pb
    │   │   ├── keras_metadata.pb
    │   │   ├── saved_model.pb
    │   │   └── variables
    │   │       ├── variables.data-00000-of-00001
    │   │       └── variables.index
    │   ├── feature_set_PCA20.h5
    │   └── feature_set_PCA30.h5
    ├── saved_dataframes
    │   ├── backup
    │   │   ├── epl_for_final_eval.pkl
    │   │   └── past_data_with_features.pkl
    │   ├── epl_for_final_eval.pkl
    │   └── past_data_with_features.pkl
    └── saved_models
        ├── backup
        │   ├── feature_set5.h5
        │   ├── feature_set5.pkl
        │   ├── feature_set_AE16.h5
        │   ├── feature_set_AE16.pkl
        │   ├── feature_set_AE30.h5
        │   ├── feature_set_AE30.pkl
        │   ├── feature_set_AE4.h5
        │   ├── feature_set_AE4.pkl
        │   ├── feature_set_PCA20.h5
        │   ├── feature_set_PCA20.pkl
        │   ├── feature_set_PCA30.h5
        │   ├── feature_set_PCA30.pkl
        │   ├── feature_set_rfe.h5
        │   ├── feature_set_rfe.pkl
        │   ├── feature_set_select_model_L1.h5
        │   ├── feature_set_select_model_L1.pkl
        │   ├── feature_set_select_model_tree.h5
        │   ├── feature_set_select_model_tree.pkl
        │   ├── feature_set_sfs.h5
        │   ├── feature_set_sfs.pkl
        │   ├── feature_set_skb.h5
        │   └── feature_set_skb.pkl
        ├── feature_set5.h5
        ├── feature_set5.pkl
        ├── feature_set_AE16.h5
        ├── feature_set_AE16.pkl
        ├── feature_set_AE30.h5
        ├── feature_set_AE30.pkl
        ├── feature_set_AE4.h5
        ├── feature_set_AE4.pkl
        ├── feature_set_PCA20.h5
        ├── feature_set_PCA20.pkl
        ├── feature_set_PCA30.h5
        ├── feature_set_PCA30.pkl
        ├── feature_set_rfe.h5
        ├── feature_set_rfe.pkl
        ├── feature_set_select_model_L1.h5
        ├── feature_set_select_model_L1.pkl
        ├── feature_set_select_model_tree.h5
        ├── feature_set_select_model_tree.pkl
        ├── feature_set_sfs.h5
        ├── feature_set_sfs.pkl
        ├── feature_set_skb.h5
        └── feature_set_skb.pkl
```