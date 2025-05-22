# 📍 Geolocalização de CEPs com Nominatim (OpenStreetMap) no Google Colab

Este projeto realiza a geolocalização de uma lista de CEPs brasileiros, consultando a latitude e longitude correspondente de cada um usando a API gratuita do **Nominatim** (OpenStreetMap).

## ⚙️ Funcionalidades

- Upload de planilha com coluna de CEPs (`.xlsx`)
- Limpeza e formatação dos CEPs
- Consulta à API Nominatim
- Geração de coordenadas geográficas (latitude/longitude)
- Exportação de nova planilha com os dados geolocalizados

## 🚀 Como usar no Google Colab

1. Acesse o notebook no Colab [aqui](https://colab.research.google.com/)
2. Faça upload da sua planilha Excel contendo a coluna `CEP`
3. O script processará os CEPs e gerará uma nova planilha para download

## 📝 Estrutura da planilha esperada

| CEP         |
|-------------|
| 01001-000   |
| 01310-100   |
| 04094-050   |

## 📦 Requisitos

O Colab instalará automaticamente:

- pandas
- openpyxl
- requests
- tqdm

## 🔁 API utilizada

A API usada é a do [Nominatim - OpenStreetMap](https://nominatim.openstreetmap.org/), respeitando os limites de uso da plataforma.

**Importante:** Para evitar bloqueios, é necessário enviar um cabeçalho `User-Agent`, que já está incluído no script.

## 📂 Saída

A saída será uma planilha `.xlsx` com as seguintes colunas:

| CEP       | Latitude   | Longitude   |
|-----------|------------|-------------|
| 01001000  | -23.5505   | -46.6333    |

## 🛑 Limitações

- A API do Nominatim possui limites de uso por segundo e por IP.
- Requisições em massa devem ser feitas com pausas (`sleep`) para evitar bloqueio.

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

Desenvolvido para fins acadêmicos e educacionais.
