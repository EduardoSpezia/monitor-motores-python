# monitor-motores-python

## Monitoramento de Motores

Este código monitora os motores de diferentes setores como:

1. Estamparia
2. Usinagem
3. Bobinagem
4. Pintura

Em cada setor ele monitora a temperatura, corrente, vibração, Rotação, potência e alertas detectados mostrando tudo para o usuário.

Todas as características monitoradas possuem um limite.

Exemplo: O limite da temperatura é de **80°C**.

Se algum motor tiver 1 parâmetro fora do limite, ele entra em inspeção programa, mas se tiver mais que 1 parâmetro fora do limite ele entra em estado **crítico**

Exemplo: **Motor em estado crítico**

- **Temperatura: 84°C**
- Corrente: 13.3A
- **Vibração 5.2 mm/s**
- Rotação: 1600 RPM
- Potência 8 kW
- Alertas detectados: **Superaquecimento e Vibração elevada**

Após descobrirem quantos parâmetros estão fora do limite eles analisam qual o estado do motor podendo ser:

1. Operação Estável (NORMAL)
2. Inspeção Programada (ATENÇÃO)
3. Parada Imediata (CRÍTICO)

Então com esse programa eles conseguem analisar quais motores precisam de uma manutenção antes de quebrar o que ajuda a parar menos a produção