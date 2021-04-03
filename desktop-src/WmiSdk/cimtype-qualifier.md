---
description: O qualificador CIMType contém texto que descreve o tipo de uma propriedade.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Qualificador CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091788"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="e80dc-103">Qualificador CIMType</span><span class="sxs-lookup"><span data-stu-id="e80dc-103">CIMType Qualifier</span></span>

<span data-ttu-id="e80dc-104">O qualificador **CIMType** contém texto que descreve o tipo de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="e80dc-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="e80dc-105">Esse texto pode ser o tipo MOF, como "String" e "sint32" ou o tipo CIM, como " \_ cadeia de caracteres CIM" e "CIM \_ sint32".</span><span class="sxs-lookup"><span data-stu-id="e80dc-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="e80dc-106">Há uma correspondência um-para-um entre o qualificador **CIMType** e o tipo da propriedade usada no parâmetro *PvtType* do método [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="e80dc-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="e80dc-107">As duas exceções são:</span><span class="sxs-lookup"><span data-stu-id="e80dc-107">The two exceptions are:</span></span>

-   <span data-ttu-id="e80dc-108">[*Propriedades de referência*](gloss-r.md), que têm a **\_ referência** de tipo CIM, que contém o valor "Ref: ClassName".</span><span class="sxs-lookup"><span data-stu-id="e80dc-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="e80dc-109">O valor de ClassName descreve o tipo de classe da propriedade de referência.</span><span class="sxs-lookup"><span data-stu-id="e80dc-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="e80dc-110">Propriedades de objeto inserido, que têm o tipo de **\_ objeto CIM** .</span><span class="sxs-lookup"><span data-stu-id="e80dc-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="e80dc-111">Observe, no entanto, que o qualificador **CIMType** pode e deve ser usado para digitar uma propriedade de referência com mais precisão.</span><span class="sxs-lookup"><span data-stu-id="e80dc-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="e80dc-112">Por exemplo, se a propriedade sempre se referir a instâncias da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , seu qualificador **CIMType** deverá ser definido como:</span><span class="sxs-lookup"><span data-stu-id="e80dc-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="e80dc-113">Por padrão, o qualificador **CIMType** de uma propriedade de referência tem o tipo **ref**.</span><span class="sxs-lookup"><span data-stu-id="e80dc-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="e80dc-114">Assim como nas propriedades de referência, o qualificador **CIMType** deve ser usado para digitar uma propriedade de objeto inserido mais exatamente com a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="e80dc-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="e80dc-115">Como o WMI permite mais tipos do que podem ser expressos por constantes padrão com o \_ prefixo VT, o qualificador **CIMType** pode ajudar a interpretar valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="e80dc-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="e80dc-116">O qualificador **CIMType** é adicionado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e80dc-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="e80dc-117">Para obter mais informações, consulte [MOF Data Types](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="e80dc-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e80dc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80dc-118">Requirements</span></span>



| <span data-ttu-id="e80dc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80dc-119">Requirement</span></span> | <span data-ttu-id="e80dc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e80dc-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e80dc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e80dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e80dc-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e80dc-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e80dc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e80dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e80dc-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e80dc-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e80dc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e80dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80dc-126">**Qualificadores WMI padrão**</span><span class="sxs-lookup"><span data-stu-id="e80dc-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="e80dc-127">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="e80dc-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="e80dc-128">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="e80dc-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

