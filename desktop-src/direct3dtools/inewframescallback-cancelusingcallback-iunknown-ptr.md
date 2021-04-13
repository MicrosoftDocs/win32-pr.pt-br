---
description: Um retorno de chamada que notifica o host de uma solicitação cancelada.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método INewFramesCallback:: CancelUsingCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 863219cd37078fbde1e7ef8b2da7677a31e12872
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456858"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span data-ttu-id="1651e-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>Método INewFramesCallback:: CancelUsingCallback</span><span class="sxs-lookup"><span data-stu-id="1651e-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback method</span></span>

<span data-ttu-id="1651e-104">Um retorno de chamada que notifica o host de uma solicitação cancelada.</span><span class="sxs-lookup"><span data-stu-id="1651e-104">A callback that notifies the host of a canceled request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1651e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1651e-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="1651e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1651e-106">Parameters</span></span>

<span data-ttu-id="1651e-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1651e-107">*requestCallback* </span></span>  
<span data-ttu-id="1651e-108">O endereço da solicitação cancelada.</span><span class="sxs-lookup"><span data-stu-id="1651e-108">The address of the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="1651e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1651e-109">Return value</span></span>

<span data-ttu-id="1651e-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1651e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1651e-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1651e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1651e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1651e-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1651e-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1651e-113">Header</span></span></p></td><td><span data-ttu-id="1651e-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1651e-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1651e-115"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="1651e-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1651e-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="1651e-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
