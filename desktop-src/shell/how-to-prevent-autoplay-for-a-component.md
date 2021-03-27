---
description: Ilustra qual chave do registro deve ser definida para evitar a reprodução automática.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Como evitar a reprodução automática para um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967895"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="c89ee-103">Como evitar a reprodução automática para um componente</span><span class="sxs-lookup"><span data-stu-id="c89ee-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="c89ee-104">Ilustra qual chave do registro deve ser definida para evitar a reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="c89ee-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="c89ee-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="c89ee-105">Instructions</span></span>


<span data-ttu-id="c89ee-106">Para evitar que a reprodução automática seja iniciada em resposta a um evento, adicione o seguinte valor de **reg \_ sz** , conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="c89ee-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="c89ee-107">O valor é o identificador de classe (CLSID) que o componente que está gerando o evento é conhecido pelo na corrompidos (tabela de objetos em execução).</span><span class="sxs-lookup"><span data-stu-id="c89ee-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="c89ee-108">O valor não tem dados.</span><span class="sxs-lookup"><span data-stu-id="c89ee-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c89ee-109">Sob essa chave, os CLSIDs não são colocados entre chaves ( {} ).</span><span class="sxs-lookup"><span data-stu-id="c89ee-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



