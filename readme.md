Кратко о переводчике (Translator instruction)
===


Инструкция (Instruction)
-------
In the first input field you should type the language you want to translate your text to.
In the second input field you should type your message for trabslation.
Supported languages - English, French, German, Spanish, Russian.

В первом поле (Type translation language) требуется ввести язык, на который необходимо перевести текст.
Во втором поле (Type your message) необходимо ввести текст для перевода на выбранный язык.
Поддерживаемые языки - English(Английский), French(Французский), German(немецкий), Spanish(Испанский), Russian(Русский).


Фрагменты кода (Code's fragments)
--------
**Подготовка (Setup)**
####
    message = ''
    attention = ''
    code_dict = {'English': 'en', 'Spanish': 'es', "German": 'de', 'Russian': 'ru', "French": 'fr', "Kazakhstan": 'kz'}
    translator = Translator()
Этот фрагмент задает пустые поля message и attention, дабы далее, в случае отправки пустого сообщения выдавался attention 
и наоборот, если message присутствует, то attention остается пустым. Так же тут присутствует словарь с языками, с которых можно осуществить
перевод. В самом конце переменной присваивается объект класса Translator, чтобы в дальнейшем
работать с ним.

This fragment sets empty fields message and attention, so that further, in case of sending an empty message, attention is issued
conversely, if message is present, attention is left blank. There is also a dictionary with languages ​​from which you can implement
translation. At the very end of the variable, an object of the Translator class is assigned, so that in the future
work with him.



**Реализация (Punchline)**
####
    to_lang = code_dict[lang]
    translation = translator.translate(text, dest=to_lang)
    translated = translation.text
    message = translated
Данный фрагмент кода определяет язык, на который хотим перевести, далее делает сам перевод во второй строчке.
В третьей строчке мы получаем текст перевода, а в последней просто создаем ненужную переменную message, чтобы
передать в Jinj'у

This piece of code determines the language into which we want to translate, then makes the translation itself in the second line.
In the third line we get the translation text, and in the last one we simply create an unnecessary message variable so that
transfer to Jinj

