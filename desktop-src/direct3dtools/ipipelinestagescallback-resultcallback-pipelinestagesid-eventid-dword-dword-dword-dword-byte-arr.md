---
description: Um retorno de chamada que notifica o host de fases de estágios de pipeline informações de imagem retornadas pela solicitação assocaited.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296058"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="474f4-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>Método IPipeLineStagesCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="474f4-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="474f4-104">Um retorno de chamada que notifica o host de fases de estágios de pipeline informações de imagem retornadas pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="474f4-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="474f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="474f4-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="474f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="474f4-106">Parameters</span></span>

<span data-ttu-id="474f4-107">*prepareid* </span><span class="sxs-lookup"><span data-stu-id="474f4-107">*stageId* </span></span>  
<span data-ttu-id="474f4-108">O estágio de pipeline representado nos resultados.</span><span class="sxs-lookup"><span data-stu-id="474f4-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="474f4-109">*Eid* </span><span class="sxs-lookup"><span data-stu-id="474f4-109">*eid* </span></span>  
<span data-ttu-id="474f4-110">O evento representado nos resultados.</span><span class="sxs-lookup"><span data-stu-id="474f4-110">The event represented in the results.</span></span>

<span data-ttu-id="474f4-111">*Largura* </span><span class="sxs-lookup"><span data-stu-id="474f4-111">*width* </span></span>  
<span data-ttu-id="474f4-112">A largura da imagem de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="474f4-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="474f4-113">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="474f4-113">*height* </span></span>  
<span data-ttu-id="474f4-114">A altura da imagem de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="474f4-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="474f4-115">*ao* </span><span class="sxs-lookup"><span data-stu-id="474f4-115">*format* </span></span>  
<span data-ttu-id="474f4-116">O formato da imagem de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="474f4-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="474f4-117">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="474f4-117">*size* </span></span>  
<span data-ttu-id="474f4-118">O tamanho da imagem em bytes.</span><span class="sxs-lookup"><span data-stu-id="474f4-118">The size of the image in bytes.</span></span>

<span data-ttu-id="474f4-119">*\_buffer count5* </span><span class="sxs-lookup"><span data-stu-id="474f4-119">*count5\_buffer* </span></span>  
<span data-ttu-id="474f4-120">A imagem de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="474f4-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="474f4-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="474f4-121">Return value</span></span>

<span data-ttu-id="474f4-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="474f4-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="474f4-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="474f4-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="474f4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="474f4-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="474f4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="474f4-125">Header</span></span></p></td><td><span data-ttu-id="474f4-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="474f4-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="474f4-127"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="474f4-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="474f4-128">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="474f4-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
