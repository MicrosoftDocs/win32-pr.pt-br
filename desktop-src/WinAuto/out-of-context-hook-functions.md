---
title: Funções de gancho fora do contexto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Saiba mais sobre: funções de gancho fora de contexto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829407"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="bf8a1-103">Funções de gancho fora do contexto</span><span class="sxs-lookup"><span data-stu-id="bf8a1-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="bf8a1-104">A lista a seguir descreve os principais aspectos das funções de gancho fora do contexto:</span><span class="sxs-lookup"><span data-stu-id="bf8a1-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="bf8a1-105">As funções de gancho fora do contexto estão localizadas no espaço de endereço do cliente, seja no corpo do código ou em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="bf8a1-106">Funções de gancho fora de contexto não são mapeadas para o espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="bf8a1-107">Quando um evento é disparado, os parâmetros da função Hook são empacotados entre limites de processo.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="bf8a1-108">Funções de gancho fora do contexto são visivelmente mais lentas do que as funções de gancho no contexto devido ao marshaling.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="bf8a1-109">O sistema enfileira as notificações de eventos para que elas cheguem de forma assíncrona (devido ao tempo necessário para realizar o marshaling).</span><span class="sxs-lookup"><span data-stu-id="bf8a1-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="bf8a1-110">Embora as notificações de eventos sejam assíncronas, a Microsoft Acessibilidade Ativa garante que a função de retorno de chamada receba todos os eventos na ordem em que são gerados.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="bf8a1-111">O componente de usuário do sistema operacional aloca memória para eventos que são manipulados por funções de gancho fora do contexto.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="bf8a1-112">A memória é liberada quando as funções de gancho retornam.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="bf8a1-113">Se uma função de Hook não processar eventos com rapidez suficiente, os recursos do usuário serão reduzidos, eventualmente resultando em uma falha ou tempos de resposta extremamente lentos.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="bf8a1-114">Esses problemas podem ocorrer se:</span><span class="sxs-lookup"><span data-stu-id="bf8a1-114">These problems may occur if:</span></span>

-   <span data-ttu-id="bf8a1-115">Os eventos são acionados muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="bf8a1-116">O sistema está lento.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-116">The system is slow.</span></span>
-   <span data-ttu-id="bf8a1-117">A função Hook processa eventos lentamente.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="bf8a1-118">O cliente está sendo executado no Windows 9x.</span><span class="sxs-lookup"><span data-stu-id="bf8a1-118">The client is running on Windows 9x.</span></span>

 

 




