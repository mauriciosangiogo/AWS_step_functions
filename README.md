# **Criando um Assistente de Delivery com AWS Step Functions e Bedrock**

## O que é a AWS Step Functions?

Conforme consta na própria página do serviço, o AWS Step Functions "é um serviço de fluxo de trabalho visual que ajuda os desenvolvedores a usar os serviços da AWS para criar aplicações distribuídas, automatizar processos, orquestrar microsserviços e criar pipelines de dados e machine learning (ML)."
Em resumo, o AWS Step Functions é uma ferramenta, que permite montar um fluxo de trabalho completo, conectando diferentes serviços e funções, dispensando o uso de códigos de programação, uma vez que a montagem do fluxo pode ser feita de forma visual "clica e arrasta".

## Como é feito?

- Primeiro, defina seu fluxo de trabalho visual no Workflow Studio, e o console gerará automaticamente o código. Você também pode codificá-lo usando trechos de código no console ou localmente com seu editor de código preferido.
- Especifique os recursos, como funções do Lambda e tópicos do SNS, que você deseja acionar em seu fluxo de trabalho.
- Inicie uma execução para visualizar e verificar se as etapas do seu fluxo de trabalho estão funcionando conforme o esperado. Inspecione e depure seu histórico de execução diretamente do console.
- Provavelmente no primeiro uso será necessário alterar configurações de permissão de perfil, isso porque será necessário habilitar/conceder permissão para que seu usuário tenha acesso aos serviços que estão sendo executados dentro do step functions. Importante ressaltar que para cada estado de máquina é criado um perfil diferente.
- Caso ainda assim ocorra falha na execução, confirmar se o serviço a ser executado dentro da ferramenta está habilitado para sua localização e perfil.

## Custos?

O custo está associado aos serviços que estão sendo executados dentro do fluxo, portanto, para estimar um valor, deve-se realizar a simulação de valores para todos serviços executados dentro do fluxo.
