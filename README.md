# Steam (SteamDB) — Web Scraping com Selenium

Este projeto automatiza um navegador (headless) para acessar a página do **SteamDB** e coletar/inspecionar elementos HTML.

## O que foi feito

O script `script_data_stem.py` executa o seguinte fluxo:

1. Instala/ativa o ChromeDriver via `chromedriver_autoinstaller`.
2. Inicia o Selenium com:
   - `headless=True`
   - configuração de janela
3. Acessa a URL base do site:
   - `https://steamdb.info/`
4. Busca elementos na página por classe (`By.CLASS_NAME`, por exemplo `span6`).
5. Usa **BeautifulSoup** para parsear o HTML retornado.
6. Itera pelas linhas/tabelas encontradas (há um `for table in soup.find_all("tr"):`).

## Arquivo

- `script_data_stem.py`
  - Código principal de scraping/inspeção.
  - Usa Selenium + BeautifulSoup.

## Fonte dos dados

- SteamDB
  - `https://steamdb.info/`

## Como executar

No diretório `WebScraping-Python/Steam`, execute:

```bash
python script_data_stem.py
```
