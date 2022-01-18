# Тест-кейсы при тестировании мобильного приложения

## Тестирование нотификации

> **Требования**

1. Уведомление приходит, когда осталось 2 часа, чтобы выполнить заказ.
Заказ нужно доставить в день, который указал пользователь, до 23 : 59.
Например, заказ на 8 мая. Если в 21 : 59 8 мая курьер ещё не доставил
самокат, ему приходит пуш-уведомление.

1. Уведомление содержит такой текст: «2 часа до конца заказа. Заказ «ул
Комнатная 12-14» нужно выполнить до времени N . Если не успеваете,
предупредите поддержку: 0101»

1. Переход по нотификации ведёт в приложение на вкладку «Мои».

<table border="1" cellpadding="0" cellspacing="0" dir="ltr">
	<tbody>
		<tr>
			<td style="text-align:center"><strong>id тест-кейса</strong></td>
			<td style="text-align:center; width:158px"><strong>Название тест-кейса</strong></td>
			<td style="text-align:center; width:184px"><strong>Предусловие</strong></td>
			<td style="text-align:center"><strong>Номер шага</strong></td>
			<td style="text-align:center; width:198px"><strong>Описание шага</strong></td>
			<td style="text-align:center; width:186px"><strong>Ожидаемый результат</strong></td>
			<td style="text-align:center; width:109px"><strong>Окружение</strong></td>
			<td style="text-align:center; width:64px"><strong>Результат</strong></td>
			<td style="text-align:center; width:78px"><strong>IБаг-репорт</strong></td>
		</tr>
		<tr>
			<td colspan="1" rowspan="4">
			<p style="text-align:center"><strong>1</strong></p>
			</td>
			<td colspan="1" rowspan="4" style="width:158px">
			<p>Вёрстка пуш-уведомления</p>
			</td>
			<td colspan="1" rowspan="4" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="4" style="width:186px">
			<p>1. Фон уведомления белый<br />
			2. Сверху слева расположена иконка колеса и логотип &quot;Яндекс.Самокат&quot;<br />
			- иконка чёрно-белая, текст логотипа чёрный<br />
			3. Под логотипом текст уведомления:<br />
			&quot;2 часа до конца заказа. Заказ &quot;&lt;название улицы, номер дома, квартира&gt;&quot; нужно выполнить до 23:59. Если не успеваете, предупредите поддержку: 0101&quot;<br />
			- весь текст чёрный<br />
			- текст &quot;2 часа до конца заказа&quot; выделен жирным</p>
			</td>
			<td colspan="1" rowspan="4" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="4" style="width:64px">
			<p>FAILED</p>
			</td>
			<td colspan="1" rowspan="4" style="width:78px">ID Баг- репорта</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">В 21:59 пришло пуш-уведомление</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="4">
			<p style="text-align:center"><strong>2</strong></p>
			</td>
			<td colspan="1" rowspan="4" style="width:158px">
			<p>Проверка указанного адреса в пуш-уведомлении</p>
			</td>
			<td colspan="1" rowspan="4" style="width:184px">
			<p>1. В веб-приложении оформить заказ:<br />
			- с адресом доставки<br />
			&quot;Комсомольский проспект 18&quot;<br />
			- с датой доставки &quot;завтра&quot;<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="4" style="width:186px">
			<p>В пуш-уведомлении указан адрес: &quot;Комсомольский проспект 18&quot;</p>
			</td>
			<td colspan="1" rowspan="4" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="4" style="width:64px">
			<p>PASSED</p>
			</td>
			<td colspan="1" rowspan="4" style="width:78px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">В 21:59 пришло пуш-уведомление</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="4">
			<p style="text-align:center"><strong>3</strong></p>
			</td>
			<td colspan="1" rowspan="4" style="width:158px">
			<p>Получение пуш-уведомления при открытом приложении</p>
			</td>
			<td colspan="1" rowspan="4" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="4" style="width:186px">
			<p>Пришло пуш-уведомление</p>
			</td>
			<td colspan="1" rowspan="4" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="4" style="width:64px">
			<p>PASSED</p>
			</td>
			<td colspan="1" rowspan="4" style="width:78px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>4</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>Получение пуш-уведомления при закрытом приложении</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Пришло пуш-уведомление</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>PASSED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>5</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>Получение пуш-уведомления за 2 часа до доставки<br />
			при принятии заказа в день доставки</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Пришло пуш-уведомление</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>SKIPPED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">
			<p>Пропущена из-за бага (ID Баг- репорта)</p>
			</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>6</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>Получение пуш-уведомления за 2 часа до доставки<br />
			при принятии заказа за 1 день до доставки</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Пришло пуш-уведомление</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>SKIPPED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">Пропущена из-за бага (ID Баг- репорта)</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>7</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>Получение пуш-уведомления за 2 часа до доставки<br />
			при принятии заказа за несколько дней до доставки</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки: сегодня + 5 дней<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Пришло пуш-уведомление</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>PASSED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">&nbsp;</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне установить дату: &quot;сегодня + 5 дней&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>8</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>Негативные проверки:<br />
			получение пуш-уведомления более, чем за 2 часа до конца заказа, при принятии заказа в день доставки</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Пуш-уведомление не пришло</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>FAILED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">
			<p>ID Баг- репорта</p>
			</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на значения:<br />
			- 00:00<br />
			- 00:01<br />
			- 12:00<br />
			- 21:56<br />
			- 21:57</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>9</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>Негативные проверки:<br />
			получение пуш-уведомления более, чем за 2 часа до конца заказа, при принятии заказа за 1 день до доставки</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Пуш-уведомление не пришло</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>FAILED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">ID Баг- репорта</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">Проверить, что на телефоне установлена дата &quot;сегодня&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">На телефоне изменить время на значения:<br />
			- 00:00<br />
			- 00:01<br />
			- 12:00<br />
			- 21:56<br />
			- 21:57</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5">
			<p style="text-align:center"><strong>10</strong></p>
			</td>
			<td colspan="1" rowspan="5" style="width:158px">
			<p>При открытом приложении клик по пуш-уведомлению открывает приложение на вкладке &quot;Мои&quot;</p>
			</td>
			<td colspan="1" rowspan="5" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="5" style="width:186px">
			<p>Открылось приложение на вкладке &quot;Мои&quot;</p>
			</td>
			<td colspan="1" rowspan="5" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="5" style="width:64px">
			<p>FAILED</p>
			</td>
			<td colspan="1" rowspan="5" style="width:78px">ID Баг- репорта</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Кликнуть по полученному пуш-уведомлению</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="6">
			<p style="text-align:center"><strong>11</strong></p>
			</td>
			<td colspan="1" rowspan="6" style="width:158px">
			<p>При закрытом приложении клик по пуш-уведомлению открывает приложение на вкладке &quot;Мои&quot;</p>
			</td>
			<td colspan="1" rowspan="6" style="width:184px">
			<p>1. В веб-приложении оформить заказ с датой доставки завтра<br />
			2. Авторизоваться в мобильном приложении</p>
			</td>
			<td style="text-align:center">1</td>
			<td style="width:198px">На телефоне установить дату: &quot;завтра&quot;</td>
			<td colspan="1" rowspan="6" style="width:186px">
			<p>Открылось приложение на вкладке &quot;Мои&quot;</p>
			</td>
			<td colspan="1" rowspan="6" style="width:109px">
			<p>ОС: Android 8.0.0</p>
			</td>
			<td colspan="1" rowspan="6" style="width:64px">
			<p>FAILED</p>
			</td>
			<td colspan="1" rowspan="6" style="width:78px">ID Баг- репорта</td>
		</tr>
		<tr>
			<td style="text-align:center">2</td>
			<td style="width:198px">На телефоне изменить время на 21:58</td>
		</tr>
		<tr>
			<td style="text-align:center">3</td>
			<td style="width:198px">В мобильном приложении во вкладке &quot;Все&quot; принять созданный заказ</td>
		</tr>
		<tr>
			<td style="text-align:center">4</td>
			<td style="width:198px">Закрыть приложение</td>
		</tr>
		<tr>
			<td style="text-align:center">5</td>
			<td style="width:198px">Подождать 1 минуту</td>
		</tr>
		<tr>
			<td style="text-align:center">6</td>
			<td style="width:198px">Кликнуть по полученному пуш-уведомлению</td>
		</tr>
	</tbody>
</table>
