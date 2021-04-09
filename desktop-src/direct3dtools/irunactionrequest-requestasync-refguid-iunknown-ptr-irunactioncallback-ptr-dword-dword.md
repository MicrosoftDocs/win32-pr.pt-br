---
description: Uma solicitação assíncrona para iniciar uma ação (por exemplo, capturar um quadro) no mecanismo.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IRunActionRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087886"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="d3d8c-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>Método IRunActionRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="d3d8c-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="d3d8c-104">Uma solicitação assíncrona para iniciar uma ação (por exemplo, capturar um quadro) no mecanismo.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3d8c-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d3d8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3d8c-106">Parameters</span></span>

<span data-ttu-id="d3d8c-107">*Action* </span><span class="sxs-lookup"><span data-stu-id="d3d8c-107">*action* </span></span>  
<span data-ttu-id="d3d8c-108">A ação especificada.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-108">The specified action.</span></span>

<span data-ttu-id="d3d8c-109">*actionPayload* </span><span class="sxs-lookup"><span data-stu-id="d3d8c-109">*actionPayload* </span></span>  
<span data-ttu-id="d3d8c-110">A carga da ação especificada.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-110">The payload of the specified action.</span></span>

<span data-ttu-id="d3d8c-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="d3d8c-111">*requestCallback* </span></span>  
<span data-ttu-id="d3d8c-112">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d3d8c-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d3d8c-113">*requestCookie* </span></span>  
<span data-ttu-id="d3d8c-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d3d8c-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d3d8c-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d3d8c-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3d8c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3d8c-117">Return value</span></span>

<span data-ttu-id="d3d8c-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3d8c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3d8c-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3d8c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d8c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d8c-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d3d8c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3d8c-121">Header</span></span></p></td><td><span data-ttu-id="d3d8c-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d3d8c-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d3d8c-123"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="d3d8c-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d3d8c-124">**IRunActionRequest**</span><span class="sxs-lookup"><span data-stu-id="d3d8c-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 
