---
description: Um retorno de chamada que notifica o host das informações de interseção do histórico de pixel retornado pela solicitação assocaited.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixelHistoryCallback2:: IntersectionsCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087547"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="4bc70-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>Método IPixelHistoryCallback2:: IntersectionsCallback</span><span class="sxs-lookup"><span data-stu-id="4bc70-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="4bc70-104">Um retorno de chamada que notifica o host das informações de interseção do histórico de pixel retornado pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="4bc70-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc70-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bc70-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="4bc70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bc70-106">Parameters</span></span>

<span data-ttu-id="4bc70-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="4bc70-107">*count* </span></span>  
<span data-ttu-id="4bc70-108">O número de interseções de histórico de pixel.</span><span class="sxs-lookup"><span data-stu-id="4bc70-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="4bc70-109">*interseções count0 \_* </span><span class="sxs-lookup"><span data-stu-id="4bc70-109">*count0\_intersections* </span></span>  
<span data-ttu-id="4bc70-110">As interseções de histórico de pixel.</span><span class="sxs-lookup"><span data-stu-id="4bc70-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bc70-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4bc70-111">Return value</span></span>

<span data-ttu-id="4bc70-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4bc70-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bc70-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4bc70-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc70-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bc70-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4bc70-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bc70-115">Header</span></span></p></td><td><span data-ttu-id="4bc70-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4bc70-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4bc70-117"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="4bc70-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4bc70-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="4bc70-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
