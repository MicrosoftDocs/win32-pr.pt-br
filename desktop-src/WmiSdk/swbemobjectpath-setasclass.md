---
description: O método SetAsClass do objeto SWbemObjectPath força o caminho para endereçar uma classe WMI.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. SetAsClass (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798216"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="72776-103">Propriedade SWbemObjectPath. SetAsClass</span><span class="sxs-lookup"><span data-stu-id="72776-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="72776-104">O método **SetAsClass** do objeto [**SWbemObjectPath**](swbemobjectpath.md) força o caminho para endereçar uma classe WMI.</span><span class="sxs-lookup"><span data-stu-id="72776-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="72776-105">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="72776-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="72776-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72776-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="72776-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="72776-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="72776-108">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="72776-108">Error codes</span></span>

<span data-ttu-id="72776-109">Depois de obter ou definir a propriedade **SetAsClass** , o objeto **Err** poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="72776-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="72776-110">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="72776-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="72776-111">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="72776-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72776-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72776-112">Requirements</span></span>



| <span data-ttu-id="72776-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="72776-113">Requirement</span></span> | <span data-ttu-id="72776-114">Valor</span><span class="sxs-lookup"><span data-stu-id="72776-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72776-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72776-115">Minimum supported client</span></span><br/> | <span data-ttu-id="72776-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72776-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72776-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72776-117">Minimum supported server</span></span><br/> | <span data-ttu-id="72776-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72776-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72776-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72776-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="72776-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72776-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72776-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="72776-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="72776-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72776-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72776-123">DLL</span><span class="sxs-lookup"><span data-stu-id="72776-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72776-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72776-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72776-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="72776-125">CLSID</span></span><br/>                    | <span data-ttu-id="72776-126">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="72776-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="72776-127">IID</span><span class="sxs-lookup"><span data-stu-id="72776-127">IID</span></span><br/>                      | <span data-ttu-id="72776-128">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="72776-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




