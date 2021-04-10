---
title: Fluxos de script no DirectShow
description: Fluxos de script no DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, fluxos de script
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- DirectShow, fluxos de script
- fluxos de script, DirectShow
- fluxos, fluxos de script no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292732"
---
# <a name="script-streams-in-directshow"></a><span data-ttu-id="d25ff-112">Fluxos de script no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d25ff-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="d25ff-113">Quando o filtro de leitor ASF do WM recebe um arquivo que inclui um fluxo do tipo \_ script WMMEDIATYPE, ele cria um pino de saída para ele que pode ser conectado ao filtro de processador de comandos de script interno do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d25ff-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="d25ff-114">Quando você chama **IGraphBuilder:: RenderFile**, esse filtro é adicionado automaticamente ao grafo e conectado.</span><span class="sxs-lookup"><span data-stu-id="d25ff-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="d25ff-115">Quando o renderizador de comando de script interno recebe um exemplo contendo um comando de script, ele dispara um **\_ \_ evento OLE do EC** cujo **lParam** contém o script.</span><span class="sxs-lookup"><span data-stu-id="d25ff-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="d25ff-116">O aplicativo é totalmente responsável por manipular esse evento.</span><span class="sxs-lookup"><span data-stu-id="d25ff-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="d25ff-117">Para obter mais informações sobre o **\_ \_ evento OLE do EC**, consulte a documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d25ff-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




