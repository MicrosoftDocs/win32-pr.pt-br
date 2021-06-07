---
description: Este tópico discute os detalhes do evento ao usar os recursos de proxy de dados de análise de tinta.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Fluxo de eventos de proxy de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b88fbb43e54b19486a6413bc44319fa2dd737486
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432538"
---
# <a name="data-proxy-event-flow"></a>Fluxo de eventos de proxy de dados

Este tópico discute os detalhes do evento ao usar os recursos de proxy de dados de análise de tinta.

## <a name="data-proxy-event-flow-overview"></a>Visão geral do fluxo de eventos do proxy de dados

No uso do proxy de dados do [**InkAnalyzer,**](inkanalyzer.md)supõe-se que o aplicativo que integra o InkAnalyzer já tenha um modelo de documento existente ao qual deseja proxy os resultados da análise. Supõe-se também que o aplicativo terá resultados de qualquer operação de análise anterior que deseja criar com base no armazenado em seu modelo de documento. Também pode haver contexto sem tinta que pode ser adicionado ao **InkAnalyzer** na forma de **um ImageNode** ou **TextWordNode**[**ContextNode**](icontextnode.md) a ser potencialmente anotado com tinta.

A chave para o sistema de proxy de dados é para o aplicativo sinalizar [**o ContextNode**](icontextnode.md) como sendo "parcialmente populado" usando [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md). Quando esse sinalizador é verdadeiro, [**o InkAnalyzer**](inkanalyzer.md) pressupo que três coisas sobre esse **ContextNode**:

-   O local do [**ContextNode**](icontextnode.md) está correto.
-   O tipo de [**ContextNode**](icontextnode.md) está correto.
-   Todas as outras informações sobre esse [**ContextNode**](icontextnode.md) são armazenadas em outro lugar.

Com base nessas três regras, se e quando o [**InkAnalyzer**](inkanalyzer.md) precisar de informações adicionais sobre [**um ContextNode,**](icontextnode.md) ele aumentará o evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) e fará referência ao **ContextNode** em questão. Isso dá ao aplicativo a oportunidade de definir todas as informações conhecidas sobre **esse ContextNode** antes que **o InkAnalyzer** o consulte mais detalhadamente. Depois de manipular um evento **PopulateContextNode,** **o ContextNode** em questão deve ter uma propriedade de local válida, o número correto de sub-nós definido se for um **contextNode** de contêiner ou ter os traços corretos definidos, usando [**SetStrkes**](icontextnode-setstrokes.md), se for uma folha de tinta **ContextNode**. A falha ao definir corretamente esse local e informações de subnónodo ou traço resultará em uma **exceção InvalidOperation.** Os sub-nós de um contêiner **ContextNode** podem ser definidos como parcialmente preenchidos; nesse caso, mais eventos **PopulateContextNode** serão gerados se o **InkAnalyzer** determinar que eles serão necessários para a operação de análise atual.

As tabelas a seguir descrevem quando [**o evento PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) será gerado durante o uso do [**InkAnalyzer.**](inkanalyzer.md)

Depois que [**o InkAnalyzer**](inkanalyzer.md) tiver calculado algumas restuls, ele voltará para o aplicativo para atualizar os resultados. O primeiro evento gerado é o [**evento InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Esse evento simplesmente significa para o aplicativo que o estado da árvore do objeto **InkAnalyzer** está prestes a mudar. Isso fornece aos aplicativos uma oportunidade de definir o sinalizador [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) como true em [**todos os ContextNodes**](icontextnodes.md) que têm o estado armazenado em outro lugar. Em seguida, o **InkAnalyzer** vai alocar uma série de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) para determinar o estado atual dos dados. Uma vez que é impedida, uma operação de reconciliação é compelda para determinar quais resultados em segundo plano ainda podem ser aplicados.

Para aplicar resultados ao [**InkAnalyzer, uma**](inkanalyzer.md) série de eventos de modificação de árvore são gerados. Os eventos de modificação de árvore descrevem, passo a passo, todas as alterações necessárias para atualizar os resultados. Esses eventos devem ser tratados com êxito sem interupção ou cancelamento. Se a operação de análise for cancelada (por meio do método [**Abort)**](iinkanalyzer-abort.md) durante o processamento dos eventos de modificação de árvore, o estado do **InkAnalyzer** será inválido e o documento inteiro poderá precisar ser analisado de novo.

As tabelas a seguir descrevem quando os eventos de modificação de árvore são gerados durante o uso do InkAnalyzer. As tabelas referem-se aos timestamps mostrados após o diagrama de fluxo de eventos.

