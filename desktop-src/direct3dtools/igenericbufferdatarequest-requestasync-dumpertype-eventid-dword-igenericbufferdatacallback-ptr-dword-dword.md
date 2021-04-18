---
description: Solicitações para retornar dados de objeto genérico que descrevem um objeto no arquivo. vsglog para o evento especificado e no formato especificado.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IGenericBufferDataRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105788740"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="b8fe0-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>Método IGenericBufferDataRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="b8fe0-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="b8fe0-104">Solicitações para retornar dados de objeto genérico que descrevem um objeto no arquivo. vsglog para o evento especificado e no formato especificado.</span><span class="sxs-lookup"><span data-stu-id="b8fe0-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fe0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8fe0-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b8fe0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8fe0-106">Parameters</span></span>

<span data-ttu-id="b8fe0-107">*dumperType* </span><span class="sxs-lookup"><span data-stu-id="b8fe0-107">*dumperType* </span></span>  
<span data-ttu-id="b8fe0-108">O formato especificado da representação textual do objeto (HTML, XML, etc.)</span><span class="sxs-lookup"><span data-stu-id="b8fe0-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="b8fe0-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="b8fe0-109">*eventID* </span></span>  
<span data-ttu-id="b8fe0-110">O evento especificado para corresponder ao conteúdo do buffer (por exemplo, um destino de renderização pode mudar ao longo do tempo).</span><span class="sxs-lookup"><span data-stu-id="b8fe0-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="b8fe0-111">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="b8fe0-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="b8fe0-112">O endereço do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="b8fe0-112">The address of the specified object.</span></span>

<span data-ttu-id="b8fe0-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b8fe0-113">*requestCallback* </span></span>  
<span data-ttu-id="b8fe0-114">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="b8fe0-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b8fe0-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b8fe0-115">*requestCookie* </span></span>  
<span data-ttu-id="b8fe0-116">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="b8fe0-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b8fe0-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b8fe0-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b8fe0-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b8fe0-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8fe0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8fe0-119">Return value</span></span>

<span data-ttu-id="b8fe0-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b8fe0-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8fe0-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8fe0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8fe0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8fe0-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b8fe0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8fe0-123">Header</span></span></p></td><td><span data-ttu-id="b8fe0-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b8fe0-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b8fe0-125"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="b8fe0-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b8fe0-126">**IGenericBufferDataRequest**</span><span class="sxs-lookup"><span data-stu-id="b8fe0-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
