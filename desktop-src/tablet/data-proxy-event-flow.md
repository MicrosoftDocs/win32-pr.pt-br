---
description: Este tópico discute os detalhes de eventos ao usar os recursos de proxy de dados de análise de tinta.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Flow de evento de proxy de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ae6eab209466094ec79c0ed96923a28751b86c585d9ef750f9d12ef892036c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092798"
---
# <a name="data-proxy-event-flow"></a>Flow de evento de proxy de dados

Este tópico discute os detalhes de eventos ao usar os recursos de proxy de dados de análise de tinta.

## <a name="data-proxy-event-flow-overview"></a>visão geral do evento de Proxy de dados Flow

No uso do proxy de dados do [**InkAnalyzer**](inkanalyzer.md), supõe-se que o aplicativo que integra o InkAnalyzer já tem um modelo de documento existente para o qual desejam fazer o proxy dos resultados da análise. Também pressupõe-se que o aplicativo terá resultados de qualquer operação de análise anterior que desejarem criar no armazenamento em seu modelo de documento. Também pode haver um contexto de não-tinta que pode ser adicionado ao **InkAnalyzer** na forma de um **ImageNode** ou **TextWordNode**[**ContextNode**](icontextnode.md) ser anotado com tinta.

A chave para o sistema de proxy de dados é que o aplicativo sinalize o [**ContextNode**](icontextnode.md) como sendo "parcialmente populado" usando [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md). Quando esse sinalizador é verdadeiro, o [**InkAnalyzer**](inkanalyzer.md) pressupõe que três coisas sobre esse **ContextNode**:

-   O local do [**ContextNode**](icontextnode.md) está correto.
-   O tipo de [**ContextNode**](icontextnode.md) está correto.
-   Todas as outras informações sobre esse [**ContextNode**](icontextnode.md) são armazenadas em outro lugar.

Com base nessas três regras, se e quando o [**InkAnalyzer**](inkanalyzer.md) precisar de informações adicionais sobre um [**ContextNode**](icontextnode.md) , ele gerará o evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) e fará referência ao **ContextNode** em questão. Isso dá ao aplicativo uma oportunidade de definir todas as informações conhecidas sobre esse **ContextNode** antes que o **InkAnalyzer** Examine isso mais detalhadamente. Depois de manipular um evento **PopulateContextNode** , o **ContextNode** em questão deve ter uma propriedade Location válida, o número correto de subnós definido se for um contêiner **ContextNode** ou ter os traços corretos definidos, usando [**setstrokes**](icontextnode-setstrokes.md), se for uma folha de tinta **ContextNode**. A falha ao definir corretamente esse local e o subnó ou as informações de traço resultarão em uma exceção **invalidOperation** . Os subnós para um contêiner **ContextNode** podem ser definidos como parcialmente preenchidos no caso em que mais eventos **PopulateContextNode** serão gerados se o **InkAnalyzer** determinar que eles serão necessários para a operação de análise atual.

As tabelas a seguir descrevem quando o evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) será gerado ao longo do uso do [**InkAnalyzer**](inkanalyzer.md).

Depois que o [**InkAnalyzer**](inkanalyzer.md) tiver computado alguns resultados, ele verificará o aplicativo para atualizar os resultados. O primeiro evento gerado é o evento [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Esse evento simplesmente significa ao aplicativo que o estado da árvore do objeto **InkAnalyzer** está prestes a ser alterado. Isso fornece aos aplicativos uma oportunidade de definir o sinalizador [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) como true em qualquer [**ContextNodes**](icontextnodes.md) que tenha o estado armazenado em outro lugar. O **InkAnalyzer** então gerará uma série de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) para determinar o estado atual dos dados. Uma vez que isso é determiend, uma operação de reconciliação é compelted para determinar quais resultados em segundo plano ainda podem ser aplicados.

Para aplicar os resultados ao [**InkAnalyzer**](inkanalyzer.md) , uma série de eventos de modificação de árvore é gerada. Os eventos de modificação de árvore descrevem, passo a passo, todas as alterações necessárias para atualizar os resultados. Esses eventos devem ser manipulados em Sucession sem interuption ou cancelando. Se a operação de análise for cancelada (por meio do método [**Abort**](iinkanalyzer-abort.md) ) durante o processamento dos eventos de modificação de árvore, o estado do **InkAnalyzer** será inválido e todo o documento poderá precisar ser analisado novamente.

As tabelas a seguir descrevem quando os eventos de modificação de árvore são gerados ao longo do uso do InkAnalyzer. As tabelas referem-se aos carimbos de data/hora mostrados a seguir diagrama de fluxo de eventos.

