---
description: Uma solicitação assíncrona para obter os quadros de lista capturados no log de gráficos.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameListRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009921"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="406b6-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>Método IFrameListRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="406b6-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="406b6-104">Uma solicitação assíncrona para obter os quadros de lista capturados no log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="406b6-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="406b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="406b6-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="406b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="406b6-106">Parameters</span></span>

<span data-ttu-id="406b6-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="406b6-107">*requestCallback* </span></span>  
<span data-ttu-id="406b6-108">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="406b6-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="406b6-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="406b6-109">*requestCookie* </span></span>  
<span data-ttu-id="406b6-110">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="406b6-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="406b6-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="406b6-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="406b6-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="406b6-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="406b6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="406b6-113">Return value</span></span>

<span data-ttu-id="406b6-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="406b6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="406b6-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="406b6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="406b6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="406b6-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="406b6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="406b6-117">Header</span></span></p></td><td><span data-ttu-id="406b6-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="406b6-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="406b6-119"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="406b6-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="406b6-120">**IFrameListRequest**</span><span class="sxs-lookup"><span data-stu-id="406b6-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 
