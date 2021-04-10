---
description: Uma função de retorno de chamada usada para notificar o host de informações sobre eventos na lista de eventos.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameEventsCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163796"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="1b8f9-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Método IFrameEventsCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="1b8f9-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="1b8f9-104">Uma função de retorno de chamada usada para notificar o host de informações sobre eventos na lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b8f9-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="1b8f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b8f9-106">Parameters</span></span>

<span data-ttu-id="1b8f9-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="1b8f9-107">*frameNumber* </span></span>  
<span data-ttu-id="1b8f9-108">O número do quadro associado aos eventos.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-108">The frame number associated with the events.</span></span>

<span data-ttu-id="1b8f9-109">*numElements* </span><span class="sxs-lookup"><span data-stu-id="1b8f9-109">*numElements* </span></span>  
<span data-ttu-id="1b8f9-110">O número total de campos em todas as colunas de todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="1b8f9-111">*numRows* </span><span class="sxs-lookup"><span data-stu-id="1b8f9-111">*numRows* </span></span>  
<span data-ttu-id="1b8f9-112">O número de eventos no resultado.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-112">The number of events in the result.</span></span>

<span data-ttu-id="1b8f9-113">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="1b8f9-113">*numColumns* </span></span>  
<span data-ttu-id="1b8f9-114">O número de colunas (campos) em cada linha.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="1b8f9-115">*count1 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="1b8f9-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="1b8f9-116">Informações sobre os eventos; um item para cada campo de cada evento.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b8f9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b8f9-117">Return value</span></span>

<span data-ttu-id="1b8f9-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1b8f9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b8f9-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b8f9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8f9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b8f9-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1b8f9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b8f9-121">Header</span></span></p></td><td><span data-ttu-id="1b8f9-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1b8f9-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1b8f9-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="1b8f9-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1b8f9-124">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="1b8f9-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
