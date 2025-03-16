# ruff_homework_SMA


1.	После определения параметров в файле pyproject.toml и первой проверки кода с помощью ruff были определены основные ошибки в коде: "E501", "E711", "E712", "F841", "I001".
2.	После определения основных ошибок параметры ruff в файле pyproject.toml были уточнены и дополнены.
3.	После использования повторных команд ruff check, ruff check --fix --unsafe-fixes ошибки "E711", "E712", "F841", "I001" устранены. 
4.	Слишком сложная структура кода, видимая на первый взгляд, подтверждена результатом вызова команды ruff check --fix --select=C90, найдено 6 результатов функций: create_app, sglistsingle, sgreport, trtmlbcounts, countsapi2, notes, требуется рефакторинг кода.
5.	Задокументированный код был удален с помощью дополнительного инструмента eradicate командой eradicate --in-place {name.app}.
6.	Вручную были дополнительно удалены некоторые комментарии:
# to eliminate two Y's in the same section #to code when i see the situation
# @app.route('/api/filtersoldinv/<str:key>/<str:val>',methods=['get'])
# def filtersoldinv(key: str,val: str):
# @app.route('/api/slackinteractmlb',methods=['post'])
# def slackinteraction():
# "text": "*ASSIGNED TO:* \n <@%s>"%(slackid)
# },
7.	Таким образом, в коде остались 11 ошибок, связанные с превышением длины строки (в комментариях и переменной bgnotes, содержащей форматированную строку).
