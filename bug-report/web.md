# Баг-репорт при тестировании веб-приложения

<table border="1" cellpadding="1" cellspacing="1" style="width:624px">
	<tbody>
		<tr>
			<td style="text-align:center; width:216px"><strong>Название поля</strong></td>
			<td style="text-align:center; width:392px"><strong>Содержание</strong></td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>ID</strong></td>
			<td style="width:392px">BUG-294070</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Заголовок</strong></td>
			<td style="width:392px">Ошибка при отмене заказа в веб-приложении &quot;Яндекс.Самокат&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Предусловие</strong></td>
			<td style="width:392px">
			<ol>
				<li>Открыть веб-приложение Яндекс.Самокат</li>
				<li>Оформить заказ</li>
			</ol>
			</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Шаги воспроизведения</strong></td>
			<td style="width:392px">
			<ol>
				<li>Найти оформленный заказ</li>
				<li>Нажать &quot;Отменить&quot;</li>
				<li>Найти отменённый заказ</li>
			</ol>
			</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>ОР</strong></td>
			<td style="width:392px">
			<p>Отменённый заказ не найден</p>
			</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>ФР</strong></td>
			<td style="width:392px">
			<p>Отменённый заказ найден</p>
			</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Приоритет</strong></td>
			<td style="width:392px">Критичный</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Окружение</strong></td>
			<td style="width:392px">Яндекс.Браузер версии 21.11.0, Chrome версии 96.0.4664.93</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Дополнительные материалы</strong></td>
			<td style="width:392px">
			<p>При нажатии кнопки &quot;Отменить&quot; отправляется запрос:</p>

<code class="language-bash">curl 'https://ce54e7e9-135d-492a-a5e2-2e00fb1589b3.serverhub.praktikum-services.ru/api/v1/orders/cancel?t=586353' \
  -X 'PUT'</code></pre>
			<p>Код ошибки: 400<br />
			Ответ:<br />
			{&quot;code&quot;:400,&quot;message&quot;:&quot;Недостаточно данных для поиска&quot;}</p>
			</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>
