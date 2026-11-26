# monitor-motores-python

## Monitoramento de Motores

Este código monitora os motores de diferentes setores como:

1. Estamparia
2. Usinagem
3. Bobinagem
4. Pintura

Em cada setor ele monitora:

- Temperatura
- Corrente
- Vibração
- Rotação
- Potência
- Alertas detectados

Todas as características monitoradas possuem um limite.

*Exemplo: O limite da temperatura é de __80°C__.*

Se algum motor tiver 1 parâmetro fora do limite, ele entra em inspeção programada, mas se tiver mais que 1 parâmetro fora do limite ele entra em estado **crítico**

*Exemplo: __Motor em estado crítico__*

- **Temperatura: 84°C**
- ~~Corrente: 13.3A~~
- **Vibração 5.2 mm/s**
- ~~Rotação: 1600 RPM~~
- ~~Potência 8 kW~~
- Alertas detectados: **Superaquecimento e Vibração elevada**

Após descobrirem quantos parâmetros estão fora do limite eles analisam qual o estado do motor podendo ser:

1. Operação Estável (__*NORMAL*__)
2. Inspeção Programada (__*ATENÇÃO*__)
3. Parada Imediata (__*CRÍTICO*__)

---

Então com esse programa eles conseguem analisar quais motores precisam de uma manutenção antes de quebrar o que ajuda a parar menos a produção.

No final o código demonstra um resumo de todos os parâmetros e motores analisados, mostrando quantos motores foram analisados, a média dos parâmetros e o motor com a maior temperatura:

| Motores | Temp. média | Corr. média | Potência total | Maior temperatura
:---  | :---: | :---: | :---: | ---:
4 |  72.58 C |  15.7 A |  31.5 kW |  MTR-02

Com isso ele consegue fazer uma manutenção preventiva mostrando quais motores estão em cada status ajudando o fornecedor.