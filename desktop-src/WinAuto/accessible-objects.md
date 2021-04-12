---
title: Objetos acessíveis
description: Com o Microsoft Acessibilidade Ativa, os elementos da interface do usuário são expostos aos clientes como objetos COM (Component Object Model).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364416"
---
# <a name="accessible-objects"></a><span data-ttu-id="6a9bb-103">Objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="6a9bb-103">Accessible Objects</span></span>

<span data-ttu-id="6a9bb-104">Com o Microsoft Acessibilidade Ativa, os elementos da interface do usuário são expostos aos clientes como objetos COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="6a9bb-104">With Microsoft Active Accessibility, UI elements are exposed to clients as Component Object Model (COM) objects.</span></span> <span data-ttu-id="6a9bb-105">Esses *objetos acessíveis* mantêm partes de informações, chamadas *Propriedades*, que descrevem o nome do objeto, o local da tela e outras informações necessárias aos auxílios de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-105">These *accessible objects* maintain pieces of information, called *properties*, which describe the object's name, screen location, and other information needed by accessibility aids.</span></span> <span data-ttu-id="6a9bb-106">Os objetos acessíveis também fornecem *métodos* que os clientes chamam para fazer com que o objeto execute alguma ação.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-106">Accessible objects also provide *methods* that clients call to cause the object to perform some action.</span></span> <span data-ttu-id="6a9bb-107">Os objetos acessíveis que têm elementos simples associados a eles também são chamados de *pais* ou *contêineres*.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-107">Accessible objects that have simple elements associated with them are also called *parents*, or *containers*.</span></span>

<span data-ttu-id="6a9bb-108">Os objetos acessíveis são implementados usando a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) baseada em com do Microsoft acessibilidade ativa.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-108">Accessible objects are implemented using Microsoft Active Accessibility's COM-based [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="6a9bb-109">Os métodos e as propriedades **IAccessible** permitem que os aplicativos cliente obtenham informações sobre elementos de interface do usuário necessários para os usuários.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-109">The **IAccessible** methods and properties enable client applications to get information about UI elements needed by users.</span></span> <span data-ttu-id="6a9bb-110">Por exemplo, [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) retorna um ponteiro de interface para um pai de um objeto acessível e [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) fornece um meio para os clientes obterem informações sobre outros objetos em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="6a9bb-110">For example, [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) returns an interface pointer to an accessible object's parent, and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) provides a means for clients to get information about other objects within a container.</span></span>

<span data-ttu-id="6a9bb-111">Para obter mais informações sobre como os objetos acessíveis e os elementos simples estão relacionados, consulte [elementos simples](simple-elements.md).</span><span class="sxs-lookup"><span data-stu-id="6a9bb-111">For more information about how accessible objects and simple elements are related, see [Simple Elements](simple-elements.md).</span></span>

 

 




