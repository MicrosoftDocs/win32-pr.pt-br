---
title: Propriedades e atributos ADSI
description: Os atributos são, às vezes, chamados de propriedades. Isso pode causar confusão. Esta documentação usa as definições a seguir para propriedades e atributos.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- ADSI de propriedades e atributos ADSI
- ADSI ADSI, usando, acessando e manipulando dados, propriedades e atributos
- ADSI de propriedades
- ADSI de atributos
- Propriedades ADSI, definidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750341"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="5db09-110">Propriedades e atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="5db09-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="5db09-111">Os atributos são, às vezes, chamados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5db09-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="5db09-112">Isso pode causar confusão.</span><span class="sxs-lookup"><span data-stu-id="5db09-112">This can cause confusion.</span></span> <span data-ttu-id="5db09-113">Esta documentação usa as definições a seguir para propriedades e atributos.</span><span class="sxs-lookup"><span data-stu-id="5db09-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="5db09-114">As propriedades são valores nomeados associados a um objeto de programação.</span><span class="sxs-lookup"><span data-stu-id="5db09-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="5db09-115">Por exemplo, a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expõe propriedades como [**Class**](iads-property-methods.md) e **Name**.</span><span class="sxs-lookup"><span data-stu-id="5db09-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="5db09-116">Os atributos são os dados associados a objetos em um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="5db09-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="5db09-117">Por exemplo, um objeto de usuário terá um atributo chamado **CN** , que contém uma cadeia de caracteres que é o nome distinto comum ou relativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="5db09-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="5db09-118">Os atributos são acessíveis por meio de métodos de interface ADSI, como [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="5db09-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="5db09-119">Para obter mais informações sobre propriedades e atributos ADSI, consulte:</span><span class="sxs-lookup"><span data-stu-id="5db09-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="5db09-120">O cache de atributo ADSI</span><span class="sxs-lookup"><span data-stu-id="5db09-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="5db09-121">Atributos únicos versus múltiplos valores</span><span class="sxs-lookup"><span data-stu-id="5db09-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="5db09-122">Active Directory atributos operacionais</span><span class="sxs-lookup"><span data-stu-id="5db09-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




