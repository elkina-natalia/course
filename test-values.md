# Классы эквивалентности и граничные значения

> **Требования**

| Название  | Тип поля  | Возможные значения  | Обязательность  |
|:----------|:----------|:----------|:----------|
| **Имя**   |текстовое поле    | Только русские буквы, пробел, тире. Длина не менее 2 и не более 15 символов    | обязательно для заполнения
| **Фамилия**    | текстовое поле    | Только русские буквы. Длина не менее 2 и не более 15 символов    | обязательно для заполнения    |
| **Адрес**    | текстовое поле    | Только русские буквы, цифры, пробел, тире, точка, запятая. Длина не менее 5 и не более 50 символов. Пробелы до и после адреса удаляются при снятии фокуса| обязательно для заполнения    |
| **Станция метро**    | текстовое поле с саджестом    | Станции метро Москвы. Список метро зашит на стороне бэкенда (в API)   | обязательно для заполнения    |
| **Телефон**    | текстовое поле    | Только цифры и знак +. Длина не менее 10 и не более 12 символов    | обязательно для заполнения    |


> **Тестовые значения**

<table border="1" cellpadding="0" cellspacing="0" dir="ltr">
	<tbody>
		<tr>
			<td style="text-align:center; width:74px"><strong>Поле</strong></td>
			<td style="text-align:center; width:205px"><strong>Название класса</strong></td>
			<td style="text-align:center; width:74px"><strong>Границы</strong></td>
			<td style="text-align:center; width:397px"><strong>Тестовые данные внутри класса (содержимое поля)</strong></td>
			<td style="text-align:center; width:258px"><strong>Тестовые данные на границах (содержимое поля)</strong></td>
			<td style="text-align:center; width:186px"><strong>Пояснение</strong></td>
		</tr>
		<tr>
			<td colspan="1" rowspan="23" style="width:74px">
			<p style="text-align:center"><strong>Имя</strong></p>
			</td>
			<td colspan="1" rowspan="4" style="width:205px">Длина поля 2 - 15 символов</td>
			<td colspan="1" rowspan="4" style="text-align:center; width:74px">2, 15</td>
			<td colspan="1" rowspan="4" style="width:397px">7 символов: Наталья</td>
			<td style="width:258px">2 символа: Ян</td>
			<td colspan="1" rowspan="4" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">3 символа: Яна</td>
		</tr>
		<tr>
			<td style="width:258px">14 символов: АллаАллаАллаАл</td>
		</tr>
		<tr>
			<td style="width:258px">15 символов: АллаАллаАллаАлл</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="2" style="width:205px">Длина поля 0 - 1 символ</td>
			<td colspan="1" rowspan="2" style="text-align:center; width:74px">0, 1</td>
			<td colspan="1" rowspan="2" style="width:397px">&nbsp;</td>
			<td style="width:258px">0 символов: пустое поле</td>
			<td colspan="1" rowspan="2" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">1 символ: А</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="2" style="width:205px">Длина поля более 15 символов</td>
			<td colspan="1" rowspan="2" style="text-align:center; width:74px">16</td>
			<td colspan="1" rowspan="2" style="width:397px">30 символов: АллаАллаАллаАллаАллаАллаАллаАл</td>
			<td style="width:258px">16 символов: АллаАллаАллаАлла</td>
			<td colspan="1" rowspan="2" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">17 символов: АллаАллаАллаАллаА</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из русских букв, тире</td>
			<td style="text-align:center; width:74px">&nbsp;</td>
			<td style="width:397px">Алла-Виктория</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из русских букв, пробела в середине</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Алла Виктория</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Только русские буквы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">Тестовое значение исключено для оптимизации, проверяется в классе &quot;2-15 символов&quot;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка с Caps Loc</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">АЛЛА</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из англ буквы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Alla</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая точку</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Алла.Виктория</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая запятую</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Алла,Виктория</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая спец символы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Алла@</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая цифры</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Алла123</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из иероглифов</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">你好你好你好</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы до имени</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">_Алла</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы после имени</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Алла_</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы до и после имени</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">_Алла_</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Поле заполнено</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td colspan="1" rowspan="2" style="width:186px">
			<p>Обязательность заполнения поля проверится в классах<br />
			&quot;2-15 символов&quot; и &quot;0-1 символ&quot;</p>
			</td>
		</tr>
		<tr>
			<td style="width:205px">Поле пустое</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="23" style="width:74px">
			<p style="text-align:center"><strong>Фамилия</strong></p>
			</td>
			<td colspan="1" rowspan="4" style="width:205px">Длина поля 2 - 15 символов</td>
			<td colspan="1" rowspan="4" style="text-align:center; width:74px">2, 15</td>
			<td colspan="1" rowspan="4" style="width:397px">7 символов: Иванова</td>
			<td style="width:258px">2 символа: Ив</td>
			<td colspan="1" rowspan="4" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">3 символа: Ива</td>
		</tr>
		<tr>
			<td style="width:258px">14 символов: ИвановаИванова</td>
		</tr>
		<tr>
			<td style="width:258px">15 символов: ИвановаИвановаИ</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="2" style="width:205px">Длина поля 0 - 1 символ</td>
			<td colspan="1" rowspan="2" style="text-align:center; width:74px">0, 1</td>
			<td colspan="1" rowspan="2" style="width:397px">&nbsp;</td>
			<td style="width:258px">0 символов: пустое поле</td>
			<td colspan="1" rowspan="2" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">1 символ: И</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="2" style="width:205px">Длина поля более 15 символов</td>
			<td colspan="1" rowspan="2" style="text-align:center; width:74px">16</td>
			<td colspan="1" rowspan="2" style="width:397px">30 символов: ИвановаИвановаИвановаИвановаИв</td>
			<td style="width:258px">16 символов: ИвановаИвановаИв</td>
			<td colspan="1" rowspan="2" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">17 символов: ИвановаИвановаИва</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из русских букв</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">Тестовое значение исключено для оптимизации, проверяется в классе &quot;2-15 символов&quot;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из англ буквы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Ivanova</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая точку</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова.</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая запятую</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова,</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая тире</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова-Иванова</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка с Caps Loc</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">ИВАНОВА</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая спец символы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова@</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая цифры</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова123</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из иероглифов</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">你好你好你好</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробел в середине</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова Иванова</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы до фамилии</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">_Иванова</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы после фамилии</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Иванова_</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы до и после фамилии</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">_Иванова_</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Поле заполнено</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td colspan="1" rowspan="2" style="width:186px">
			<p>Обязательность заполнения поля проверится в классах<br />
			&quot;2-15 символов&quot; и &quot;0-1 символ&quot;</p>
			</td>
		</tr>
		<tr>
			<td style="width:205px">Поле пустое</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="25" style="width:74px">
			<p style="text-align:center"><strong>Адрес</strong></p>
			</td>
			<td colspan="1" rowspan="4" style="width:205px">Длина поля 5 - 50 символов</td>
			<td colspan="1" rowspan="4" style="text-align:center; width:74px">5, 50</td>
			<td colspan="1" rowspan="4" style="width:397px">26 символов: &quot;Комсомольский проспект, 18&quot;</td>
			<td style="width:258px">5 символов: Комсо</td>
			<td colspan="1" rowspan="4" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">6 символов: Комсом</td>
		</tr>
		<tr>
			<td style="width:258px">49 символов: Комсомольский проспект Комсомольский проспект, 18</td>
		</tr>
		<tr>
			<td style="width:258px">50 символов: Комсомольский проспект Комсомольский проспект, 188</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="2" style="width:205px">Длина поля более 50 символов</td>
			<td colspan="1" rowspan="2" style="text-align:center; width:74px">51</td>
			<td colspan="1" rowspan="2" style="width:397px">82 символа: Комсомольский проспект, 18. Комсомольский проспект, 18. Комсомольский проспект, 18</td>
			<td style="width:258px">51 символ: Комсомольский проспект Комсомольский проспект, 188а</td>
			<td colspan="1" rowspan="2" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">52 символа: Комсомольский проспект Комсомольский проспект, 188аа</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="4" style="width:205px">Длина поля 0 - 4 символа</td>
			<td colspan="1" rowspan="4" style="text-align:center; width:74px">0, 4</td>
			<td colspan="1" rowspan="4" style="width:397px">2 символа: Ко</td>
			<td style="width:258px">0 символов: пустое поле</td>
			<td colspan="1" rowspan="4" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">1 символ: К</td>
		</tr>
		<tr>
			<td style="width:258px">3 символа: Ком</td>
		</tr>
		<tr>
			<td style="width:258px">4 символа: Комс</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из русских букв, цифр,<br />
			пробела, тире, точки, запятой</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект, 18, к. 1-2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Отсутствие русских букв</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">18, 1-2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Только русские буквы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Отсутствие пробелов</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект,18,к.1-2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Отсутствие тире</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект, 18, к. 1</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Отсутствие точки</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект, 18, к 1-2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Отсутствие запятой</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект 18 к. 1-3</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая англ буквы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">komsomolsky prospekt, 18, k. 1-2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая спец символы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект, 18, к. 1/2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из иероглифов</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">你好你好你好</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы до адреса</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">_Комсомольский проспект, 18, к. 1-2</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы после адреса</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Комсомольский проспект, 18, к. 1-2_</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы до и после адреса</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">_Комсомольский проспект, 18, к. 1-2_</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Поле заполнено</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td colspan="1" rowspan="2" style="width:186px">
			<p>Обязательность заполнения поля проверится в классах<br />
			&quot;0-4 символа&quot; и &quot;5-50 символов&quot;</p>
			</td>
		</tr>
		<tr>
			<td style="width:205px">Поле пустое</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="4" style="width:74px">
			<p style="text-align:center"><strong>Станция метро</strong></p>
			</td>
			<td style="width:205px">Станция из списка</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Профсоюзная</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Станция не из списка</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">Приморская</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Поле заполнено</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">Обязательность заполнения проверится в классе &quot;Станция из списка&quot;</td>
		</tr>
		<tr>
			<td style="width:205px">Поле пустое</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">пустое поле</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="23" style="width:74px">
			<p style="text-align:center"><strong>Телефон</strong></p>
			</td>
			<td colspan="1" rowspan="3" style="width:205px">Длина поля 10 - 12 символов</td>
			<td colspan="1" rowspan="3" style="text-align:center; width:74px">10, 12</td>
			<td colspan="1" rowspan="3" style="width:397px">&nbsp;</td>
			<td style="width:258px">10 символов: +791234567</td>
			<td colspan="1" rowspan="3" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">11 символов: +7912345678</td>
		</tr>
		<tr>
			<td style="width:258px">12 символов: +79123456789</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="4" style="width:205px">Длина поля 0 - 9 символов</td>
			<td colspan="1" rowspan="4" style="text-align:center; width:74px">0, 9</td>
			<td colspan="1" rowspan="4" style="width:397px">5 символов: +7900</td>
			<td style="width:258px">0 символов: пустое поле</td>
			<td colspan="1" rowspan="4" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">1 символ: 1</td>
		</tr>
		<tr>
			<td style="width:258px">8 символов: +7912345</td>
		</tr>
		<tr>
			<td style="width:258px">9 символов: +79123456</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="2" style="width:205px">Длина поля более 12 символов</td>
			<td colspan="1" rowspan="2" style="text-align:center; width:74px">13</td>
			<td colspan="1" rowspan="2" style="width:397px">20 символов: +7912345678912345678</td>
			<td style="width:258px">13 символов: +791234567891</td>
			<td colspan="1" rowspan="2" style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:258px">14 символов: +7912345678912</td>
		</tr>
		<tr>
			<td style="width:205px">Цифры и +</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">Тестовое значение исключено для оптимизации, проверяется в классе &quot;10-12 символов&quot;</td>
		</tr>
		<tr>
			<td style="width:205px">Только цифры</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;89001234567&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Код другой страны</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+19001234567&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая буквы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+7аааааааааа&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, содержащая спец символы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+7900123456@&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Дополнительные символы</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+7(900)123-45-67&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Строка, состоящая из нулей</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+00000000000&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Плюс в середине</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;7900+1234567&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробелы между цифрами</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+7 900 123 45 67&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробел в начале</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;_+79001234567&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробел в конце</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;+79001234567_&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Пробел в начале и в конце</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&quot;_+79001234567_&quot;</td>
			<td style="width:258px">&nbsp;</td>
			<td style="width:186px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:205px">Поле заполнено</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
			<td colspan="1" rowspan="2" style="width:186px">
			<p>Обязательность заполнения поля проверится в классах<br />
			&quot;0-9 символов&quot; и &quot;10-12 символов&quot;</p>
			</td>
		</tr>
		<tr>
			<td style="width:205px">Поле пустое</td>
			<td style="width:74px">&nbsp;</td>
			<td style="width:397px">&nbsp;</td>
			<td style="width:258px">&nbsp;</td>
		</tr>
	</tbody>
</table>
