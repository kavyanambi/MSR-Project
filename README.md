This is a reproduction project as part of the MSR course 2022 at UniKo, CS department, SoftLang Team    


Team name: echo  



Student names:  
Kavya Sasikumar  
Poornima Muddajji Kariyanna

Objective of reproduction

Description:

Reproducting the framework(inspect4Py) for feature extraction which can be used to train machine learning models.Any GitHub repo can be run against Inspect4py will extract all the metadata and features in a JSON file.The evaluation includes a lot of annotation of each repositories info to csv manually.so we reproduced the feature extraction of the python repository with different cases

Input Data
GitHub repositories containing python files.

Output Data
The OutputDir directory will have the same subdirectory structure as the input directory given by the user. In order to ease the inspection of all the features extracted for a given directory (and its subdirectories) we have aggregated all generated json information in a single JSON file stored at OutputDir/DirectoryInfo.json.In other words, OutputDir/DirectoryInfo.json, represents all the features extracted of all files found in a given directory (and its subdirectories).

Findings of reproduction

Process delta: 

inspect4py extracts relevant code features, detects class and function metadata and identifies the main entry points for using it

Output delta:

*The are few repositories with package which have customised scripts instead of setup.py,Those are not captured .

*Some scripts are misclassified as tests therefore lot of scripts are missing when compared to given input file

*If repo has different extension other than .py ,it does’t identify ex:html,java them as different file



Implementation of reproduction

• Hardware requirements: 64bit CPU, 4 or more than
 works with both Mac or Linux OS
	
• Software requirements :
 Windows 10 or 11 with python version 3.7 or higher
Jyupter Notebook
Git repository access to get all the input python files

• Validation: The evaluation metric is not exactly calculated as mentioned in the paper since lot of manually annotation is the procedure followed in the paper. The reproducibility mainly hints as a preprocessing step which can be used for feature extraction before training machine learning models. It can also be used to automatically fill up Readme file which gives a summary of the project.

• Data : 
Input: Repository of python files, same as the paper suggested.

Output: Extracted features produced as a JSON file 
