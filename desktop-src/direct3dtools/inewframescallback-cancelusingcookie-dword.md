---
description: Um retorno de chamada que notifica o host de uma solicitação cancelada usando um cookie que identifica exclusivamente a solicitação.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método INewFramesCallback:: CancelUsingCookie'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456515"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="5009d-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>Método INewFramesCallback:: CancelUsingCookie</span><span class="sxs-lookup"><span data-stu-id="5009d-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="5009d-104">Um retorno de chamada que notifica o host de uma solicitação cancelada usando um cookie que identifica exclusivamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5009d-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="5009d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5009d-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="5009d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5009d-106">Parameters</span></span>

<span data-ttu-id="5009d-107">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="5009d-107">*requestCookie* </span></span>  
<span data-ttu-id="5009d-108">O cookie que idenfies exclusivamente a solicitação cancelada.</span><span class="sxs-lookup"><span data-stu-id="5009d-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="5009d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5009d-109">Return value</span></span>

<span data-ttu-id="5009d-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5009d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5009d-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5009d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5009d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5009d-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5009d-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5009d-113">Header</span></span></p></td><td><span data-ttu-id="5009d-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5009d-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5009d-115"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="5009d-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5009d-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="5009d-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
