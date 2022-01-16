# Тест-кейсы при тестировании веб-приложения

## Тест-кейсы на логику бронирования каршеринга

> **Требования**

Если пользователь корректно заполнил все поля и нажал кнопку «Забронировать», в центре экрана появится окно с заголовком «Машина забронирована». Внутри — марка, номер, иконка и адрес машины, а также стоимость поездки и таймер, который отсчитывает время бесплатного ожидания.

Если поля «Откуда» и «Куда» заполнены, отображается точная стоимость поездки. Если нет — стоимость за минуту.

По заданию тестировать таймер не нужно

> **Тест-кейсы**

<table border="1" cellpadding="1" cellspacing="1" style="width:1208px">
	<tbody>
		<tr>
			<td style="text-align:center"><strong>Номер</strong></td>
			<td style="text-align:center; width:144px"><strong>Название тест-кейса</strong></td>
			<td style="text-align:center; width:182px"><strong>Предусловие</strong></td>
			<td style="text-align:center; width:6px"><strong>Номер шага</strong></td>
			<td style="text-align:center; width:126px"><strong>Описание шага</strong></td>
			<td style="text-align:center; width:332px"><strong>Ожидаемый результат</strong></td>
			<td style="text-align:center; width:121px"><strong>Окружение</strong></td>
			<td style="text-align:center; width:73px"><strong>Статус</strong></td>
			<td style="text-align:center; width:85px"><strong>Ссылка на баг-репорт</strong></td>
		</tr>
		<tr>
			<td rowspan="3" style="text-align:center"><strong>1</strong></td>
			<td rowspan="3" style="width:144px">Проверка логики бронирования при заполнении полей &quot;Откуда&quot; и &quot;Куда&quot;</td>
			<td rowspan="3" style="width:182px">
			<p>1. Перейти на тестовый стенд</p>
			<p>2. Ввести в поле &quot;Откуда&quot; - &quot;Хамовнический вал, 18&quot;</p>
			<p>3. Ввести в поле &quot;Куда&quot; - &quot;Усачева, 3&quot;</p>
			<p>4. Выбрать режим &quot;Свой&quot;</p>
			<p>5. Выбрать вид транспорта &quot;Каршеринг&quot;</p>
			<p>6. Нажать на кнопку &quot;Забронировать&quot;</p>
			</td>
			<td style="text-align:center; width:6px">1</td>
			<td style="width:126px">Добавить права</td>
			<td rowspan="3" style="width:332px">В центре экрана появится окно с заголовком &quot;Машина забронирована&quot;. Внутри &mdash; марка, номер, иконка и адрес машины, точная стоимость поездки и таймер, который отсчитывает время бесплатного ожидания</td>
			<td rowspan="3" style="text-align:center; width:121px">Яндекс.Браузер</td>
			<td rowspan="3" style="text-align:center; width:73px">FAILED</td>
			<td rowspan="3" style="width:85px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">2</td>
			<td style="width:126px">Добавить банковскую карту</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">3</td>
			<td style="width:126px">Нажать на кнопку бронирования</td>
		</tr>
		<tr>
			<td rowspan="5" style="text-align:center"><strong>2</strong></td>
			<td rowspan="5" style="width:144px">Проверка логики бронирования, если поля &quot;Откуда&quot; и &quot;Куда&quot; не заполнены</td>
			<td rowspan="5" style="width:182px">
			<p>1. Перейти на тестовый стенд</p>
			<p>2. Ввести в поле &quot;Откуда&quot; - &quot;Хамовнический вал, 18&quot;</p>
			<p>3. Ввести в поле &quot;Куда&quot; - &quot;Усачева, 3&quot;</p>
			<p>4. Выбрать режим &quot;Свой&quot;</p>
			<p>5. Выбрать вид транспорта &quot;Каршеринг&quot;</p>
			<p>6. Нажать на кнопку &quot;Забронировать&quot;</p>
			</td>
			<td style="text-align:center; width:6px">1</td>
			<td style="width:126px">Добавить права</td>
			<td rowspan="5" style="width:332px">В центре экрана появится окно с заголовком &laquo;Машина забронирована&raquo;. Внутри &mdash; марка, номер, иконка и адрес машины, стоимость поездки за минуту и таймер, который отсчитывает время бесплатного ожидания</td>
			<td rowspan="5" style="text-align:center; width:121px">Яндекс.Браузер</td>
			<td rowspan="5" style="text-align:center; width:73px">FAILED</td>
			<td rowspan="5" style="width:85px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">2</td>
			<td style="width:126px">Добавить банковскую карту</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">3</td>
			<td style="width:126px">Очистить поле &quot;Откуда&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">4</td>
			<td style="width:126px">Очистить поле &quot;Куда&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">5</td>
			<td style="width:126px">Нажать на кнопку бронирования</td>
		</tr>
		<tr>
			<td rowspan="5" style="text-align:center"><strong>3</strong></td>
			<td rowspan="5" style="width:144px">Проверка логики бронирования при отмене поездки</td>
			<td rowspan="5" style="width:182px">
			<p>1. Перейти на тестовый стенд</p>
			<p>2. Ввести в поле &quot;Откуда&quot; - &quot;Хамовнический вал, 18&quot;</p>
			<p>3. Ввести в поле &quot;Куда&quot; - &quot;Усачева, 3&quot;</p>
			<p>4. Выбрать режим &quot;Свой&quot;</p>
			<p>5. Выбрать вид транспорта &quot;Каршеринг&quot;</p>
			<p>6. Нажать на кнопку &quot;Забронировать&quot;</p>
			</td>
			<td style="text-align:center; width:6px">1</td>
			<td style="width:126px">Добавить права</td>
			<td rowspan="5" style="width:332px">В центре экрана появится окно с подтверждением отмены поездки</td>
			<td rowspan="5" style="text-align:center; width:121px">Яндекс.Браузер</td>
			<td rowspan="5" style="text-align:center; width:73px">FAILED</td>
			<td rowspan="5" style="width:85px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">2</td>
			<td style="width:126px">Добавить банковскую карту</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">3</td>
			<td style="width:126px">Нажать на кнопку бронирования</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">4</td>
			<td style="width:126px">В появившемся окне &quot;Машина забронирована&quot; нажать на кнопку &quot;Отмена&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">5</td>
			<td style="width:126px">В появившемся окне подтвердить отмену поездки</td>
		</tr>
		<tr>
			<td rowspan="5" style="text-align:center"><strong>4</strong></td>
			<td rowspan="5" style="width:144px">Проверка логики бронирования при обновлении страницы</td>
			<td rowspan="5" style="width:182px">
			<p>1. Перейти на тестовый стенд</p>
			<p>2. Ввести в поле &quot;Откуда&quot; - &quot;Хамовнический вал, 18&quot;</p>
			<p>3. Ввести в поле &quot;Куда&quot; - &quot;Усачева, 3&quot;</p>
			<p>4. Выбрать режим &quot;Свой&quot;</p>
			<p>5. Выбрать вид транспорта &quot;Каршеринг&quot;</p>
			<p>6. Нажать на кнопку &quot;Забронировать&quot;</p>
			</td>
			<td style="text-align:center; width:6px">1</td>
			<td style="width:126px">Добавить права</td>
			<td rowspan="5" style="width:332px">В центре экрана будет отображаться окно &quot;Машина забронирована&quot; с данными до обновления</td>
			<td rowspan="5" style="text-align:center; width:121px">Яндекс.Браузер</td>
			<td rowspan="5" style="text-align:center; width:73px">FAILED</td>
			<td rowspan="5" style="width:85px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">2</td>
			<td style="width:126px">Добавить банковскую карту</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">3</td>
			<td style="width:126px">Нажать на кнопку бронирования</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">4</td>
			<td style="width:126px">Убедиться, что появилось окно &quot;Машина забронирована&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:6px">5</td>
			<td style="width:126px">Обновить страницу</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>
