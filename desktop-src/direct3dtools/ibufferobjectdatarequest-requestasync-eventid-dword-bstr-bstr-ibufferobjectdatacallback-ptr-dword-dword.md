---
description: Solicitações para obter o conteúdo bruto de um objeto (buffer, textura, exibição de destino de renderização, etc.).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IBufferObjectDataRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087489"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="91a2a-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>Método IBufferObjectDataRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="91a2a-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="91a2a-104">Solicitações para obter o conteúdo bruto de um objeto (buffer, textura, exibição de destino de renderização, etc.)</span><span class="sxs-lookup"><span data-stu-id="91a2a-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="91a2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91a2a-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="91a2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91a2a-106">Parameters</span></span>

<span data-ttu-id="91a2a-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="91a2a-107">*eventID* </span></span>  
<span data-ttu-id="91a2a-108">O evento especificado para corresponder ao conteúdo do buffer (por exemplo, um destino de renderização pode mudar ao longo do tempo).</span><span class="sxs-lookup"><span data-stu-id="91a2a-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="91a2a-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="91a2a-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="91a2a-110">O endereço do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="91a2a-110">The address of the specified object.</span></span>

<span data-ttu-id="91a2a-111">*Grupo* </span><span class="sxs-lookup"><span data-stu-id="91a2a-111">*File* </span></span>  
<span data-ttu-id="91a2a-112">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde os resultados são gravados.</span><span class="sxs-lookup"><span data-stu-id="91a2a-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="91a2a-113">*Ao* </span><span class="sxs-lookup"><span data-stu-id="91a2a-113">*Format* </span></span>  
<span data-ttu-id="91a2a-114">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="91a2a-114">Not currently used.</span></span> <span data-ttu-id="91a2a-115">Uma cadeia de caracteres COM que especifica o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="91a2a-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="91a2a-116">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="91a2a-116">*requestCallback* </span></span>  
<span data-ttu-id="91a2a-117">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="91a2a-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="91a2a-118">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="91a2a-118">*requestCookie* </span></span>  
<span data-ttu-id="91a2a-119">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="91a2a-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="91a2a-120">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="91a2a-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="91a2a-121">Não usado.</span><span class="sxs-lookup"><span data-stu-id="91a2a-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="91a2a-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91a2a-122">Return value</span></span>

<span data-ttu-id="91a2a-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="91a2a-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91a2a-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91a2a-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a2a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a2a-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="91a2a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91a2a-126">Header</span></span></p></td><td><span data-ttu-id="91a2a-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="91a2a-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="91a2a-128"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="91a2a-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="91a2a-129">**IBufferObjectDataRequest**</span><span class="sxs-lookup"><span data-stu-id="91a2a-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
