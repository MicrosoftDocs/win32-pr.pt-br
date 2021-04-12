---
title: Inicializando objetos persistentes
description: Inicializando objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366755"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="65068-103">Inicializando objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="65068-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="65068-104">Várias das interfaces de objeto persistente, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), permitem que os clientes inicializem objetos para um estado "novo" ou "padrão".</span><span class="sxs-lookup"><span data-stu-id="65068-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="65068-105">Esse estado inicial é diferente do de um objeto recém-criado, que não tem estado.</span><span class="sxs-lookup"><span data-stu-id="65068-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="65068-106">Inicializar o estado de um objeto, mesmo para o estado padrão, pode ser uma operação de computação intensiva ou com uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65068-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="65068-107">Ao separar a criação da inicialização, a inicialização pode ser executada somente quando é realmente necessária e os clientes podem evitar a inicialização de objetos para o estado padrão somente para carregar imediatamente os dados armazenados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="65068-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65068-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65068-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65068-109">Interfaces de objeto persistentes</span><span class="sxs-lookup"><span data-stu-id="65068-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 