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
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="81a25-103">Fluxos de script ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="81a25-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="81a25-104">Quando o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) recebe um arquivo que inclui um fluxo do tipo \_ script WMMEDIATYPE, ele cria um pino de saída para ele que pode ser conectado ao filtro de [processador de comandos de script interno](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="81a25-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="81a25-105">Quando você chama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), esse filtro é adicionado automaticamente ao grafo e conectado.</span><span class="sxs-lookup"><span data-stu-id="81a25-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="81a25-106">Quando o renderizador de comando de script interno recebe um exemplo contendo um comando de script, ele dispara um evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) cujo *lParam* contém o script.</span><span class="sxs-lookup"><span data-stu-id="81a25-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="81a25-107">O aplicativo é totalmente responsável por manipular esse evento.</span><span class="sxs-lookup"><span data-stu-id="81a25-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81a25-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81a25-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81a25-109">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="81a25-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



