---
title: Gerenciamento de esquema
description: O componente do provedor de exemplo ADSI define as classes de esquema \ 0034; Organizational Unit \ 0034; e \ 0034; Usuário \ 0034; e gerencia essas classes de esquema da seguinte maneira.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- ADSI de gerenciamento de esquema
- ADSI de gerenciamento de esquema
- Gerenciando esquemas ADSI
- esquemas, gerenciando ADSI
- Gerenciando um esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104567920"
---
# <a name="schema-management"></a><span data-ttu-id="c74bb-108">Gerenciamento de esquema</span><span class="sxs-lookup"><span data-stu-id="c74bb-108">Schema Management</span></span>

<span data-ttu-id="c74bb-109">O componente do provedor de exemplo ADSI define as classes de esquema "Organizational Unit" e "user" e gerencia essas classes de esquema da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c74bb-109">The ADSI example provider component defines the schema classes "Organizational Unit" and "User" and manages these schema classes in the following way.</span></span>

<span data-ttu-id="c74bb-110">A classe de esquema "Organizational Unit" é representada por um objeto de contêiner ADs e pode conter outras "unidades organizacionais" e "usuários".</span><span class="sxs-lookup"><span data-stu-id="c74bb-110">The "Organizational Unit" schema class is represented by an ADs container object and can contain other "Organizational Units" and "Users".</span></span> <span data-ttu-id="c74bb-111">O objeto contêiner dá suporte às interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="c74bb-111">The container object supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="c74bb-112">A classe de esquema "user" é representada por um objeto Active Directory genérico e não contém outros tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="c74bb-112">The "User" schema class is represented by a generic Active Directory object and does not contain other types of objects.</span></span> <span data-ttu-id="c74bb-113">No componente de provedor de exemplo, o objeto de usuário é implementado como um objeto de Active Directory genérico que dá suporte às interfaces **IUnknown**, **IDispatch** e **IADs**.</span><span class="sxs-lookup"><span data-stu-id="c74bb-113">In the example provider component, the User object is implemented as a generic Active Directory object that supports the interfaces **IUnknown**, **IDispatch**, and **IADs**.</span></span> <span data-ttu-id="c74bb-114">Lembre-se de que o objeto de usuário, nesse caso, não oferece suporte à interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="c74bb-114">Be aware that the User object, in this case, does not support the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span>

<span data-ttu-id="c74bb-115">O componente de provedor de exemplo também deve implementar o objeto de namespace ADs, que dá suporte às interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="c74bb-115">The example provider component must also implement the ADs namespace object, which supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span>

<span data-ttu-id="c74bb-116">A figura a seguir mostra os detalhes do esquema que representa as duas classes de esquema de componente de provedor de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c74bb-116">The following figure shows the details of the schema that represents the two example provider component schema classes.</span></span>

![esquema de componente do provedor de exemplo ADSI](images/dssmsch.png)

<span data-ttu-id="c74bb-118">Lembre-se de que, na figura anterior, a classe de esquema "Organizational Unit" define três propriedades: "Description", "headcounts" e "ID".</span><span class="sxs-lookup"><span data-stu-id="c74bb-118">Be aware that in the preceding figure the "Organizational Unit" schema class defines three properties: "Description," "Headcounts," and "ID."</span></span> <span data-ttu-id="c74bb-119">A classe de esquema "user" define quatro propriedades: "ID", "Name", "PhoneNumber" e "title".</span><span class="sxs-lookup"><span data-stu-id="c74bb-119">The "User" schema class defines four properties: "ID," "Name," "PhoneNumber," and "Title."</span></span> <span data-ttu-id="c74bb-120">A propriedade "ID" é compartilhada por ambas as classes de esquema.</span><span class="sxs-lookup"><span data-stu-id="c74bb-120">The "ID" property is shared by both schema classes.</span></span> <span data-ttu-id="c74bb-121">Cada propriedade é definida pelo objeto de sintaxe "String" ou "Integer".</span><span class="sxs-lookup"><span data-stu-id="c74bb-121">Each property is defined by either the "String" or the "Integer" syntax object.</span></span>

> [!Note]  
> <span data-ttu-id="c74bb-122">Os objetos de sintaxe não estão presentes na primeira versão do componente de provedor de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c74bb-122">Syntax objects are not present in the first release of the example provider component.</span></span> <span data-ttu-id="c74bb-123">No entanto, na maioria das implementações de esquema ADSI da Microsoft, os objetos de sintaxe são incluídos no objeto de contêiner de esquema, assim como os objetos de classe de esquema e propriedade.</span><span class="sxs-lookup"><span data-stu-id="c74bb-123">However, in most Microsoft ADSI schema implementations, the syntax objects are included in the schema container object, just as the schema class and property objects are.</span></span> <span data-ttu-id="c74bb-124">Por esse motivo, eles são mostrados aqui.</span><span class="sxs-lookup"><span data-stu-id="c74bb-124">For this reason, they are shown here.</span></span>

 

<span data-ttu-id="c74bb-125">Esse componente de provedor torna os dados de esquema acessíveis para o aplicativo cliente ADSI na forma de objetos de classe ADs, objetos de propriedade ADs e objetos de sintaxe ADs, tudo dentro de um objeto contêiner de classe de esquema, para que os dados de esquema possam ser recuperados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c74bb-125">This provider component makes schema data accessible to the ADSI client application in the form of ADs class objects, ADs property objects, and ADs syntax objects, all within a schema class container object, so that schema data can be retrieved at run time.</span></span>

<span data-ttu-id="c74bb-126">O ADsPaths para os objetos de contêiner de classe de esquema definidos para o componente de provedor de exemplo são "Sample://Seattle/schema" e "Sample://Toronto/schema".</span><span class="sxs-lookup"><span data-stu-id="c74bb-126">The ADsPaths for the schema class container objects defined for the example provider component are "Sample://Seattle/schema" and "Sample://Toronto/schema".</span></span> <span data-ttu-id="c74bb-127">Neste exemplo, o conteúdo dos esquemas é idêntico.</span><span class="sxs-lookup"><span data-stu-id="c74bb-127">In this example, the contents of the schemas are identical.</span></span>

 

 