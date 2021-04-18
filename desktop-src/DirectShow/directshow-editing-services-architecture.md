---
description: Arquitetura de serviços de edição do DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Arquitetura de serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105751669"
---
# <a name="directshow-editing-services-architecture"></a>Arquitetura de serviços de edição do DirectShow

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

A ilustração a seguir mostra a arquitetura dos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

![arquitetura de serviços de edição do DirectShow](images/architecture.png)

-   Linha do tempo: representa uma produção de vídeo como uma coleção de clipes de origem, transições e efeitos, organizados em um conjunto de faixas aninhadas. Para obter mais informações, consulte [o modelo de linha do tempo](the-timeline-model.md).
-   Analisador XML: analisa a linha do tempo e gera um arquivo de saída, ou lê um arquivo de entrada e gera uma linha do tempo. O DES dá suporte a um formato de persistência baseado em XML.
-   Mecanismo de renderização: traduz a linha do tempo em um formulário que pode ser renderizado como mídia de streaming. Por padrão, o mecanismo de renderização produz um grafo de filtro do DirectShow (consulte a próxima seção).
-   Localizador de mídia: mantém um cache de locais de elementos de mídia. Quando uma tentativa de abrir um elemento de mídia falha, o DES usa o cache para localizar o elemento, com base em um histórico de aberturas bem-sucedidas.

A linha do tempo é uma descrição abstrata de um projeto de edição de vídeo. Ele especifica os clipes de origem usados no projeto, os horários de início e de parada, efeitos e transições e assim por diante. No entanto, a linha do tempo não renderiza os fluxos de vídeo e áudio. Em vez disso, o mecanismo de renderização converte a linha do tempo em um grafo de filtro, para visualização ou saída de arquivo. Um aplicativo manipula a linha do tempo em vez de manipular diretamente o grafo de filtro, o que seria complicado e propenso a erros.

A tabela a seguir lista as principais tarefas que um aplicativo de edição de vídeo típico executa, juntamente com as interfaces que oferecem suporte a cada tarefa. As seções posteriores descrevem essas tarefas e as interfaces mais detalhadamente.



| Tarefa                                     | Interface (s)                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| Construa ou modifique uma linha do tempo.          | [**IAMTimeline**](iamtimeline.md) e as outras interfaces **IAMTimelineXXXX**          |
| Salvar e carregar arquivos de projeto.             | [**IXml2Dex**](ixml2dex.md)                                                             |
| Visualizar um projeto ou gravá-lo em um arquivo. | [**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md) |



 

Além disso, um aplicativo pode executar algumas ou todas as tarefas secundárias a seguir.



| Tarefa                                                                                           | Interface (s)                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtenha informações sobre arquivos de mídia. (Número de fluxos; formato e duração de cada fluxo.) | [**IMediaDet**](imediadet.md)                                               |
| Defina as propriedades em transições e efeitos.                                                     | [**IPropertySetter**](ipropertysetter.md)                                   |
| Receber notificação quando ocorrerem erros durante a renderização.                                       | [**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md) |
| Recuperar quadros de pôster.                                                                        | [**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com os serviços de edição do DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



