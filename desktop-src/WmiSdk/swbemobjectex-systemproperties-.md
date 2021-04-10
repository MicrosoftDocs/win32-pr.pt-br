---
description: Retorna um objeto SWbemPropertySet que contém a coleção de propriedades do sistema WMI que se aplicam ao objeto.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: Propriedade de temProperties_ de SWbemObjectEx.Sys(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171656"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="371a3-103">SWbemObjectEx.Sys\_ Propriedade temProperties</span><span class="sxs-lookup"><span data-stu-id="371a3-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="371a3-104">A **Propriedade SystemProperties \_** do objeto [**SWbemObjectEx**](swbemobjectex.md) retorna um objeto [**SWbemPropertySet**](swbempropertyset.md) que contém a coleção de propriedades do [sistema WMI](wmi-system-properties.md) que se aplicam ao objeto.</span><span class="sxs-lookup"><span data-stu-id="371a3-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="371a3-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="371a3-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="371a3-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="371a3-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="371a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="371a3-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="371a3-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="371a3-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="371a3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="371a3-109">Examples</span></span>

<span data-ttu-id="371a3-110">O exemplo de código a seguir recupera os valores de propriedade para a classe de processo do Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="371a3-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="371a3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="371a3-111">Requirements</span></span>



| <span data-ttu-id="371a3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="371a3-112">Requirement</span></span> | <span data-ttu-id="371a3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="371a3-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="371a3-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="371a3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="371a3-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="371a3-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="371a3-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="371a3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="371a3-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="371a3-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="371a3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="371a3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="371a3-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="371a3-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="371a3-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="371a3-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="371a3-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="371a3-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="371a3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="371a3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="371a3-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="371a3-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="371a3-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="371a3-124">CLSID</span></span><br/>                    | <span data-ttu-id="371a3-125">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="371a3-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="371a3-126">IID</span><span class="sxs-lookup"><span data-stu-id="371a3-126">IID</span></span><br/>                      | <span data-ttu-id="371a3-127">ISWbemObjectEx de IID \_</span><span class="sxs-lookup"><span data-stu-id="371a3-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="371a3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="371a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371a3-129">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="371a3-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




