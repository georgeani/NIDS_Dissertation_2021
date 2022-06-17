# Third Year Dissertation Project

This repository contains my third year dissertation. My dissertation focused in evaluating and creating a DNN for a Network Intrusion Detection System (NIDS).

The goal is the creation of a lightweight NIDS that have results comparable to those of published methods. The code can be found in [here](/Code/Dissertation_Code.ipynb).

The paper presented for my final year project can be found [here](/DNN_NIDS_FYP_2021/Dissertation%20PDF.pdf).

# Abstract

Intrusion Detection Systems (IDS) are crucial in detecting possible attacks on a network and informing the administrator about the attack and the attack type. IDS are distinguished into Host-based IDS (HIDS), that check for attacks inside a computer, and Network-based IDS (NIDS), that check for attacks in a network. Additionally, IDS can be Anomaly-based IDS, which utilizes different Machine Learning and Deep Learning techniques to learn attack patterns and Rule-based IDS which utilizes rules that are derived from historical data to detect attacks. Anomaly-based IDS can detect zero-day attacks. As such, there is the need to create a Deep Neural Network (DNN) that can learn to detect and categorize the attacks in order to be used in Anomaly-based IDS. The aim of this paper is to create a DNN that can detect and categorize the attacks that are found in the CIC-IDS-2017 dataset while being as accurate and lightweight as possible. The DNN architectures created will be evaluated from different metrics to gain a better understanding of which architecture performs the best. Pre-processing of the dataset to extract the best performance will be researched to help create an IDS that can perform better with less computational overhead. The experimental data derived by the selected architecture shows a model that performs exceptionally well for the number of attack types it has to detect compared to other published works. Yet, published work tends to perform better as different attack categorization is used. Attacks are bundled to their categories and/or more complex architectures are employed, that is not as lightweight as the proposed one.


# Guidance on how to use the code Provided

*********General Information*********

It should be noted that the code provided is an experimental prototype.

As such, it is written in a Jupyter Notebook file. That allows certain parts of
the code to run independently. This is very helpful when standalone parts of the code
need to be tested as there is no need for the whole code to run.

The datasets that were produced from the pre-processing of the data unfortunately
could not be included in the submission due to their size.

Note that this link is only accessible through University accounts.

To view the code and the results please open the HTML file in this folder, file name B915247_21COC251.html.

The code has been developed in the free environment provided by Google Colab.


*********Running the code*********

As mentioned before the code is written in a Jupyter Notebook that can only be opened
using a Jupyter Notebook server.

To open the .ipynd file and run the code. The computer needs to have Python installed and 
the Jupyter Notebook package should also be installed.

Having installed these prerequisites the Jupyter Notebook should be started using the Jupyter Notebook command.

Then using the GUI you should open the folder containing the B915247_21COC251.ipynb file and click on the file to open it.

To run the code, the following libraries need to be installed using pip:

* sklearn (Scikit-learn)
* imblearn (Imbalance-learn)
* matplotlib
* NumPy
* pandas
* seaborn
* Keras (Keras)
* TensorFlow (Tensorflow)
* fast_ml
* aif360

The installation can happen in an Anaconda environment or directly in the Python environment running on the computer.

To run most of the parts of the code the first and second piece of code needs to run to import all the dependencies that are used by the code.

In regards to the datasets available, only the datasets resulting from pre-processing are available and not the intermediary data.


*********Loading Files*********


To load the Normalizer, PowerTransformer and LabelEncoder you will need to modify the code by removing the string in the loader and replacing it 
with the file names if the files are in the same folder. Otherwise, the absolute path to the files should be used instead.

The file names with the configurations for the respective object they activate:
* normalizer.save: Used by the Normalizer, used to normalize the testing, training and validation datasets that are used for training and validation of the models.
* standardizer.save: used by the PowerTransformer, used to normalize the testing, training and validation datasets that are used for training and validation of the models.
* classes.npy: LabelEncoder values for the encoding of the classes that are found in the dataset.

The features have been saved in a file named feature_36.txt. These can be loaded in the same way as the Normalizer and other files
that have been mentioned above.

The code can be found in the B915247_21COC251.ipynb but some snippets can be seen below.

* variable_name = joblib.load('--Enter file path--'): Can be used to load the normalizer.save and standardizer.save. Make sure that the objects have been instantiated before.
Replace the object_name with the name of the variable you are using.

* encoder.classes_ = np.load('--Enter file path--', allow_pickle=True): Please ensure that you have created a LabelEncoder object before you load the encoder configurations.


To load different trained models the following code can help:

* model_name = tf.keras.models.load_model('--Enter file path--')

The model files have a .h5 extension. Make sure you change model_name with your desired variable name.

To load the datasets the following code can help:

* df_name = pd.read_csv(r"--Enter file path--", index_col="Unnamed: 0")
* df_name = reduce_memory_usage(df_name, convert_to_category=False)

Please replace the df_name with your desired variable name.

Note that depending on the dataset that you are loading you may need to change the index_col value.
If you are importing the resulting datasets keep it as index_col="Unnamed: 0". If you are importing the CSV files from the CIC-IDS-2017 raw change the setting to index_col=None.

It should be noted that strings in the parts that are loading files are the absolute paths and as such, they should be replaced with the absolute paths of the system
that are evaluated in if they are not in the same folder with the code, otherwise, they can be replaced with the name of the file with its extension.