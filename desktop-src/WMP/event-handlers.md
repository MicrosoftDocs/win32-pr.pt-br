---
title: Manipuladores de eventos
description: Manipuladores de eventos
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Capas do Windows Media Player, manipuladores de eventos no JScript
- capas, manipuladores de eventos em JScript
- eventos, JScript
- Arquivos JScript para capas, manipuladores de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761450"
---
# <a name="event-handlers"></a><span data-ttu-id="504e8-107">Manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="504e8-107">Event Handlers</span></span>

<span data-ttu-id="504e8-108">O Microsoft JScript é usado para processar eventos no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="504e8-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="504e8-109">Consulte [manipulação de eventos](handling-events.md) para obter mais informações sobre manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="504e8-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="504e8-110">Você pode ter mais de uma linha de código em um manipulador de eventos, mas deve-se ter cuidado para não exceder o comprimento da linha que o JScript permite.</span><span class="sxs-lookup"><span data-stu-id="504e8-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="504e8-111">Separe as linhas por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="504e8-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="504e8-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="504e8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="504e8-113">**Usando o JScript**</span><span class="sxs-lookup"><span data-stu-id="504e8-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




