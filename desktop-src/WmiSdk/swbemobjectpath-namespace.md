---
description: A propriedade namespace do objeto SWbemObjectPath contém o nome do namespace que faz parte do caminho do objeto.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. Namespace (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170005"
---
# <a name="swbemobjectpathnamespace-property"></a><span data-ttu-id="3b2b4-103">Propriedade SWbemObjectPath. namespace</span><span class="sxs-lookup"><span data-stu-id="3b2b4-103">SWbemObjectPath.Namespace property</span></span>

<span data-ttu-id="3b2b4-104">A propriedade **namespace** do objeto [**SWbemObjectPath**](swbemobjectpath.md) contém o nome do namespace que faz parte do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3b2b4-104">The **Namespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the namespace that is part of the object path.</span></span> <span data-ttu-id="3b2b4-105">Por exemplo, o caminho a seguir mostra a propriedade namespace que retorna a \\ cimv2 raiz:</span><span class="sxs-lookup"><span data-stu-id="3b2b4-105">For example, the following path shows the namespace property that returns root\\cimv2:</span></span>

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

<span data-ttu-id="3b2b4-106">Para obter a explicação da sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3b2b4-106">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3b2b4-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3b2b4-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b2b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b2b4-108">Syntax</span></span>


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a><span data-ttu-id="3b2b4-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3b2b4-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3b2b4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b2b4-110">Examples</span></span>

<span data-ttu-id="3b2b4-111">O exemplo a seguir mostra como obter o nome do namespace de instâncias do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que são discos rígidos.</span><span class="sxs-lookup"><span data-stu-id="3b2b4-111">The following example shows you how to obtain the namespace name from instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) that are hard disks.</span></span> <span data-ttu-id="3b2b4-112">O script se conecta ao namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="3b2b4-112">The script connects to the default namespace.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a><span data-ttu-id="3b2b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b2b4-113">Requirements</span></span>



| <span data-ttu-id="3b2b4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b2b4-114">Requirement</span></span> | <span data-ttu-id="3b2b4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3b2b4-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2b4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b2b4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2b4-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b2b4-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b2b4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b2b4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2b4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b2b4-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b2b4-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b2b4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b2b4-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b2b4-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b2b4-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3b2b4-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b2b4-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3b2b4-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3b2b4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3b2b4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b2b4-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b2b4-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b2b4-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="3b2b4-126">CLSID</span></span><br/>                    | <span data-ttu-id="3b2b4-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="3b2b4-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="3b2b4-128">IID</span><span class="sxs-lookup"><span data-stu-id="3b2b4-128">IID</span></span><br/>                      | <span data-ttu-id="3b2b4-129">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="3b2b4-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

