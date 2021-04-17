---
title: Elementos simples
description: Um elemento simples é um elemento de interface do usuário que compartilha um objeto IAccessible com outros elementos e se baseia nesse objeto IAccessible (normalmente seu pai) para expor suas propriedades.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811398"
---
# <a name="simple-elements"></a><span data-ttu-id="6db7d-103">Elementos simples</span><span class="sxs-lookup"><span data-stu-id="6db7d-103">Simple Elements</span></span>

<span data-ttu-id="6db7d-104">Um *elemento simples* é um elemento de interface do usuário que compartilha um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com outros elementos e se baseia nesse objeto **IAccessible** (normalmente seu pai) para expor suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6db7d-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="6db7d-105">Para diferenciar entre os elementos que compartilham um objeto **IAccessible** , o servidor atribui um identificador filho positivo exclusivo a cada elemento simples.</span><span class="sxs-lookup"><span data-stu-id="6db7d-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="6db7d-106">Essa atribuição é feita em uma base por instância de interface, portanto, as IDs devem ser exclusivas dentro desse contexto.</span><span class="sxs-lookup"><span data-stu-id="6db7d-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="6db7d-107">Muitas implementações atribuem essas IDs sequencialmente, começando com 1.</span><span class="sxs-lookup"><span data-stu-id="6db7d-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="6db7d-108">Esse esquema não permite que elementos simples tenham filhos próprios.</span><span class="sxs-lookup"><span data-stu-id="6db7d-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="6db7d-109">Elementos simples também são conhecidos como *filhos*.</span><span class="sxs-lookup"><span data-stu-id="6db7d-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="6db7d-110">Para ser identificado e exposto exclusivamente, um elemento simples requer um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e uma ID filho.</span><span class="sxs-lookup"><span data-stu-id="6db7d-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="6db7d-111">Portanto, ao se comunicar com um objeto **IAccessible** , os clientes devem fornecer a ID filho apropriada.</span><span class="sxs-lookup"><span data-stu-id="6db7d-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="6db7d-112">Um identificador especial, **childID \_** próprio, pode ser usado para fazer referência ao próprio objeto acessível, em vez de um de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="6db7d-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="6db7d-113">O objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) compartilhado entre elementos simples geralmente corresponde a um objeto pai comum na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6db7d-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="6db7d-114">Por exemplo, as caixas de listagem do sistema expõem um objeto acessível para a caixa de listagem geral e elementos simples para cada item da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6db7d-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="6db7d-115">Nesse caso, o objeto **IAccessible** da caixa de listagem também é o pai ou o contêiner dos itens da lista.</span><span class="sxs-lookup"><span data-stu-id="6db7d-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="6db7d-116">Para obter mais informações sobre objetos acessíveis, consulte [objetos acessíveis](accessible-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6db7d-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 