![iimage mostrando o fluxo entre a interface do usuário do aplicativo e o analisador de segundo plano](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Adicionando um traço



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 e T9<br/> | \[Dentro da chamada para Evento de exploração \] \[ de árvore AddStrke()\]<br/> | [**Evento PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerado<br/> | Pode haver n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados dependendo de quantos [**ContextNodes**](icontextnodes.md) não classificados existem com um valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) definido como true.<br/> |
| T1, T5 e T9<br/> | \[Evento de modificação de árvore\]<br/>                                  | [**Evento ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerado<br/>   | Haverá apenas um evento [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerado como resultado da chamada ao [**método AddStrke.**](iinkanalyzer-addstroke.md) Todos os traços são adicionados ao mesmo [**ContextNode não classificado.**](icontextnode.md)<br/>                      |



 

### <a name="deleting-a-stroke"></a>Excluindo um traço



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 e T10<br/> | \[Dentro da chamada para [**RemoveStrke**](iinkanalyzer-removestroke.md)() \] \[ Evento de exploração de árvore\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/> | Pode haver vários eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados dependendo de quantos [**ContextNodes**](icontextnodes.md) relacionados aos traços que estão sendo excluídos têm um valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) de true.<br/> |
| T2, T6 e T10<br/> | \[Evento de modificação de árvore\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento gerado<br/> | Pode haver qualquer número de [**eventos ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) gerados, dependendo do conteúdo de tinta que está sendo excluído e da estrutura de Análise atual.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Chamando o método BackgroundAnalyze



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[Dentro da chamada para [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)() \] \[ Evento de exploração de árvore\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/> | Pode haver n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados, dependendo de quantos [**ContextNodes**](icontextnodes.md) em toda a árvore têm um valor [**PartiallyPopulated**](icontextnode-createpartiallypopulatedsubnode.md) de true (um evento por [**ContextNode**](icontextnode.md) necessário na operação de Análise atual).<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Após a chamada para BackgroundAnalyze() retornar



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 a T7<br/>   | \[Eventos gerados do thread BG\]<br/> | Evento de atividade gerado<br/> | Vários eventos de atividade serão gerados durante esse período de análise em segundo plano.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Quando IntermediateResults estiver pronto



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 a T8<br/>   | \[Eventos gerados do thread BG, que significam o início da primeira operação de reconciliação\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento gerado<br/>         | Apenas um [**evento InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) gerado. Esse evento é gerado antes de inspecionar o estado do [**InkAnalyzer,**](inkanalyzer.md)dando ao aplicativo a oportunidade de definir o valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) em qualquer nós ou executar qualquer bloqueio de documento local necessário.<br/> |
| T7 a T8<br/>   | \[Evento de exploração de árvore\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/>                   | Pode haver n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento gerado<br/>                     | Pode haver n número de eventos [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                                 |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento gerado<br/>                   | Pode haver n número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Pode haver n número de eventos [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Pode haver n número de eventos [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                         |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Pode haver n número de [**eventos StrokeReparented**](-ianalysisproxyevents-strokereparented.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                                     |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Pode haver n número de eventos [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                           |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Pode haver n número de eventos [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                       |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento gerado<br/> | Pode haver n número de [**eventos ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) gerados, dependendo do conteúdo da tinta. **ContextNodePropertiesUpdated** são agendados para serem rasados depois que todos os outros eventos de modificação [**ContextNode**](icontextnode.md) são gerados durante esse [**período de Reconciliação.**](iinkanalyzer-reconcile.md)<br/>              |
| T7 a T8<br/>   | \[Evento significa o fim da primeira operação de reconciliação\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) Evento gerado<br/>                        | Somente um [**evento IntermediateResults**](-ianalysisevents-intermediateresults.md) será gerado por operação de análise.<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>Depois que IntermediateResults tiver sido tratado



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| T8 a T11<br/>  | \[Eventos gerados do thread BG\]<br/> | [**Atividade**](-ianalysisevents-activity.md) Evento gerado<br/> | Vários [**eventos de**](-ianalysisevents-activity.md) atividade serão gerados durante esse período de análise em segundo plano.<br/> |



 

### <a name="when-final-results-are-ready"></a>Quando os resultados finais estão prontos



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T11 a T12<br/> | \[Eventos gerados do thread BG, que significam o início da segunda operação de reconciliação\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento gerado<br/>         | Apenas um [**evento InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) gerado. Esse evento é gerado antes de inspecionar o estado do [**InkAnalyzer,**](inkanalyzer.md)dando ao aplicativo a oportunidade de definir o valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) em qualquer nós ou executar qualquer bloqueio de documento local necessário.<br/> |
| T11 a T12<br/> | \[Evento de exploração de árvore\]<br/>                                                               | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/>                   | Pode haver qualquer número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento gerado<br/>                     | Pode haver qualquer número de [**eventos ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                               |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento gerado<br/>                   | Pode haver qualquer número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Pode haver qualquer número de eventos [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Pode haver qualquer número de [**eventos ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                       |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Pode haver qualquer número de [**eventos StrokeReparented**](-ianalysisproxyevents-strokereparented.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                                   |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Pode haver qualquer número de eventos [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) gerados, dependendo do conteúdo de tinta.<br/>                                                                                                                                                                                                                                         |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Pode haver qualquer número de [**eventos ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                     |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento gerado<br/> | Pode haver qualquer número de [**eventos ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) gerados, dependendo do conteúdo da tinta. **ContextNodePropertiesUpdated** são agendados para serem rasados depois que todos os outros eventos de modificação [**ContextNode**](icontextnode.md) são gerados durante esse [**período de Reconciliação.**](iinkanalyzer-reconcile.md)<br/>            |
| T11 a T12<br/> | \[Evento significa o fim da segunda operação de reconciliação\]<br/>                            | [**Resultados**](-ianalysisevents-results.md) Evento gerado<br/>                                                | Somente um [**evento Results**](-ianalysisevents-results.md) será gerado por operação de análise.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




