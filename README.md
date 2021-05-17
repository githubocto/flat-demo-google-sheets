# Flat Data Demo: Google Sheets

This demo is part of a larger Flat Data project created by [GitHub OCTO](https://octo.github.com/). Read more about the project [here](https://octo.github.com/projects/flat-data).

## What this demo does

This repository uses a [Flat Data Action](https://octo.github.com/blog/flat-data) to fetch a public Google Sheet as a JSON and XML file. Specifically it chains together two flat steps, each one downloading the sheet as a different format.

Inside `.github/workflows/flat.yaml`:
```yaml
- name: Fetch data
      uses: githubocto/flat@v2
      with:
        http_url: 'https://spreadsheets.google.com/feeds/cells/1coaXmKes8b3GUFDGbmb-Hj4bek1HOEI-WCmOF4tIHwI/1/public/full' 
        downloaded_filename: google-sheet.xml
- name: Fetch data
      uses: githubocto/flat@v2
      with:
        http_url: 'https://spreadsheets.google.com/feeds/cells/1coaXmKes8b3GUFDGbmb-Hj4bek1HOEI-WCmOF4tIHwI/1/public/full?alt=json' 
        downloaded_filename: google-sheet.json
```

## License

[MIT](LICENSE)
