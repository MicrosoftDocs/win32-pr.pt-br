---
description: Uma solicitação assíncrona para obter informações sobre quais colunas (campos) esse tipo de solicitação de eventos de quadro dá suporte.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameEventsRequest:: RequestSupportedColumnsAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645957"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="4d2fe-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>Método IFrameEventsRequest:: RequestSupportedColumnsAsync</span><span class="sxs-lookup"><span data-stu-id="4d2fe-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="4d2fe-104">Uma solicitação assíncrona para obter informações sobre quais colunas (campos) esse tipo de solicitação de eventos de quadro dá suporte.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-104">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d2fe-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4d2fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d2fe-106">Parameters</span></span>

<span data-ttu-id="4d2fe-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4d2fe-107">*requestCallback* </span></span>  
<span data-ttu-id="4d2fe-108">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4d2fe-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4d2fe-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4d2fe-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d2fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d2fe-111">Return value</span></span>

<span data-ttu-id="4d2fe-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d2fe-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d2fe-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d2fe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d2fe-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4d2fe-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d2fe-115">Header</span></span></p></td><td><span data-ttu-id="4d2fe-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4d2fe-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4d2fe-117"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="4d2fe-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4d2fe-118">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="4d2fe-118">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
