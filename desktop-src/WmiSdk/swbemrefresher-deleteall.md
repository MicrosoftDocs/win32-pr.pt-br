---
description: O método SWbemRefresher. DeleteAll remove todos os itens da coleção no objeto SWbemRefresher. Objeto SWbemRefresher.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Método SWbemRefresher. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105789381"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="dac4a-103">Método SWbemRefresher. DeleteAll</span><span class="sxs-lookup"><span data-stu-id="dac4a-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="dac4a-104">O método **SWbemRefresher. DeleteAll** remove todos os itens da coleção no objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="dac4a-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="dac4a-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dac4a-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dac4a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dac4a-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="dac4a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dac4a-107">Parameters</span></span>

<span data-ttu-id="dac4a-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dac4a-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dac4a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dac4a-109">Return value</span></span>

<span data-ttu-id="dac4a-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dac4a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac4a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dac4a-111">Remarks</span></span>

<span data-ttu-id="dac4a-112">O [**SWbemRefreshableItem**](swbemrefreshableitem.md) correspondente para cada item removido tem sua propriedade de [**atualização**](swbemrefreshableitem-refresher.md) definida como **NULL**, o que indica que ele não tem mais um atualizador pai.</span><span class="sxs-lookup"><span data-stu-id="dac4a-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac4a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac4a-113">Requirements</span></span>



| <span data-ttu-id="dac4a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac4a-114">Requirement</span></span> | <span data-ttu-id="dac4a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dac4a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dac4a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac4a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dac4a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dac4a-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dac4a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac4a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dac4a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dac4a-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dac4a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dac4a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac4a-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac4a-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dac4a-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dac4a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="dac4a-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dac4a-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dac4a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dac4a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dac4a-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac4a-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dac4a-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="dac4a-126">CLSID</span></span><br/>                    | <span data-ttu-id="dac4a-127">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="dac4a-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="dac4a-128">IID</span><span class="sxs-lookup"><span data-stu-id="dac4a-128">IID</span></span><br/>                      | <span data-ttu-id="dac4a-129">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="dac4a-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="dac4a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="dac4a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac4a-131">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="dac4a-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




