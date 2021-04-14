---
description: Um retorno de chamada que notifica o host de quais estágios de pipeline são usados pela chamada de desenho da solicitação assocaited.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback:: GetSupportedStages'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500321"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="e0085-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Método IPipeLineStagesCallback:: GetSupportedStages</span><span class="sxs-lookup"><span data-stu-id="e0085-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="e0085-104">Um retorno de chamada que notifica o host de quais estágios de pipeline são usados pela chamada de desenho da solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="e0085-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0085-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0085-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="e0085-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0085-106">Parameters</span></span>

<span data-ttu-id="e0085-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="e0085-107">*numColumns* </span></span>  
<span data-ttu-id="e0085-108">O número de estágios retornados.</span><span class="sxs-lookup"><span data-stu-id="e0085-108">The number of stages returned.</span></span>

<span data-ttu-id="e0085-109">*count0 \_ pStages* </span><span class="sxs-lookup"><span data-stu-id="e0085-109">*count0\_pStages* </span></span>  
<span data-ttu-id="e0085-110">Os estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0085-110">The pipeline stages.</span></span>

<span data-ttu-id="e0085-111">*swapChainWidth* </span><span class="sxs-lookup"><span data-stu-id="e0085-111">*swapChainWidth* </span></span>  
<span data-ttu-id="e0085-112">A largura da cadeia de permuta assocaited com a chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="e0085-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="e0085-113">Isso é usado ao solicitar imagens de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0085-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="e0085-114">*swapChainHeight* </span><span class="sxs-lookup"><span data-stu-id="e0085-114">*swapChainHeight* </span></span>  
<span data-ttu-id="e0085-115">A altura da cadeia de permuta assocaited com a chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="e0085-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="e0085-116">Isso é usado ao solicitar imagens de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0085-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0085-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0085-117">Return value</span></span>

<span data-ttu-id="e0085-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e0085-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0085-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0085-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0085-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0085-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e0085-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0085-121">Header</span></span></p></td><td><span data-ttu-id="e0085-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e0085-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e0085-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="e0085-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e0085-124">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="e0085-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
