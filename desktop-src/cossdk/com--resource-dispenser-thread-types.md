---
description: Tipos de thread do dispensador de recursos COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipos de thread do dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370395"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="b4fb0-103">Tipos de thread do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="b4fb0-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="b4fb0-104">Chamadas em um dispensador de recursos COM+ podem se originar em um dos seguintes tipos de thread:</span><span class="sxs-lookup"><span data-stu-id="b4fb0-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="b4fb0-105">Thread apartment (STA)</span><span class="sxs-lookup"><span data-stu-id="b4fb0-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="b4fb0-106">Thread gratuito (MTA)</span><span class="sxs-lookup"><span data-stu-id="b4fb0-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="b4fb0-107">Thread não COM (aplicativo ou o thread do coletor de lixo do [Gerenciador do dispensador](com--dispenser-manager.md) )</span><span class="sxs-lookup"><span data-stu-id="b4fb0-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="b4fb0-108">Se um dispensador de recurso não for um objeto COM, ele deverá ser capaz de lidar com chamadas que chegam de qualquer thread a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="b4fb0-109">Se um dispensador de recurso for um objeto COM, o objeto COM deverá ser registrado com um modelo de threading de **ambos**.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="b4fb0-110">Isso permite que threads STA ou MTA criem e usem o dispensador de recurso sem uma opção de thread.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="b4fb0-111">Se um dispensador de recurso criar e usar outro objeto COM (por exemplo, um Gerenciador de recursos fora de processo), o dispensador de recursos poderá precisar manter vários proxies para esse outro objeto COM e garantir que as chamadas para o objeto sejam feitas usando o proxy apropriado para o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="b4fb0-112">Quando o dispensador de recurso cria esse objeto, ele realiza marshaling e salva a referência.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="b4fb0-113">Antes de chamar o objeto novamente, ele deve ser desempacotado para criar um proxy para o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="b4fb0-114">Pode ser mais eficiente armazenar em cache esses proxies por thread, mantendo um mapa da ID do thread para um ponteiro de proxy.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="b4fb0-115">Esse mapa se expande conforme novos threads são usados no processo.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4fb0-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4fb0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4fb0-117">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="b4fb0-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



