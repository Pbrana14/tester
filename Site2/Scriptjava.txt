<script>
	const form = document.querySelector('form');
	const tabela = document.querySelector('table tbody');

	form.addEventListener('submit', (e) => {
		e.preventDefault();

		const produtoInput = document.querySelector('#produto');
		const produto = produtoInput.value.trim();

		if (produto.length === 0) return;

		const row = document.createElement('tr');
		const tdProduto = document.createElement('td');
		const tdSelecionado = document.createElement('td');
		const checkbox = document.createElement('input');
		checkbox.type =
