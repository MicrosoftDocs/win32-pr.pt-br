---
description: Um retorno de chamada que notifica o host dos resultados da solicitação de histórico de pixel.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixelHistoryCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296044"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="d3cbb-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>Método IPixelHistoryCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="d3cbb-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="d3cbb-104">Um retorno de chamada que notifica o host dos resultados da solicitação de histórico de pixel.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3cbb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3cbb-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="d3cbb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3cbb-106">Parameters</span></span>

<span data-ttu-id="d3cbb-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="d3cbb-107">*count* </span></span>  
<span data-ttu-id="d3cbb-108">O número de resultados.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-108">The number of results.</span></span>

<span data-ttu-id="d3cbb-109">*count0 \_ pixelHistoryOperation* </span><span class="sxs-lookup"><span data-stu-id="d3cbb-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="d3cbb-110">Os resultados.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3cbb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3cbb-111">Return value</span></span>

<span data-ttu-id="d3cbb-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3cbb-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3cbb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3cbb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3cbb-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d3cbb-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3cbb-115">Header</span></span></p></td><td><span data-ttu-id="d3cbb-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d3cbb-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d3cbb-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="d3cbb-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d3cbb-118">**IPixelHistoryCallback**</span><span class="sxs-lookup"><span data-stu-id="d3cbb-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
