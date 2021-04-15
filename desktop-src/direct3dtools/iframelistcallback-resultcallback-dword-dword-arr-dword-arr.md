---
description: Uma função de retorno de chamada usada para notificar o host sobre quais quadros foram capturados.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameListCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456860"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span data-ttu-id="8e254-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>Método IFrameListCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="8e254-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback::ResultCallback method</span></span>

<span data-ttu-id="8e254-104">Uma função de retorno de chamada usada para notificar o host sobre quais quadros foram capturados.</span><span class="sxs-lookup"><span data-stu-id="8e254-104">A callback function used to notify the host of which frames were captured.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e254-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e254-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a><span data-ttu-id="8e254-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e254-106">Parameters</span></span>

<span data-ttu-id="8e254-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="8e254-107">*numFrames* </span></span>  
<span data-ttu-id="8e254-108">O número de quadros capturados.</span><span class="sxs-lookup"><span data-stu-id="8e254-108">The number of frames captured.</span></span>

<span data-ttu-id="8e254-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="8e254-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="8e254-110">Os números de quadro dos quadros capturados.</span><span class="sxs-lookup"><span data-stu-id="8e254-110">The frame numbers of the captured frames.</span></span>

<span data-ttu-id="8e254-111">*count0 \_ frameEventIDs* </span><span class="sxs-lookup"><span data-stu-id="8e254-111">*count0\_frameEventIDs* </span></span>  
<span data-ttu-id="8e254-112">O evento final associado a cada quadro.</span><span class="sxs-lookup"><span data-stu-id="8e254-112">The final event associated with each frame.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e254-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e254-113">Return value</span></span>

<span data-ttu-id="8e254-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e254-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e254-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e254-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e254-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e254-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e254-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e254-117">Header</span></span></p></td><td><span data-ttu-id="8e254-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8e254-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8e254-119"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="8e254-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8e254-120">**IFrameListCallback**</span><span class="sxs-lookup"><span data-stu-id="8e254-120">**IFrameListCallback**</span></span>](/windows/desktop/direct3dtools/iframelistcallback)

 

 
