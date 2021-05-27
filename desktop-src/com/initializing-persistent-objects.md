---
title: Inicializando objetos persistentes
description: Inicializando objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549192"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="1e5e7-103">Inicializando objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="1e5e7-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="1e5e7-104">Várias das interfaces de objeto persistente, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), permitem que os clientes inicializem objetos para um estado "novo" ou "padrão".</span><span class="sxs-lookup"><span data-stu-id="1e5e7-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="1e5e7-105">Esse estado inicial é diferente do de um objeto recém-criado, que não tem estado.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="1e5e7-106">Inicializar o estado de um objeto, mesmo para o estado padrão, pode ser uma operação de computação intensiva ou com uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="1e5e7-107">Ao separar a criação da inicialização, a inicialização pode ser executada somente quando é realmente necessária e os clientes podem evitar a inicialização de objetos para o estado padrão somente para carregar imediatamente os dados armazenados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e5e7-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e5e7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e5e7-109">Interfaces de objeto persistentes</span><span class="sxs-lookup"><span data-stu-id="1e5e7-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 