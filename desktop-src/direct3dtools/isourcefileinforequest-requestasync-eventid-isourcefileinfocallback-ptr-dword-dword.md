---
description: Uma solicitação assíncrona para obter os arquivos de origem associados à pilha de chamadas de um evento.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ISourceFileInfoRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba5fddf153b2a771ab54bf89036f8087ad0f7524
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105765083"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span data-ttu-id="40e45-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>Método ISourceFileInfoRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="40e45-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest::RequestAsync method</span></span>

<span data-ttu-id="40e45-104">Uma solicitação assíncrona para obter os arquivos de origem associados à pilha de chamadas de um evento.</span><span class="sxs-lookup"><span data-stu-id="40e45-104">An asynchronous request to get the source files associated with the callstack of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e45-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40e45-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="40e45-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40e45-106">Parameters</span></span>

<span data-ttu-id="40e45-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="40e45-107">*eventID* </span></span>  
<span data-ttu-id="40e45-108">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="40e45-108">The specified event.</span></span>

<span data-ttu-id="40e45-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="40e45-109">*requestCallback* </span></span>  
<span data-ttu-id="40e45-110">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="40e45-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="40e45-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="40e45-111">*requestCookie* </span></span>  
<span data-ttu-id="40e45-112">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="40e45-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="40e45-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="40e45-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="40e45-114">Não usado.</span><span class="sxs-lookup"><span data-stu-id="40e45-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="40e45-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40e45-115">Return value</span></span>

<span data-ttu-id="40e45-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="40e45-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40e45-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="40e45-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40e45-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e45-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="40e45-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40e45-119">Header</span></span></p></td><td><span data-ttu-id="40e45-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="40e45-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="40e45-121"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="40e45-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="40e45-122">**ISourceFileInfoRequest**</span><span class="sxs-lookup"><span data-stu-id="40e45-122">**ISourceFileInfoRequest**</span></span>](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
