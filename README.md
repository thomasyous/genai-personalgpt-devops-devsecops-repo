### Project Modified by ASG and Raghu The Security Expert

This project is inspired by [privateGPT](https://github.com/imartinez/privateGPT) and [ollama](https://github.com/jmorganca/ollama).

#### Step 1: Set Up a Virtual Environment
Create a virtual environment named `personalGPT` using conda. This will help isolate the project dependencies and keep your main Python environment clean.
```sh
conda create -n personalGPT


#### Step 2: Install the Required Packages
Install all the necessary packages specified in the requirements.txt file. This ensures that your project has all the dependencies it needs to run properly.

```
pip install -r requirements.txt
```

#### Step 3:  Pull the Models
If you do not already have models loaded in Ollama, pull the required models. Make sure Ollama is running on your system, which can be downloaded from Ollama.
#### Make sure to have Ollama running on your system from https://ollama.ai
```
ollama pull mistral
```

#### Step 4: Prepare Your Input Documents
Create a directory named input_documents and place all your files in this folder. This is where your documents will be stored and processed.


#### Step 5: Ingest the files 
Run the ingestion script to process the files you have placed in the input_documents directory. Use python3 if you are on macOS.

```
python ingest.py
```


#### Step 6: Run the Application
Execute the main script to start the application. Use python3 if you are on macOS. This will allow you to interact with your documents.
```
python myPersonalGPT.py
```

##### Now, you can enter queries and interact with your documents. For example:
```
Enter a query: Explain the code in the *.java file?
```

### Trying a Different Model
To experiment with a different model, pull the desired model and run the application with the new model specified.
```
ollama pull llama2:13b
MODEL=llama2:13b python myPersonalGPT.py
```

## Adding more files
To add more files, simply place them in the input_documents directory. The supported file extensions include:

Put any and all your files into the `input_documents` directory

The supported extensions are:

- `.csv`: CSV,
- `.docx`: Word Document,
- `.doc`: Word Document,
- `.enex`: EverNote,
- `.eml`: Email,
- `.epub`: EPub,
- `.html`: HTML File,
- `.md`: Markdown,
- `.msg`: Outlook Message,
- `.odt`: Open Document Text,
- `.pdf`: Portable Document Format (PDF),
- `.pptx` : PowerPoint Document,
- `.ppt` : PowerPoint Document,
- `.txt`: Text file (UTF-8),
