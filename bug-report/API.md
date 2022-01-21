# Баг-репорт при тестировании API

<table border="1" cellpadding="1" cellspacing="1" style="width:624px">
	<tbody>
		<tr>
			<td style="text-align:center; width:216px"><strong>Название поля</strong></td>
			<td style="text-align:center; width:392px"><strong>Содержание</strong></td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>ID</strong></td>
			<td style="width:392px">BUG-240944</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Заголовок</strong></td>
			<td style="width:392px"><strong>DELETE /api/v1/orders/:id</strong> возвращает 404 Not Found при удалении корзины</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Описание</strong></td>
			<td style="width:392px">Корзина не удаляется в авторизованном и неавторизованном режимах</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Шаги воспроизведения</strong></td>
			<td style="width:392px">
			<ol>
				<li>Создать корзину методом <strong>POST/api/v1/orders</strong> с телом запроса:
				<pre>
<code class="language-json">{
    "productsList": [
        {
            "id": 1,
            "quantity": 2
        },
        {
            "id": 5,
            "quantity": 2
        }
    ]
}
</code></pre>
				</li>
				<li>Удалить созданную корзину методом <strong>DELETE /api/v1/orders/:id</strong></li>
			</ol>
			</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>ОР</strong></td>
			<td style="width:392px">
			<p>200 ОК</p>
			</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>ФР</strong></td>
			<td style="width:392px">404 Not Found и сообщение: &quot;Корзина с :id не найдена&quot;</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Приоритет</strong></td>
			<td style="width:392px">Средний</td>
		</tr>
		<tr>
			<td style="text-align:center; width:216px"><strong>Окружение</strong></td>
			<td style="width:392px">Адрес сервера</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>
