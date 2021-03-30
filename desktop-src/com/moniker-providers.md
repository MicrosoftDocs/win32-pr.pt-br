---
title: Provedores de moniker
description: Provedores de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635852"
---
# <a name="moniker-providers"></a><span data-ttu-id="693dd-103">Provedores de moniker</span><span class="sxs-lookup"><span data-stu-id="693dd-103">Moniker Providers</span></span>

<span data-ttu-id="693dd-104">Em geral, um componente deve ser um provedor de moniker quando ele permite acesso a um de seus objetos, enquanto ainda controla o armazenamento do objeto.</span><span class="sxs-lookup"><span data-stu-id="693dd-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="693dd-105">Se um componente vai distribuir os identificadores de recurso que identificam seus objetos, ele deve ser capaz de executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="693dd-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="693dd-106">Quando solicitado, crie um moniker que identifique um objeto.</span><span class="sxs-lookup"><span data-stu-id="693dd-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="693dd-107">Habilite o moniker a ser associado quando um cliente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) .</span><span class="sxs-lookup"><span data-stu-id="693dd-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="693dd-108">Um provedor de moniker deve criar um moniker de uma *classe de moniker* apropriada para identificar um objeto.</span><span class="sxs-lookup"><span data-stu-id="693dd-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="693dd-109">A classe moniker refere-se a uma implementação específica da interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) que define o tipo de moniker criado.</span><span class="sxs-lookup"><span data-stu-id="693dd-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="693dd-110">Embora você possa implementar **IMoniker** para criar uma nova classe de moniker, ela é frequentemente desnecessária porque o OLE fornece implementações de várias classes de moniker diferentes, cada uma com seu próprio CLSID.</span><span class="sxs-lookup"><span data-stu-id="693dd-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="693dd-111">Consulte [implementações de moniker OLE](ole-moniker-implementations.md) para obter descrições das classes moniker que o OLE fornece.</span><span class="sxs-lookup"><span data-stu-id="693dd-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="693dd-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="693dd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="693dd-113">Clientes de moniker</span><span class="sxs-lookup"><span data-stu-id="693dd-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="693dd-114">Implementações de moniker OLE</span><span class="sxs-lookup"><span data-stu-id="693dd-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




