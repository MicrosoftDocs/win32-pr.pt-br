---
description: Um retorno de chamada que notifica o host das informações de operação primitivas do histórico de pixel retornado pela solicitação associada.
MS-HAID: vspixengine.IPixelHistoryCallback2\_PrimitivesCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback2: método rimitivesCallback de:P'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2A67EC3B-72F2-4347-AD23-961CDE0D456F
api_name:
- IPixelHistoryCallback2.PrimitivesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8512bde1acd96ebbe132eeb91872d04ce043b44f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500627"
---
# <a name="span-idvspixengineipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arrspanipixelhistorycallback2primitivescallback-method"></a><span data-ttu-id="be3e0-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2: método rimitivesCallback de:P</span><span class="sxs-lookup"><span data-stu-id="be3e0-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2::PrimitivesCallback method</span></span>

<span data-ttu-id="be3e0-104">Um retorno de chamada que notifica o host das informações de operação primitivas do histórico de pixel retornado pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="be3e0-104">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be3e0-105">Syntax</span></span>


```C++
HRESULT PrimitivesCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_primitives
);
```

## <a name="parameters"></a><span data-ttu-id="be3e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be3e0-106">Parameters</span></span>

<span data-ttu-id="be3e0-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="be3e0-107">*count* </span></span>  
<span data-ttu-id="be3e0-108">O número de primitivos.</span><span class="sxs-lookup"><span data-stu-id="be3e0-108">The number of primitives.</span></span>

<span data-ttu-id="be3e0-109">*\_primitivos count0* </span><span class="sxs-lookup"><span data-stu-id="be3e0-109">*count0\_primitives* </span></span>  
<span data-ttu-id="be3e0-110">Os primitivos.</span><span class="sxs-lookup"><span data-stu-id="be3e0-110">The primitives.</span></span>

## <a name="return-value"></a><span data-ttu-id="be3e0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be3e0-111">Return value</span></span>

<span data-ttu-id="be3e0-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="be3e0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be3e0-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be3e0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="be3e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be3e0-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="be3e0-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be3e0-115">Header</span></span></p></td><td><span data-ttu-id="be3e0-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="be3e0-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="be3e0-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="be3e0-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="be3e0-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="be3e0-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
