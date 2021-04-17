---
description: Depois de criar um documento HTML de origem do ERP (página de referência de evento), você deve nomeá-lo antes que Monitor de Rede possa exibi-lo no Visualizador de Eventos.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Nomeando uma página de referência de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748426"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="074c3-103">Nomeando uma página de referência de evento</span><span class="sxs-lookup"><span data-stu-id="074c3-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="074c3-104">Depois de criar um documento HTML de origem do ERP (página de referência de evento), você deve nomeá-lo antes que Monitor de Rede possa exibi-lo no Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="074c3-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="074c3-105">Monitor de nome e arquivos ERP de especialistas com este formato:</span><span class="sxs-lookup"><span data-stu-id="074c3-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="074c3-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**Especialistaname**</span><span class="sxs-lookup"><span data-stu-id="074c3-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="074c3-107">Nome do arquivo DLL, excluindo a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="074c3-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="074c3-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="074c3-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="074c3-109">Identificador de evento do especialista em ERP.</span><span class="sxs-lookup"><span data-stu-id="074c3-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="074c3-110">O identificador de evento também é encontrado no membro **EventIdent** da estrutura **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="074c3-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="074c3-111">Para obter mais informações sobre como criar um ERP, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="074c3-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="074c3-112">Criando páginas de referência de evento expert e monitor</span><span class="sxs-lookup"><span data-stu-id="074c3-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="074c3-113">Escrevendo uma página de referência de evento</span><span class="sxs-lookup"><span data-stu-id="074c3-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="074c3-114">Testando uma página de referência de evento</span><span class="sxs-lookup"><span data-stu-id="074c3-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



