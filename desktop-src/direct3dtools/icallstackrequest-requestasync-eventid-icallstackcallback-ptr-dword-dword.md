---
description: Uma solicitação assíncrona para obter a pilha de chamadas RVAs (endereços virtuais relativos) do evento especificado.
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ICallStackRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163800"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="6e219-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>Método ICallStackRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="6e219-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="6e219-104">Uma solicitação assíncrona para obter a pilha de chamadas RVAs (endereços virtuais relativos) do evento especificado.</span><span class="sxs-lookup"><span data-stu-id="6e219-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e219-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e219-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="6e219-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e219-106">Parameters</span></span>

<span data-ttu-id="6e219-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="6e219-107">*eventID* </span></span>  
<span data-ttu-id="6e219-108">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="6e219-108">The specified event.</span></span>

<span data-ttu-id="6e219-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="6e219-109">*requestCallback* </span></span>  
<span data-ttu-id="6e219-110">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="6e219-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="6e219-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="6e219-111">*requestCookie* </span></span>  
<span data-ttu-id="6e219-112">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="6e219-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="6e219-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="6e219-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="6e219-114">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6e219-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e219-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e219-115">Return value</span></span>

<span data-ttu-id="6e219-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e219-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e219-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e219-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e219-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e219-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6e219-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e219-119">Header</span></span></p></td><td><span data-ttu-id="6e219-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6e219-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6e219-121"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="6e219-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6e219-122">**ICallStackRequest**</span><span class="sxs-lookup"><span data-stu-id="6e219-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 
