---
title: Controle de acesso e criação de objeto
description: O servidor de Active Directory falhará ao criar um objeto filho se o chamador não tiver o \_ direito de \_ ADS \_ Create \_ filho para esse tipo de objeto no contêiner pai.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Controle de acesso e AD de criação de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084423"
---
# <a name="access-control-and-object-creation"></a><span data-ttu-id="5d851-104">Controle de acesso e criação de objeto</span><span class="sxs-lookup"><span data-stu-id="5d851-104">Access Control and Object Creation</span></span>

<span data-ttu-id="5d851-105">O servidor de Active Directory falhará ao criar um objeto filho se o chamador não tiver o **direito de ADS \_ \_ \_ Create \_ filho** para esse tipo de objeto no contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="5d851-105">The Active Directory server will fail to create a child object if the caller does not have the **ADS\_RIGHT\_DS\_CREATE\_CHILD** for that object type on the parent container.</span></span> <span data-ttu-id="5d851-106">Para determinar os tipos de objetos filho que o chamador pode criar em um objeto de diretório, leia o atributo **allowedChildClassesEffective** do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d851-106">To determine the types of child objects that the caller can create in a directory object, read the object's **allowedChildClassesEffective** attribute.</span></span>

<span data-ttu-id="5d851-107">Quando você usa o método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para criar um objeto filho, o objeto não é tornado persistente até [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ser chamado no novo objeto.</span><span class="sxs-lookup"><span data-stu-id="5d851-107">When you use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) method to create a child object, the object is not made persistent until [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) is called on the new object.</span></span> <span data-ttu-id="5d851-108">Entre as chamadas **Create** e **setinfo** , o thread de criação pode colocar valores em qualquer uma das propriedades do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="5d851-108">Between the **Create** and **SetInfo** calls, the creating thread can put values into any of the new object's properties.</span></span> <span data-ttu-id="5d851-109">Após a chamada **setinfo** , o thread de criação não necessariamente tem os direitos de acesso para definir as propriedades do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="5d851-109">After the **SetInfo** call, the creating thread does not necessarily have the access rights to set the new object's properties.</span></span> <span data-ttu-id="5d851-110">Para garantir que o chamador tenha esses direitos, especifique um descritor de segurança explícito durante a criação.</span><span class="sxs-lookup"><span data-stu-id="5d851-110">To ensure that the caller has these rights, specify an explicit security descriptor during creation.</span></span> <span data-ttu-id="5d851-111">A DACL deve ter uma ACE que concede ao chamador os direitos de acesso necessários no objeto.</span><span class="sxs-lookup"><span data-stu-id="5d851-111">The DACL should have an ACE that gives the caller the necessary access rights on the object.</span></span>

<span data-ttu-id="5d851-112">Para obter mais informações sobre o controle de acesso e a criação de objetos, consulte [como descritores de segurança são definidos em novos objetos de diretório](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5d851-112">For more information about access control and object creation, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span>

 

 