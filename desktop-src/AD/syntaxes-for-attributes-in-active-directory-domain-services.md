---
title: Sintaxes para atributos em Active Directory Domain Services
description: Active Directory Domain Services definir um conjunto de sintaxes de atributo para especificar o tipo de dados contidos em um atributo.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Sintaxes para atributos de Active Directory Domain Services Active Directory
- Atributos Active Directory, sintaxes para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084430"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a><span data-ttu-id="0923e-105">Sintaxes para atributos em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="0923e-105">Syntaxes for Attributes in Active Directory Domain Services</span></span>

<span data-ttu-id="0923e-106">Active Directory Domain Services definir um conjunto de sintaxes de atributo para especificar o tipo de dados contidos em um atributo.</span><span class="sxs-lookup"><span data-stu-id="0923e-106">Active Directory Domain Services define a set of attribute syntaxes for specifying the type of data contained by an attribute.</span></span> <span data-ttu-id="0923e-107">As sintaxes predefinidas não aparecem na verdade no diretório, e você não pode adicionar novas sintaxes.</span><span class="sxs-lookup"><span data-stu-id="0923e-107">The predefined syntaxes do not actually appear in the directory, and you cannot add new syntaxes.</span></span> <span data-ttu-id="0923e-108">Vários métodos podem ser usados para identificar a sintaxe de uma classe de atributo:</span><span class="sxs-lookup"><span data-stu-id="0923e-108">Several methods can be used to identify the syntax of an attribute class:</span></span>

-   <span data-ttu-id="0923e-109">Os métodos [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs. GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put)e [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) usam a estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) para obter e definir os valores dos atributos de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0923e-109">The [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs.GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put), and [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) methods use the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure to get and set the values of an object's attributes.</span></span> <span data-ttu-id="0923e-110">O membro **VT** dessa estrutura é um valor **VarType** que identifica o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0923e-110">The **vt** member of this structure is a **VARTYPE** value that identifies the data type.</span></span>
-   <span data-ttu-id="0923e-111">Os métodos das interfaces [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usam um valor da enumeração [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) para especificar o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0923e-111">The methods of the [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interfaces use a value from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration to specify the data type.</span></span>
-   <span data-ttu-id="0923e-112">Para especificar a sintaxe de uma nova classe de atributo, defina os atributos [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) e [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) de um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) .</span><span class="sxs-lookup"><span data-stu-id="0923e-112">To specify the syntax of a new attribute class, set the [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) and [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) attributes of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object.</span></span> <span data-ttu-id="0923e-113">Se o valor de **oMSyntax** for 127, você também deverá definir o atributo [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) .</span><span class="sxs-lookup"><span data-stu-id="0923e-113">If the value of **oMSyntax** is 127, you must also set the [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) attribute.</span></span> <span data-ttu-id="0923e-114">Para obter mais informações, consulte [escolhendo uma sintaxe](choosing-a-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="0923e-114">For more information, see [Choosing a Syntax](choosing-a-syntax.md).</span></span>

<span data-ttu-id="0923e-115">Para obter uma lista completa das sintaxes fornecidas pelo Active Directory Domain Services, incluindo o valor de **VarType** e [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) correspondente de cada sintaxe, consulte [sintaxes](/windows/desktop/ADSchema/syntaxes).</span><span class="sxs-lookup"><span data-stu-id="0923e-115">For a complete list of the syntaxes provided by Active Directory Domain Services, including each syntax's corresponding **VARTYPE** and [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value, see [Syntaxes](/windows/desktop/ADSchema/syntaxes).</span></span>

 

 