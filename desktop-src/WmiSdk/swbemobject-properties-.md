---
description: A \_ Propriedade Properties do objeto SWbemObject retorna um objeto SWbemPropertySet que é uma coleção das propriedades da classe ou instância atual. Esta propriedade é somente para leitura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Properties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773044"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="85c85-104">Propriedade SWbemObject. Properties \_</span><span class="sxs-lookup"><span data-stu-id="85c85-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="85c85-105">A **propriedade \_ Properties** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemPropertySet**](swbempropertyset.md) que é uma coleção das propriedades da classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="85c85-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="85c85-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="85c85-106">This property is read-only.</span></span>

<span data-ttu-id="85c85-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="85c85-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="85c85-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="85c85-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c85-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85c85-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="85c85-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="85c85-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="85c85-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="85c85-111">Examples</span></span>

<span data-ttu-id="85c85-112">O exemplo de código do PowerShell para [gerar scripts de classe WMI do PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) na galeria do TechNet usa a \_ Propriedade Properties para gerar um script para cada uma das classes WMI que listarão o nome da classe WMI e as propriedades.</span><span class="sxs-lookup"><span data-stu-id="85c85-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="85c85-113">O código a seguir, extraído da [lista todas as propriedades de um exemplo de](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) código VBScript da classe WMI na galeria do TechNet, lista as propriedades de uma classe WMI especificada.</span><span class="sxs-lookup"><span data-stu-id="85c85-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="85c85-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c85-114">Requirements</span></span>



| <span data-ttu-id="85c85-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c85-115">Requirement</span></span> | <span data-ttu-id="85c85-116">Valor</span><span class="sxs-lookup"><span data-stu-id="85c85-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85c85-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85c85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85c85-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85c85-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85c85-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85c85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85c85-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85c85-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85c85-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85c85-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c85-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c85-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="85c85-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="85c85-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="85c85-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="85c85-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="85c85-125">DLL</span><span class="sxs-lookup"><span data-stu-id="85c85-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85c85-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85c85-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="85c85-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="85c85-127">CLSID</span></span><br/>                    | <span data-ttu-id="85c85-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="85c85-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="85c85-129">IID</span><span class="sxs-lookup"><span data-stu-id="85c85-129">IID</span></span><br/>                      | <span data-ttu-id="85c85-130">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="85c85-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