![iImage mostrando o fluxo entre a interface do usuário do aplicativo e o analisador de segundo plano](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Adicionando um traço



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 e T9<br/> | \[Dentro da chamada para o \] evento de exploração de árvore addstroke () \[\]<br/> | Evento [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerado<br/> | Pode haver n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados dependendo de quantas [**ContextNodes**](icontextnodes.md) não **classificadas** existem com um valor [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) definido como true.<br/> |
| T1, T5 e T9<br/> | \[Evento de modificação de árvore\]<br/>                                  | Evento [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerado<br/>   | Haverá apenas um evento [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerado como resultado da chamada do método [**addstroke**](iinkanalyzer-addstroke.md) . Todos os traços são adicionados ao mesmo [**ContextNode**](icontextnode.md)não classificado.<br/>                      |



 

### <a name="deleting-a-stroke"></a>Excluindo um traço



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 e T10<br/> | \[Dentro da chamada para [](iinkanalyzer-removestroke.md)o evento de \] exploração da árvore RemoveStroke () \[\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/> | Pode haver um número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados dependendo de quantas [**ContextNodes**](icontextnodes.md) relacionadas aos traços sendo excluídos têm um valor de [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) de true.<br/> |
| T2, T6 e T10<br/> | \[Evento de modificação de árvore\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento gerado<br/> | Pode haver qualquer número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) gerados, dependendo do conteúdo de tinta que está sendo excluído e da estrutura de análise atual.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Chamando o método BackgroundAnalyze



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[Dentro da chamada para [](iinkanalyzer-backgroundanalyze.md)o evento de \] exploração da árvore BackgroundAnalyze () \[\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/> | Pode haver n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados, dependendo de quantas [**ContextNodes**](icontextnodes.md) em toda a árvore têm um valor de [**PartiallyPopulated**](icontextnode-createpartiallypopulatedsubnode.md) de true (um evento por [**ContextNode**](icontextnode.md) que é necessário na operação de análise atual).<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Após a chamada para BackgroundAnalyze () retornar



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 para T7<br/>   | \[Eventos gerados a partir do segmento BG\]<br/> | Evento de atividade gerado<br/> | Vários eventos de atividade serão gerados durante este período de fundo de análise.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Quando IntermediateResults estão prontos



| Carimbo de Data/Hora | Tipo de evento ou finalidade | Evento gerado | Comentário                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 T8<br/>   | \[Eventos gerados do BG thread, indicando o início da primeira operação de reconciliação\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Evento gerado<br/>         | Apenas um evento [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) é gerado. Esse evento é gerado antes de inspecionar o estado do [**InkAnalyzer**](inkanalyzer.md), dando ao aplicativo uma oportunidade de definir o valor de [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) em qualquer nó ou executar qualquer bloqueio de documento local necessário.<br/> |
| T7 T8<br/>   | \[Evento de exploração de árvore\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Evento gerado<br/>                   | Pode haver n número de eventos [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                               |
| T7 T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Evento gerado<br/>                     | Pode haver n número de eventos [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                                 |
| T7 T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento gerado<br/>                   | Pode haver n número de eventos [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                               |
| T7 T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Pode haver n número de eventos [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                               |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Pode haver n número de eventos [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                         |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Pode haver n número de [**eventos StrokeReparented**](-ianalysisproxyevents-strokereparented.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                                     |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Pode haver n número de eventos [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                           |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Pode haver n número de eventos [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                       |
| T7 a T8<br/>   | \[Evento de modificação de árvore\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento gerado<br/> | Pode haver n número de [**eventos ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) gerados, dependendo do conteúdo da tinta. **ContextNodePropertiesUpdated** são agendados para serem rasados depois que todos os outros eventos de modificação [**ContextNode**](icontextnode.md) são gerados durante [**esse período de Reconciliação.**](iinkanalyzer-reconcile.md)<br/>              |
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
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Evento gerado<br/>                   | Pode haver qualquer número de [**eventos ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Pode haver qualquer número de eventos [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                             |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Pode haver qualquer número de [**eventos ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                       |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Pode haver qualquer número de [**eventos StrokeReparented**](-ianalysisproxyevents-strokereparented.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                                   |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Pode haver qualquer número de eventos [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) gerados, dependendo do conteúdo de tinta.<br/>                                                                                                                                                                                                                                         |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Pode haver qualquer número de [**eventos ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) gerados, dependendo do conteúdo da tinta.<br/>                                                                                                                                                                                                                                     |
| T11 a T12<br/> | \[Evento de modificação de árvore\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Evento gerado<br/> | Pode haver qualquer número de [**eventos ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) gerados, dependendo do conteúdo da tinta. **ContextNodePropertiesUpdated** são agendados para serem rasados depois que todos os outros eventos de modificação [**ContextNode**](icontextnode.md) são gerados durante [**esse período de Reconciliação.**](iinkanalyzer-reconcile.md)<br/>            |
| T11 a T12<br/> | \[Evento significa o final da segunda operação de reconciliação\]<br/>                            | [**Resultados**](-ianalysisevents-results.md) Evento gerado<br/>                                                | Somente um [**evento Results**](-ianalysisevents-results.md) será gerado por operação de análise.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




