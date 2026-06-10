# promt aba de acompanhamento

Analise cuidadosamente a estrutura deste projeto antes de fazer qualquer alteração.

O objetivo é ajustar a aba de **Acompanhamento** para que ela reflita corretamente os dados reais do processo de envio digital de documentações.

Contexto do ajuste:

A aba de Acompanhamento precisa usar como base:

1. Todo o histórico da tabela **HISTORICO DE ENVIO DIGITAL** do HANA;
2. Todo o fluxo/processo existente na aba de **Envio de Documentações**;
3. Os gráficos já existentes na tela de Acompanhamento;
4. O mapa de monitoramento geográfico já existente;
5. Os filtros existentes na interface.

Antes de alterar o código, faça uma análise da estrutura atual e identifique:

* Quais arquivos/componentes controlam a aba de Acompanhamento;
* Quais arquivos/componentes controlam a aba de Envio de Documentações;
* Onde estão as chamadas para o HANA ou para a API/backend que busca os dados;
* Onde estão os gráficos já existentes;
* Onde está o mapa de monitoramento geográfico;
* Onde estão os filtros da tela;
* Se existe algum trecho de código duplicado, inconsistente ou com risco de erro;
* Se os dados exibidos atualmente são mockados, filtrados incorretamente ou não refletem todo o histórico real.

Depois da análise, faça os ajustes necessários seguindo estas regras:

1. A aba de **Acompanhamento** deve refletir todo o histórico real da tabela **HISTORICO DE ENVIO DIGITAL** do HANA.

2. Os dados da aba de Acompanhamento também devem estar coerentes com todo o processo existente na aba de **Envio de Documentações**, permitindo acompanhar o fluxo completo das documentações enviadas.

3. Todos os gráficos já existentes devem ser revisados para garantir que:

   * estejam usando dados reais;
   * considerem o histórico completo;
   * respeitem os filtros aplicados;
   * atualizem dinamicamente quando os filtros mudarem;
   * apresentem as informações de forma clara;
   * não quebrem visualmente dentro dos cards;
   * tenham responsividade correta dentro dos cards;
   * não estourem a largura ou altura do container;
   * mantenham boa visualização em diferentes tamanhos de tela.

4. O mapa de monitoramento geográfico deve ser ajustado para refletir os dados reais do histórico de envio digital, considerando corretamente as informações de localização disponíveis.

5. Os filtros da aba de Acompanhamento precisam funcionar de forma dinâmica, afetando corretamente:

   * todos os gráficos;
   * todos os cards;
   * o mapa geográfico;
   * qualquer indicador ou resumo presente na tela.

6. Revise a lógica dos filtros para garantir que não exista conflito entre estado local, estado global, props, query params, cache ou chamadas assíncronas.

7. Revise a estrutura do código para identificar possíveis fontes de erro, como:

   * dados undefined ou null;
   * campos com nomes inconsistentes entre frontend, backend e HANA;
   * conversão incorreta de datas;
   * problemas de timezone;
   * filtros que não são aplicados em todos os componentes;
   * gráficos renderizando antes dos dados carregarem;
   * ausência de loading state;
   * ausência de tratamento de erro;
   * uso de dados mockados;
   * dependências incorretas em useEffect;
   * estados duplicados;
   * problemas de responsividade nos cards;
   * componentes recebendo props incompletas.

8. Crie também um novo gráfico na aba de Acompanhamento para visualizar, ao longo do tempo, a quantidade de entregas realizadas.

Esse novo gráfico deve permitir analisar em quais períodos ocorreram mais entregas.

Sugestão para o novo gráfico:

* Tipo: gráfico de linha ou gráfico de barras temporal;
* Eixo X: período/data da entrega;
* Eixo Y: quantidade de entregas realizadas;
* Deve respeitar os filtros aplicados;
* Deve permitir agrupamento por dia, semana ou mês, se essa estrutura já existir no projeto;
* Deve ficar dentro de um card responsivo;
* Deve seguir o mesmo padrão visual dos demais gráficos da aplicação.

9. Caso seja necessário criar funções utilitárias para tratar os dados, organize-as de forma reutilizável, por exemplo:

   * função para normalizar dados vindos do HANA;
   * função para aplicar filtros;
   * função para agrupar entregas por período;
   * função para preparar dados dos gráficos;
   * função para preparar dados do mapa geográfico.

10. Não reescreva a tela inteira sem necessidade. Preserve a estrutura atual do projeto e altere apenas o necessário.

11. Não remova funcionalidades existentes.

12. Mantenha o padrão de código já utilizado no projeto, incluindo:

* organização de pastas;
* nomes de componentes;
* padrão de hooks;
* padrão de services/APIs;
* biblioteca de gráficos utilizada;
* biblioteca de mapa utilizada;
* padrão visual dos cards;
* padrão de filtros.

13. Antes de implementar, me mostre um resumo da análise com:

* arquivos encontrados;
* componentes envolvidos;
* fluxo atual dos dados;
* possíveis problemas encontrados;
* plano de alteração.

14. Depois implemente os ajustes.

15. Após implementar, revise o código e verifique:

* se não existem imports quebrados;
* se não existem variáveis não utilizadas;
* se os gráficos carregam mesmo quando não há dados;
* se há mensagens adequadas para loading, erro e dados vazios;
* se os filtros atualizam os gráficos e o mapa corretamente;
* se os cards permanecem responsivos;
* se o novo gráfico de entregas ao longo do tempo está funcionando;
* se os dados exibidos vêm do histórico real do HANA.

Critérios de aceitação:

* A aba de Acompanhamento deve exibir dados reais da tabela HISTORICO DE ENVIO DIGITAL.
* Os gráficos existentes devem refletir corretamente o processo de envio digital.
* O mapa geográfico deve refletir os dados reais e responder aos filtros.
* Os filtros devem atualizar dinamicamente gráficos, cards e mapa.
* Os gráficos devem ficar corretamente dimensionados dentro dos cards.
* Deve existir um novo gráfico temporal mostrando a quantidade de entregas realizadas ao longo do tempo.
* O código deve permanecer organizado, sem duplicação desnecessária e sem quebrar funcionalidades existentes.
