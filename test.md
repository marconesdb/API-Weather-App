# Weather App

Este é um projeto simples em TypeScript que consome a API do OpenWeatherMap para consultar as condições do tempo de uma cidade específica.

## Funcionalidades

- Consulta de condições climáticas atuais.
- Exibição de dados como temperatura.
- Exibição de ícone representativo do clima atual.

## Pré-requisitos

- Node.js (versão 14 ou superior)
- npm (versão 6 ou superior)

## Instalação

1. Clone este repositório:

   ```bash
   git clone https://github.com/marconesdb/API-Weather-App.git
   ```

2. Navegue até o diretório do projeto:

   ```bash
   cd Previsao-do-Tempo
   ```

3. Instale as dependências:

   ```bash
   npm install
   ```

## Criação do Projeto

Para criar um projeto em TypeScript do zero, siga os passos abaixo:

1. Inicialize um novo projeto Node.js:

   ```bash
   npm init -y
   ```

2. Instale as dependências necessárias:

   ```bash
   npm install -D typescript 
   ```

3. Inicialize o TypeScript:

   ```bash
   npx tsc --init
   ```

4. No arquivo `tsconfig.json`, configure a saída do TypeScript:

   ```json
   {
     "compilerOptions": {
       "outDir": "./js",
      "noEmitOnError": true, 
     }
   }
   ```

5. O comando npx tsc --watch é usado em projetos TypeScript para compilar os arquivos TypeScript (.ts) em JavaScript (.js) e monitorar as alterações nos arquivos .ts em tempo real. Quando qualquer arquivo TypeScript é alterado, o compilador recompila automaticamente o código, sem a necessidade de executar manualmente o comando de compilação toda vez que você fizer uma mudança.

   ```bash
   npx tsc --watch
   ```


## Configuração

1. Crie sua conta no site https://openweathermap.org/ e gere uma chave API_KEY como essa:

   ```plaintext
   API_KEY=1f400f79f817bc5ae64e794087792064
   ```
2. adicione a chave de sua API no link da API abaixo e remova as chaves:

```
 const resposta = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${localizacao}&appid={API key}lang=pt_br&units=metric`);

```
## Uso

1. Execute o projeto:

   ```bash
   Abra o arquivo index.html e realize a pesquisa com 
   o nome da cidade que deseja ver a temperatura.
   ```

2. O projeto exibirá as informações do tempo para a cidade escolhida.



## Exemplo de Resposta da API

```json
{
  "coord": {
    "lon": -43.8603,
    "lat": -16.735
  },
  "weather": [
    {
      "id": 800,
      "main": "Clear",
      "description": "céu limpo",
      "icon": "01n"
    }
  ],
  "base": "stations",
  "main": {
    "temp": 20.53,
    "feels_like": 20.25,
    "temp_min": 20.53,
    "temp_max": 20.53,
    "pressure": 1016,
    "humidity": 72
  },
  "visibility": 10000,
  "wind": {
    "speed": 1.54,
    "deg": 20
  },
  "clouds": {
    "all": 0
  },
  "dt": 1622849400,
  "sys": {
    "type": 1,
    "id": 8412,
    "country": "BR",
    "sunrise": 1622798827,
    "sunset": 1622840860
  },
  "timezone": -10800,
  "id": 3455923,
  "name": "Montes Claros",
  "cod": 200
}
```

## Contato

- Desenvolvedor: Marcone Silva de Brito
- Email: marconebritt@gmail.com

## Licença

Este projeto está licenciado sob a Licença MIT. 