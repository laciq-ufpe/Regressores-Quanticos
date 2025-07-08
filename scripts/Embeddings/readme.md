
# Projeto de Regressores Quânticos

Este repositório contém experimentos com diferentes técnicas de **data embedding** aplicadas a modelos de **regressão quântica**.

## ⚙️ Requisitos e Ambiente

Para rodar os notebooks localmente, é necessário instalar o [**uv**](https://github.com/astral-sh/uv). A instalação é simples e está descrita no repositório oficial.

### Passo a passo:

1. Clone este repositório.

2. Navegue até a pasta principal do projeto `Regressores-Quanticos`.

3. Execute o comando:

   ```bash
   uv venv
   ```

   Esse comando irá criar um ambiente virtual e configurar o kernel do Jupyter automaticamente.

4. No **VS Code**, selecione o kernel correspondente ao ambiente virtual criado na aba de kernels do Jupyter Notebook.

---

## 📂 Estrutura do Projeto

Dentro da pasta `/scripts/Embeddings/`, existe um notebook chamado `exemplo.ipynb`. Ele contém a classe principal que será utilizado nos testes.

Na classe `QuantumRegressor`, há uma função chamada `quantum_circuit`, onde devem ser realizados os testes com diferentes **embeddings**. Essa alteração deve ser feita no seguinte trecho de código:

```python
# Embedding!
features = np.array(x_input)
qml.AngleEmbedding(features=features, wires=range(self.n_qubits), rotation='X')
```

Substitua o `AngleEmbedding` pelo embedding desejado para cada experimento.

---

## 📊 Registro dos Experimentos

Cada experimento deve ser registrado na lista abaixo, informando o nome do embedding utilizado e o responsável pela execução.

Após a conclusão de cada experimento, o responsável deve salvar os resultados em um arquivo `.json`, nomeado de acordo com o embedding utilizado. O conteúdo do arquivo deve seguir a estrutura de uma tabela do Pandas. As métricas a serem registradas podem ser obtidas por meio da função `stats` da classe `QuantumRegressor`.

### ✅ Lista de Experimentos

- `AngleEmbedding` – Lucas Reis
- `Embedding de Fourier` – Eduardo
- `Talysson` – Lucas Reis
---

