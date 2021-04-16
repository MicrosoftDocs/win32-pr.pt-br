---
description: Um retorno de chamada que notifica o host do pipeline prepara as informações de malha retornadas pela solicitação assocaited.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback:: MeshDataVertCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500384"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="f1c99-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Método IPipeLineStagesCallback:: MeshDataVertCallback</span><span class="sxs-lookup"><span data-stu-id="f1c99-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="f1c99-104">Um retorno de chamada que notifica o host do pipeline prepara as informações de malha retornadas pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="f1c99-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c99-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1c99-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="f1c99-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1c99-106">Parameters</span></span>

<span data-ttu-id="f1c99-107">*numVertices* </span><span class="sxs-lookup"><span data-stu-id="f1c99-107">*numVertices* </span></span>  
<span data-ttu-id="f1c99-108">O número de vértices nos resultados.</span><span class="sxs-lookup"><span data-stu-id="f1c99-108">The number of vertices in the results.</span></span>

<span data-ttu-id="f1c99-109">*numBufferLayoutEntries* </span><span class="sxs-lookup"><span data-stu-id="f1c99-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="f1c99-110">O número de entradas de layout de buffer nos resultados.</span><span class="sxs-lookup"><span data-stu-id="f1c99-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="f1c99-111">*entradas de count1 \_* </span><span class="sxs-lookup"><span data-stu-id="f1c99-111">*count1\_entries* </span></span>  
<span data-ttu-id="f1c99-112">O layout do buffer é todo.</span><span class="sxs-lookup"><span data-stu-id="f1c99-112">The buffer layout entires.</span></span> <span data-ttu-id="f1c99-113">Elas descrevem a assinatura de saída do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f1c99-113">These describe the shader output signature.</span></span>

<span data-ttu-id="f1c99-114">*Stride* </span><span class="sxs-lookup"><span data-stu-id="f1c99-114">*stride* </span></span>  
<span data-ttu-id="f1c99-115">O tamanho (STRIDE) de uma parte de saída inteira.</span><span class="sxs-lookup"><span data-stu-id="f1c99-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="f1c99-116">*numVBBytes* </span><span class="sxs-lookup"><span data-stu-id="f1c99-116">*numVBBytes* </span></span>  
<span data-ttu-id="f1c99-117">O tamanho do buffer de vértice em bytes.</span><span class="sxs-lookup"><span data-stu-id="f1c99-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="f1c99-118">*count4 \_ pVBData* </span><span class="sxs-lookup"><span data-stu-id="f1c99-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="f1c99-119">O buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="f1c99-119">The vertex buffer.</span></span>

<span data-ttu-id="f1c99-120">*numIBBytes* </span><span class="sxs-lookup"><span data-stu-id="f1c99-120">*numIBBytes* </span></span>  
<span data-ttu-id="f1c99-121">O tamanho do buffer de índice em bytes.</span><span class="sxs-lookup"><span data-stu-id="f1c99-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="f1c99-122">*count6 \_ pIBData* </span><span class="sxs-lookup"><span data-stu-id="f1c99-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="f1c99-123">O buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="f1c99-123">The index buffer.</span></span>

<span data-ttu-id="f1c99-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="f1c99-124">*indexSize* </span></span>  
<span data-ttu-id="f1c99-125">O tamanho de cada índice em bytes.</span><span class="sxs-lookup"><span data-stu-id="f1c99-125">The size of each index in bytes.</span></span>

<span data-ttu-id="f1c99-126">*IBOffset* </span><span class="sxs-lookup"><span data-stu-id="f1c99-126">*IBOffset* </span></span>  
<span data-ttu-id="f1c99-127">Um deslocamento no buffer de índice que especifica onde os índices devem começar a ser usados.</span><span class="sxs-lookup"><span data-stu-id="f1c99-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="f1c99-128">*baseVertex* </span><span class="sxs-lookup"><span data-stu-id="f1c99-128">*baseVertex* </span></span>  
<span data-ttu-id="f1c99-129">Um deslocamento para o buffer de vértice que especifica onde os vértices devem começar a ser usados.</span><span class="sxs-lookup"><span data-stu-id="f1c99-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="f1c99-130">*minVertex*</span><span class="sxs-lookup"><span data-stu-id="f1c99-130">*minVertex*</span></span>   

<span data-ttu-id="f1c99-131">*IBIndexesVB* </span><span class="sxs-lookup"><span data-stu-id="f1c99-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="f1c99-132">verdadeiro quando o buffer de índice é usado; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="f1c99-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="f1c99-133">*numIndices* </span><span class="sxs-lookup"><span data-stu-id="f1c99-133">*numIndices* </span></span>  
<span data-ttu-id="f1c99-134">O número de índices usados.</span><span class="sxs-lookup"><span data-stu-id="f1c99-134">The number of indices used.</span></span>

<span data-ttu-id="f1c99-135">*visualização* </span><span class="sxs-lookup"><span data-stu-id="f1c99-135">*topology* </span></span>  
<span data-ttu-id="f1c99-136">O topolology do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f1c99-136">The topolology of the shader.</span></span> <span data-ttu-id="f1c99-137">Isso não é necessariamente o mesmo que a topologia da chamada Draw associada.</span><span class="sxs-lookup"><span data-stu-id="f1c99-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1c99-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1c99-138">Return value</span></span>

<span data-ttu-id="f1c99-139">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f1c99-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1c99-140">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1c99-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1c99-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c99-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f1c99-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1c99-142">Header</span></span></p></td><td><span data-ttu-id="f1c99-143">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f1c99-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f1c99-144"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="f1c99-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f1c99-145">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="f1c99-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
