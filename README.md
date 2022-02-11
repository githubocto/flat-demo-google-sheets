# Flat Data Demo: Google Sheets

This demo is part of a larger Flat Data project created by [GitHub OCTO](https://octo.github.com/). Read more about the project [here](https://octo.github.com/projects/flat-data).

## What this demo does

This repository uses a [Flat Data Action](https://github.com/githubocto/flat) to fetch a public Google Sheet as a CSV. In order to use you have Publish your Google Sheet to the web and then fetch the "CSV" link for the file. 

Inside `.github/workflows/flat.yaml`:
```yaml
- name: Fetch data
      uses: githubocto/flat@v3
      with:
        http_url: 'https://docs.google.com/spreadsheets/d/e/2PACX-1vQT7KW2U7o4zh2Sh5qpTl42OQzbKZG-glDd3rVcXhvQ1MtXTQiitvGEV6xvkfrXAn1dYADV1qLc2CEC/pub?output=csv' 
        downloaded_filename: google-sheet.csv
```

## License

[MIT](LICENSE)
