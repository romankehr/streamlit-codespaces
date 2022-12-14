# PROBLEM

If you try to start Streamlit in a GitHub Codespace with

```streamlit run YourFile.py```

and open the provided URL, you'll be stuck at

![alt text](https://github.com/RomanKehr/streamlit-codespaces/raw/main/pleasewait.png "Please wait...")

# Workaround

Start Streamlit with

```streamlit run YourFile.py --enableCORS=false --enableXsrfProtection=false```

or add the following lines to your _.streamlit\config.toml_

```
[server]
enableCORS = false
enableXsrfProtection = false
```

After this, you can access your streamlit app in the browser from inside the codespace without a problem.

*WARNING: You might want to set these back to their default values ```true``` or remove the lines before publishing.*
