---
description: Fluxos de script ASF no DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Fluxos de script ASF no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919998"
---
# <a name="asf-script-streams-in-directshow"></a>Fluxos de script ASF no DirectShow

Quando o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) recebe um arquivo que inclui um fluxo do tipo \_ script WMMEDIATYPE, ele cria um pino de saída para ele que pode ser conectado ao filtro de [processador de comandos de script interno](internal-script-command-renderer-filter.md) . Quando você chama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), esse filtro é adicionado automaticamente ao grafo e conectado. Quando o renderizador de comando de script interno recebe um exemplo contendo um comando de script, ele dispara um evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) cujo *lParam* contém o script. O aplicativo é totalmente responsável por manipular esse evento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



