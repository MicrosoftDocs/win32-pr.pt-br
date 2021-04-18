---
description: A propriedade Qualifiers \_ do objeto SWbemObject retorna um objeto SWbemQualifierSet que é uma coleção de qualificadores para a classe ou instância atual. Esta propriedade é somente para leitura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Qualifiers_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766476"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="553c6-104">Propriedade SWbemObject. Qualifiers \_</span><span class="sxs-lookup"><span data-stu-id="553c6-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="553c6-105">A propriedade **Qualifiers \_** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que é uma coleção de qualificadores para a classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="553c6-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="553c6-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="553c6-106">This property is read-only.</span></span>

<span data-ttu-id="553c6-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="553c6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="553c6-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="553c6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="553c6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="553c6-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="553c6-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="553c6-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="553c6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="553c6-111">Examples</span></span>

<span data-ttu-id="553c6-112">A [lista todos os qualificadores para um](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) exemplo de código VBScript da classe WMI na galeria do TechNet usa a \_ Propriedade Qualifier para listar os qualificadores de classe para uma classe WMI especificada.</span><span class="sxs-lookup"><span data-stu-id="553c6-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="553c6-113">A amostra de código [listar todas as classes abstratas no WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript na galeria do TechNet lista todas as classes abstratas WMI definidas no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="553c6-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="553c6-114">A amostra de código [listar todas as classes dinâmicas no WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript usa a \_ Propriedade Qualifier para listar todas as classes dinâmicas WMI (incluindo classes de associação) definidas no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="553c6-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="553c6-115">O exemplo de código do [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell na galeria do TechNet lista todas as propriedades graváveis no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="553c6-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="553c6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="553c6-116">Requirements</span></span>



| <span data-ttu-id="553c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="553c6-117">Requirement</span></span> | <span data-ttu-id="553c6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="553c6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="553c6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="553c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="553c6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="553c6-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="553c6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="553c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="553c6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="553c6-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="553c6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="553c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="553c6-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="553c6-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="553c6-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="553c6-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="553c6-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="553c6-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="553c6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="553c6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="553c6-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="553c6-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="553c6-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="553c6-129">CLSID</span></span><br/>                    | <span data-ttu-id="553c6-130">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="553c6-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="553c6-131">IID</span><span class="sxs-lookup"><span data-stu-id="553c6-131">IID</span></span><br/>                      | <span data-ttu-id="553c6-132">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="553c6-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




