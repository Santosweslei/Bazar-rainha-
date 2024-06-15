document.addEventListener('DOMContentLoaded', () => {
    const produtos = [
        { id: 1, nome: 'Produto 1', preco: 100.0, descricao: 'Descrição do Produto 1' },
        { id: 2, nome: 'Produto 2', preco: 200.0, descricao: 'Descrição do Produto 2' },
        { id: 3, nome: 'Produto 3', preco: 300.0, descricao: 'Descrição do Produto 3' },
    ];

    const produtosContainer = document.getElementById('produtos');

    produtos.forEach(produto => {
        const produtoDiv = document.createElement('div');
        produtoDiv.className = 'produto';
        produtoDiv.innerHTML = `
            <h3>${produto.nome}</h3>
            <p>${produto.descricao}</p>
            <p>Preço: R$ ${produto.preco.toFixed(2)}</p>
        `;
        produtosContainer.appendChild(produtoDiv);
    });
});
