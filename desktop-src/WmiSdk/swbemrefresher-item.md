---
description: O método SWbemRefresher. Item retorna o SWbemRefreshableItem especificado da coleção. SWbemRefreshableItem da coleção.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Método SWbemRefresher. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172478"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="43a70-103">Método SWbemRefresher. Item</span><span class="sxs-lookup"><span data-stu-id="43a70-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="43a70-104">O método **SWbemRefresher. Item** retorna o [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado da coleção.</span><span class="sxs-lookup"><span data-stu-id="43a70-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="43a70-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="43a70-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="43a70-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43a70-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="43a70-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a70-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a70-108">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="43a70-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="43a70-109">Valor de índice do item na coleção.</span><span class="sxs-lookup"><span data-stu-id="43a70-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a70-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43a70-110">Return value</span></span>

<span data-ttu-id="43a70-111">Se a chamada for bem-sucedida, o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado será retornado.</span><span class="sxs-lookup"><span data-stu-id="43a70-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43a70-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="43a70-112">Error codes</span></span>

<span data-ttu-id="43a70-113">Se o atualizador não tiver nenhum item com o índice especificado, **wbemErrNotFound** será gerado.</span><span class="sxs-lookup"><span data-stu-id="43a70-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a70-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a70-114">Requirements</span></span>



| <span data-ttu-id="43a70-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a70-115">Requirement</span></span> | <span data-ttu-id="43a70-116">Valor</span><span class="sxs-lookup"><span data-stu-id="43a70-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43a70-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a70-117">Minimum supported client</span></span><br/> | <span data-ttu-id="43a70-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43a70-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43a70-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a70-119">Minimum supported server</span></span><br/> | <span data-ttu-id="43a70-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43a70-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43a70-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43a70-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a70-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a70-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="43a70-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="43a70-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="43a70-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43a70-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43a70-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43a70-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a70-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a70-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="43a70-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="43a70-127">CLSID</span></span><br/>                    | <span data-ttu-id="43a70-128">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="43a70-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="43a70-129">IID</span><span class="sxs-lookup"><span data-stu-id="43a70-129">IID</span></span><br/>                      | <span data-ttu-id="43a70-130">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="43a70-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="43a70-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a70-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a70-132">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="43a70-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




