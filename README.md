# Heroku Buildpack Tesseract

This package provide a custom Heroku buildpack providing the [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) binary and all the required libraries to Heroku apps. Training data language(s) are configurable (default English). 

## Configuration

The first step consists in allowing your Heroku app to use multiple buildpacks. Heroku natively supports [multiple buildpacks per app](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

1. setup your app as  
    ```
    heroku buildpacks:set heroku/LANG
    heroku buildpacks:add https://github.com/oswellchan/heroku-buildpack-tesseract
    ```
	
    where `LANG` is the language used by your app (e.g., `ruby`, `python`, or `nodejs`). A complete list of Heroku buildpacks can be found [here](https://devcenter.heroku.com/articles/buildpacks).
2. OPTIONAL: set heroku config var "TESSERACT_OCR_LANGUAGES" to one or more languages, e.g. "eng,deu". [Supported languages](https://github.com/tesseract-ocr/tessdata)
3. you can use the `tesseract` binary in your Heroku app!
4. deploy :)

## Note
This fork adds configurable multi-language support

## License
MIT License.

Original work Copyright (c) 2013 Marco Azimonti  
Modified work Copyright (c) 2015 Matteo Maggioni  
Modified work Copyright (c) 2017 Oswell Chan
Modified work Copyright (c) 2017 Marcel Scheid
