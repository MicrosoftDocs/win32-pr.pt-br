---
title: Monikers
description: Um moniker no COM não é apenas uma maneira de identificar um objeto \ 8212; um moniker também é implementado como um objeto.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004951"
---
# <a name="monikers"></a><span data-ttu-id="307a5-103">Monikers</span><span class="sxs-lookup"><span data-stu-id="307a5-103">Monikers</span></span>

<span data-ttu-id="307a5-104">Um moniker no COM não é apenas uma maneira de identificar um objeto — um moniker também é implementado como um objeto.</span><span class="sxs-lookup"><span data-stu-id="307a5-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="307a5-105">Esse objeto fornece serviços que permitem que um componente obtenha um ponteiro para o objeto identificado pelo moniker.</span><span class="sxs-lookup"><span data-stu-id="307a5-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="307a5-106">Esse processo é conhecido como *Associação*.</span><span class="sxs-lookup"><span data-stu-id="307a5-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="307a5-107">Os monikers são objetos que implementam a interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) e geralmente são implementados em DLLs como objetos de componente.</span><span class="sxs-lookup"><span data-stu-id="307a5-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="307a5-108">Há duas maneiras de exibir o uso de monikers: como um cliente moniker, um componente que usa um moniker para obter um ponteiro para outro objeto; e como um provedor de moniker, um componente que fornece monikers que identificam seus objetos para clientes de moniker.</span><span class="sxs-lookup"><span data-stu-id="307a5-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="307a5-109">O OLE usa monikers para se conectar e ativar objetos, estejam eles no mesmo computador ou em uma rede.</span><span class="sxs-lookup"><span data-stu-id="307a5-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="307a5-110">Um uso muito importante é para conexões de rede.</span><span class="sxs-lookup"><span data-stu-id="307a5-110">A very important use is for network connections.</span></span> <span data-ttu-id="307a5-111">Eles também são usados para identificar, conectar e executar objetos de link de documento OLE composto.</span><span class="sxs-lookup"><span data-stu-id="307a5-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="307a5-112">Nesse caso, a origem do link atua como o provedor do moniker e o contêiner que contém o objeto de link atua como o cliente do moniker.</span><span class="sxs-lookup"><span data-stu-id="307a5-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="307a5-113">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="307a5-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="307a5-114">Clientes de moniker</span><span class="sxs-lookup"><span data-stu-id="307a5-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="307a5-115">Provedores de moniker</span><span class="sxs-lookup"><span data-stu-id="307a5-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="307a5-116">Implementações de moniker OLE</span><span class="sxs-lookup"><span data-stu-id="307a5-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="307a5-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="307a5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="307a5-118">O Component Object Model</span><span class="sxs-lookup"><span data-stu-id="307a5-118">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




