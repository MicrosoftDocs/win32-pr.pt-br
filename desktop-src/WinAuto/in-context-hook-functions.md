---
title: Funções de In-Context Hook
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Saiba mais sobre: funções de In-Context Hook'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171981"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="008c7-103">Funções de In-Context Hook</span><span class="sxs-lookup"><span data-stu-id="008c7-103">In-Context Hook Functions</span></span>

<span data-ttu-id="008c7-104">A lista a seguir descreve os principais aspectos das funções de gancho no contexto:</span><span class="sxs-lookup"><span data-stu-id="008c7-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="008c7-105">As funções de ganchos no contexto devem estar localizadas em uma DLL (biblioteca de vínculo dinâmico) que o sistema mapeia para o espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="008c7-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="008c7-106">As funções de gancho no contexto compartilham o espaço de endereço com o servidor.</span><span class="sxs-lookup"><span data-stu-id="008c7-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="008c7-107">Quando o servidor dispara um evento, o sistema chama uma função de gancho sem realizar marshaling (empacotamento e envio de parâmetros de interface entre limites de processo).</span><span class="sxs-lookup"><span data-stu-id="008c7-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="008c7-108">As funções de gancho no contexto tendem a ser muito rápidas e recebem notificações de eventos de forma síncrona porque não há marshaling.</span><span class="sxs-lookup"><span data-stu-id="008c7-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="008c7-109">Alguns eventos podem ser fornecidos fora do processo, mesmo que você solicite que eles sejam entregues em processo (usando o \_ sinalizador de INCONTEXTO WINEVENT).</span><span class="sxs-lookup"><span data-stu-id="008c7-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="008c7-110">Você pode ver essa situação com problemas de interoperabilidade de aplicativos de 64 bits e 32 bits e com eventos do console do Windows.</span><span class="sxs-lookup"><span data-stu-id="008c7-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 




