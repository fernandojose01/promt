#promt visão de processo e envio de documentos
Analise o projeto sem fazer alterações ainda.

Preciso identificar por que o histórico/detalhamento do cliente está exibindo registros inexistentes, repetidos, em branco e fora da ordem cronológica.

Verifique principalmente:

* aba de Envio de Documentações;
* detalhamento do cliente;
* histórico do cliente;
* timeline da aba de Envio de Documentações;
* aba de Visão de Processo;
* timeline da Visão de Processo;
* contagem de tentativas;
* hover/tooltip das tentativas;
* status dos tipos de documentos como entregue ou não entregue;
* services/APIs/bases usados para comunicações de entrega de documentos.

Quero que você me diga:

1. Quais arquivos estão envolvidos;
2. Como os dados chegam até o histórico e as timelines;
3. Onde pode estar surgindo duplicidade;
4. Onde podem estar surgindo registros em branco;
5. Onde a ordenação cronológica é feita;
6. Onde a contagem de tentativas é calculada;
7. Onde o status de documento entregue/não entregue é definido;
8. Qual seria o melhor plano de ajuste para centralizar a lógica e reaproveitar na Visão de Processo.

Não altere o código ainda.

Agora implemente os ajustes com base na análise anterior.

Corrija o histórico/detalhamento do cliente para mostrar apenas registros reais das bases de comunicações de entrega de documentos.

Remova registros repetidos, registros em branco e registros inexistentes.

Corrija a ordenação cronológica dos eventos.

Centralize a lógica da timeline da aba de Envio de Documentações em uma função, hook ou utilitário reutilizável, e aplique a mesma lógica na timeline da Visão de Processo.

Garanta que as contagens das duas abas batam.

Ajuste a coluna de tentativas da Visão de Processo para usar a mesma lógica de contagem e o mesmo hover/tooltip da aba de Envio de Documentações.

Corrija a lógica dos tipos de documentos na timeline da Visão de Processo para que documentos entregues não apareçam como não entregues.

Preserve a estrutura atual do projeto, mantenha o padrão visual existente e altere apenas o necessário.
