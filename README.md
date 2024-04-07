# Plataforma de Viagens de Carro Compartilhadas

## Introdução

Este projeto faz parte de uma solução maior voltada para viagens de carro compartilhadas por aplicativo. A funcionalidade central deste módulo é encontrar a corrida mais próxima para o motorista, dado um mapa de solicitações de corrida.

## Funcionalidade

O algoritmo desenvolvido, `findNewRide(driverPositionX, driverPositionY)`, utiliza um mapa 2D para localizar a solicitação de corrida mais próxima do motorista, com base nas suas coordenadas atuais. O mapa representa um pequeno bairro de 16x16 posições, onde as posições com o valor `1` indicam uma solicitação de corrida.

### Mapa de Passageiros

O mapa de passageiros é uma matriz 16x16 que simula as solicitações de corrida em um bairro, conforme o exemplo abaixo:

```javascript
const passengerMap = [
    [0, 0, 0, ..., 0],
    [0, 1, 0, ..., 0],
    ...,
    [0, 0, 0, ..., 1]
];
```

### Utilização

Para encontrar a corrida mais próxima, utilize a função `findNewRide(driverPositionX, driverPositionY)`, passando as coordenadas atuais do motorista. O retorno será um array contendo as coordenadas do passageiro mais próximo e a distância até ele, em quilômetros, com duas casas decimais.

### Exemplo de Retorno

```javascript
[[7, 0], '7.00 km']
```

## Testes

O projeto inclui 256 casos de teste, cobrindo todas as possíveis posições do motorista no bairro simulado. Os testes ajudam a verificar a precisão do algoritmo em encontrar a corrida mais próxima. O resultado dos testes será exibido no console, indicando `PASS` para testes bem-sucedidos e `FAIL` para falhas, junto com as coordenadas testadas.

## Requisitos

- Precisão na localização da corrida mais próxima.
- Funcionamento perfeito para todos os 256 casos de teste.
- Cálculo da distância utilizando a distância euclidiana.

## Desenvolvimento

Este módulo foi desenvolvido com foco na eficiência e precisão, utilizando conceitos de arrays e laços aninhados para iterar pelo mapa de passageiros e calcular a distância até as solicitações de corrida.

---
