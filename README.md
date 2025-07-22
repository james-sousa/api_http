# API de Eventos (Python HTTPServer)

API simples para gerenciamento e listagem de eventos presenciais e online, desenvolvida com a biblioteca nativa `http.server`. Ideal para fins educacionais ou portfólio pessoal.

---

## Estrutura do Projeto

```
.
├── evento.py            # Classe base Evento
├── evento_online.py     # Subclasse EventoOnline
├── server.py            # Servidor HTTP com rotas HTML e JSON
```

---

## Como Executar

1. **Clone o repositório:**

```bash
git clone https://github.com/james-sousa/api_http.git
cd api_http
```

2. **Execute o servidor (Python 3):**

```bash
python3 server.py
```

3. **Acesse no navegador ou ferramentas como `curl` ou `Postman`:**

```
http://localhost:8000
```

---

## Rotas Disponíveis

### `GET /`

* Página HTML simples de teste.

### `GET /eventos`

* Retorna uma **página HTML com tabela** listando todos os eventos.

### `GET /api/eventos`

* Retorna um **JSON** com todos os eventos registrados.

### Exemplo de resposta JSON:

```json
[
  {
    "id": 1,
    "nome": "live python",
    "local": "https://tamarcado.com/eventos?id=1"
  },
  {
    "id": 2,
    "nome": "Live java",
    "local": "https://tamarcado.com/eventos?id=2"
  },
  {
    "id": 3,
    "nome": "Aula de java",
    "local": "Picos"
  }
]
```

---

## Estrutura das Classes

### `Evento`

* Atributos:

  * `id`: Identificador único
  * `nome`: Nome do evento
  * `local`: Local do evento
* Métodos:

  * `imprime_informacoes()`: imprime dados no terminal
  * `to_json()`: exporta como JSON
  * `calcula_limite_pessoas_area(area)`: define limite de pessoas com base na área (m²)

### `EventoOnline (Evento)`

* Herda de `Evento`, sobrescreve o `local` com um link único.
* Redefine `imprime_informacoes()`.

---

## Tecnologias Utilizadas

* Python 3
* Módulo nativo `http.server`
* Programação orientada a objetos (POO)

---

## Possíveis Melhorias Futuras

* Suporte a métodos `POST`, `PUT`, `DELETE`
* Uso de frameworks como Flask ou FastAPI
* Armazenamento em banco de dados (ex: SQLite)
* Testes automatizados com `unittest` ou `pytest`
* Documentação com Swagger/OpenAPI
* Interface frontend com HTML + JS

---

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais informações.

---

## Autor

Desenvolvido por [james sousa](https://github.com/seu-usuario) — entre em contato!
