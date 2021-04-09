---
description: Um retorno de chamada que notifica o host das informações de framebuffer retornadas pela solicitação associada.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameBufferCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087638"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="0ad68-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Método IFrameBufferCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="0ad68-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="0ad68-104">Um retorno de chamada que notifica o host das informações de framebuffer retornadas pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="0ad68-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ad68-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="0ad68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad68-106">Parameters</span></span>

<span data-ttu-id="0ad68-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="0ad68-107">*frameNumber* </span></span>  
<span data-ttu-id="0ad68-108">O número do quadro.</span><span class="sxs-lookup"><span data-stu-id="0ad68-108">The frame number.</span></span>

<span data-ttu-id="0ad68-109">*Largura* </span><span class="sxs-lookup"><span data-stu-id="0ad68-109">*width* </span></span>  
<span data-ttu-id="0ad68-110">A largura do quadro.</span><span class="sxs-lookup"><span data-stu-id="0ad68-110">The width of the frame.</span></span>

<span data-ttu-id="0ad68-111">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="0ad68-111">*height* </span></span>  
<span data-ttu-id="0ad68-112">A altura do quadro.</span><span class="sxs-lookup"><span data-stu-id="0ad68-112">The height of the frame.</span></span>

<span data-ttu-id="0ad68-113">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="0ad68-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="0ad68-114">O destino de renderização do qual os resultados são provenientes.</span><span class="sxs-lookup"><span data-stu-id="0ad68-114">The render target that the results come from.</span></span> <span data-ttu-id="0ad68-115">É sempre um slot especificado pela solicitação de buffer de quadro ou, se não for uma chamada de desenho, então o primeiro RTV Bount à fonte de saída.</span><span class="sxs-lookup"><span data-stu-id="0ad68-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="0ad68-116">*frameDuraction* </span><span class="sxs-lookup"><span data-stu-id="0ad68-116">*frameDuraction* </span></span>  
<span data-ttu-id="0ad68-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="0ad68-117">Not used.</span></span>

<span data-ttu-id="0ad68-118">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="0ad68-118">*size* </span></span>  
<span data-ttu-id="0ad68-119">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="0ad68-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="0ad68-120">*\_buffer count5* </span><span class="sxs-lookup"><span data-stu-id="0ad68-120">*count5\_buffer* </span></span>  
<span data-ttu-id="0ad68-121">O conteúdo do destino de renderização no \_ formato R8G8B8A8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="0ad68-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ad68-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ad68-122">Return value</span></span>

<span data-ttu-id="0ad68-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0ad68-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ad68-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ad68-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad68-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ad68-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0ad68-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ad68-126">Header</span></span></p></td><td><span data-ttu-id="0ad68-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0ad68-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0ad68-128"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="0ad68-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0ad68-129">**IFrameBufferCallback**</span><span class="sxs-lookup"><span data-stu-id="0ad68-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
