# Web Scraper para Amazon

Este projeto é um scraper que coleta dados de produtos listados na Amazon, permitindo analisar e filtrar informações como título, preço, classificações, número de avaliações e disponibilidade. Os dados são extraídos usando `selenium` e processados com `BeautifulSoup` e `pandas`.

## Funcionalidades

- **Extração de dados**: Coleta título, preço, classificação, avaliações e status de disponibilidade dos produtos.
- **Filtragem de preços**: Permite filtrar produtos com base em um intervalo de preços.
- **Armazenamento de dados**: Salva os resultados em arquivos nos formatos Excel, CSV e JSON.

## Tecnologias Utilizadas

- **Linguagem**: Python 3
- **Bibliotecas**:
  - `selenium` para navegação automatizada.
  - `BeautifulSoup` para parsing de HTML.
  - `pandas` para manipulação de dados.
  - `numpy` para operações numéricas.
  - `webdriver_manager` para gerenciar o ChromeDriver.
  - `concurrent.futures` para processamento paralelo.

## Pré-requisitos

1. **Instalar o Python** (>= 3.7).
2. Instalar as dependências do projeto:

```bash
pip install selenium beautifulsoup4 pandas numpy webdriver-manager
```
3. Ter o navegador Google Chrome instalado.

## Como Usar

1. **Executar o script**:
   - Execute o notebook ou converta-o para um script Python e rode no terminal.

2. **Entrar com o nome do produto**:
   - O script pedirá que você insira o nome do produto que deseja buscar.

3. **Escolher filtro de preços** (opcional):
   - Caso queira, você pode filtrar produtos com preços entre 50% e 100% do preço máximo encontrado.

4. **Salvar os resultados**:
   - Os dados serão salvos automaticamente em três formatos: `amazon_produtos_filtrados.xlsx`, `amazon_produtos_filtrados.csv` e `amazon_produtos_filtrados.json`.

## Estrutura do Projeto

- **Funções principais**:
  - `get_title(soup)`: Extrai o título do produto.
  - `get_price(soup)`: Extrai o preço do produto.
  - `get_rating(soup)`: Extrai a classificação do produto.
  - `get_review_count(soup)`: Extrai o número de avaliações do produto.
  - `get_availability(soup)`: Verifica a disponibilidade do produto.
  - `get_product_details(link)`: Coleta todos os detalhes de um produto.

- **ThreadPoolExecutor**:
  - Realiza requisições simultâneas para melhorar a eficiência da coleta de dados.

## Considerações Finais

Este projeto foi desenvolvido para fins educacionais e demonstração de técnicas de scraping. Certifique-se de seguir os termos de serviço da Amazon ao utilizar este scraper. Adapte o tempo entre requisições para evitar bloqueios do site.

## Licença

Este projeto está disponível sob a licença MIT. Sinta-se à vontade para usá-lo e modificá-lo conforme necessário.

