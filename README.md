# promt aba de acompanhamento

Analise a estrutura deste projeto sem fazer alterações ainda.

Quero entender como estão organizadas:

* a aba de Acompanhamento;
* a aba de Envio de Documentações;
* os gráficos da aba de Acompanhamento;
* o mapa de monitoramento geográfico;
* os filtros;
* as chamadas para o HANA ou API/backend;
* o uso da tabela HISTORICO DE ENVIO DIGITAL.

Identifique quais arquivos e componentes estão envolvidos, como os dados fluem até os gráficos e o mapa, e aponte possíveis problemas como dados mockados, filtros incompletos, inconsistência de campos, problemas de responsividade nos cards, estados duplicados ou chamadas assíncronas mal estruturadas.

Não altere o código ainda. Apenas apresente a análise e um plano de ajustes.



Agora implemente os ajustes com base na análise anterior.

Agora implemente os ajustes com base na análise anterior.

A aba de **Acompanhamento** deve refletir os dados reais da tabela **HISTORICO DE ENVIO DIGITAL** do HANA e o processo completo da aba de **Envio de Documentações**.

Ajuste os gráficos existentes, o mapa geográfico e os filtros para funcionarem de forma dinâmica e coerente.

Garanta que os gráficos fiquem responsivos dentro dos cards, sem estourar largura ou altura, mantendo o padrão visual atual.

Atenção: os **KPIs de pendentes** não devem ser calculados com base no histórico da tabela **HISTORICO DE ENVIO DIGITAL**, pois pendente representa a situação atual do processo. Esses KPIs devem usar os dados atuais da aba de **Envio de Documentações** ou a base/API atual correspondente.

Use o histórico apenas para informações de eventos passados, como entregas realizadas, tentativas, evolução temporal, timeline, gráficos históricos e análises por período.

Além disso, crie um novo gráfico temporal mostrando a quantidade de entregas realizadas ao longo do tempo, para permitir analisar em quais períodos ocorreram mais entregas.

Esse novo gráfico deve usar os dados reais do histórico, considerar apenas entregas realizadas/concluídas, respeitar os filtros aplicados e seguir o mesmo padrão visual dos demais gráficos.

Revise também o mapa de monitoramento geográfico para refletir os dados reais solicitados e responder corretamente aos filtros.

Preserve a estrutura atual do projeto, altere apenas o necessário, mantenha o padrão visual existente e revise possíveis erros de código, estados, filtros, imports, loading, tratamento de erro, dados vazios, dados nulos, datas inválidas e uso indevido de dados mockados.

Critérios de aceitação:

* A aba de Acompanhamento deve exibir dados reais.
* O histórico deve vir da tabela HISTORICO DE ENVIO DIGITAL do HANA.
* KPIs de pendentes devem usar os dados atuais do processo, não o histórico.
* Gráficos históricos devem usar o histórico real.
* Os filtros devem atualizar KPIs, gráficos e mapa dinamicamente.
* O mapa geográfico deve refletir os dados reais.
* Os gráficos devem ficar responsivos dentro dos cards.
* Deve existir um novo gráfico temporal de entregas realizadas ao longo do tempo.
* O código deve continuar organizado, sem quebrar funcionalidades existentes.

