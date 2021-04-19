---
description: A propriedade RelPath do objeto SWbemObjectPath contém o caminho relativo do caminho completo.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. RelPath (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756504"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="b23ca-103">Propriedade SWbemObjectPath. RelPath</span><span class="sxs-lookup"><span data-stu-id="b23ca-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="b23ca-104">A propriedade **RelPath** do objeto [**SWbemObjectPath**](swbemobjectpath.md) contém o caminho relativo do caminho completo.</span><span class="sxs-lookup"><span data-stu-id="b23ca-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="b23ca-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b23ca-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b23ca-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b23ca-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23ca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b23ca-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="b23ca-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b23ca-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="b23ca-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b23ca-109">Examples</span></span>

<span data-ttu-id="b23ca-110">O exemplo de código VBScript a seguir mostra a diferença entre os dados obtidos de [**SWbemObject \_ . Path**](swbemobject-path-.md) e **SWbemObjectPath. RelPath**.</span><span class="sxs-lookup"><span data-stu-id="b23ca-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="b23ca-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b23ca-111">Requirements</span></span>



| <span data-ttu-id="b23ca-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b23ca-112">Requirement</span></span> | <span data-ttu-id="b23ca-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b23ca-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b23ca-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b23ca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b23ca-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b23ca-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b23ca-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b23ca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b23ca-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b23ca-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b23ca-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b23ca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b23ca-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b23ca-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b23ca-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b23ca-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="b23ca-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b23ca-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b23ca-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b23ca-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b23ca-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b23ca-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b23ca-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="b23ca-124">CLSID</span></span><br/>                    | <span data-ttu-id="b23ca-125">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="b23ca-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="b23ca-126">IID</span><span class="sxs-lookup"><span data-stu-id="b23ca-126">IID</span></span><br/>                      | <span data-ttu-id="b23ca-127">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="b23ca-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




