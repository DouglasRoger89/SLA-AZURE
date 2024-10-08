# SLA-AZURE

Termo 	Definição
Objetivo de nível de serviço (SLO) 	Uma medida do desempenho e da confiabilidade de uma carga de trabalho ou aplicativo. Um SLO é um alvo específico e mensurável definido para interações específicas com o cliente. É um destino que você define para sua carga de trabalho no aplicativo com base na qualidade do serviço que seus usuários devem esperar receber.
Indicador de nível de serviço (SLI) 	Uma métrica emitida por um serviço. As métricas de SLI são agregadas para quantificar um valor de SLO.
SLA (Contrato de Nível de Serviço) 	Um acordo contratual entre o prestador de serviços e o cliente do serviço. O não cumprimento do contrato pode ter consequências financeiras para o prestador de serviços.
Tempo médio para recuperação (MTTR) 	O tempo necessário para restaurar um componente após a detecção de uma falha.
Tempo médio entre falhas (MTBF) 	A duração pela qual a carga de trabalho pode executar a função esperada sem interrupção, até que ela falhe.
RTO (objetivo de tempo de recuperação) 	Tempo máximo aceitável que um aplicativo pode ficar indisponível após um incidente.
RPO (Objetivo de Ponto de Recuperação) 	A duração máxima aceitável da perda de dados durante um incidente.

SLOs e SLAs

Um SLO é uma medida do desempenho e da confiabilidade de uma carga de trabalho ou aplicativo. Um SLO é um alvo específico e mensurável definido para interações específicas com o cliente. É uma meta que você define para sua carga de trabalho ou aplicativo sobre a qualidade do serviço que seus usuários devem esperar receber.

Um SLO pode ser definido em termos de uma variedade de métricas, como disponibilidade, tempo de resposta, taxa de transferência, taxa de sucesso e outras. Por exemplo, um SLO para um serviço Web pode ser que ele estará disponível para os usuários 99,9% do tempo em um determinado mês, ou que responderá a 95% das solicitações dentro de 500 milissegundos.

Antes de definir os SLOs para seu aplicativo ou carga de trabalho, revise os SLAs publicados pela Microsoft para os serviços subjacentes nos quais seu aplicativo ou carga de trabalho está hospedado.

Valores de SLA

A tabela a seguir define valores comuns de SLA.


![image](https://github.com/user-attachments/assets/612669ca-61b0-4015-a521-9201a045bfff)

LES

Pense em SLIs como métricas de nível de componente que contribuem para um SLO. Os SLIs mais significativos são aqueles que afetam seus fluxos críticos da perspectiva de seus clientes. Para muitos fluxos, as SLIs incluem latência, taxa de transferência, taxa de erro e disponibilidade. Um bom SLI ajuda a identificar quando um SLO corre o risco de ser violado. Correlacione o SLI a clientes específicos quando possível.

Para evitar a coleta de métricas inúteis, limite o número de SLIs para cada fluxo. Busque três SLIs por fluxo, se possível.
Métricas de recuperação

Os destinos de recuperação correspondem às métricas RTO, RPO, MTTR e MTBF. Em contraste com as metas de disponibilidade, as metas de recuperação para essas medições não dependem muito dos SLAs da Microsoft. A Microsoft publica garantias de RTO e RPO apenas para alguns produtos, como o Banco de Dados SQL.

As definições para metas de recuperação realistas dependem de sua análise de modo de falha e de seus planos e testes para continuidade de negócios e recuperação de desastres. Antes de concluir este trabalho, discuta as metas aspiracionais com as partes interessadas e certifique-se de que seu projeto de arquitetura ofereça suporte às metas de recuperação da melhor maneira possível. Comunique claramente às partes interessadas que quaisquer fluxos ou cargas de trabalho inteiras que não sejam exaustivamente testadas para métricas de recuperação não devem ter SLAs garantidos. Certifique-se de que as partes interessadas entendam que as metas de recuperação podem mudar ao longo do tempo à medida que as cargas de trabalho são atualizadas. A carga de trabalho pode se tornar mais complexa à medida que os clientes são adicionados ou à medida que você adota novas tecnologias para melhorar a experiência do cliente. Essas alterações podem aumentar ou diminuir suas métricas de recuperação.

