---
description: Uma solicitação assíncrona para obter dados de malha do evento especificado.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesRequest3:: RequestMeshAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812241"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="6f938-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>Método IPipeLineStagesRequest3:: RequestMeshAsync</span><span class="sxs-lookup"><span data-stu-id="6f938-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="6f938-104">Uma solicitação assíncrona para obter dados de malha do evento especificado.</span><span class="sxs-lookup"><span data-stu-id="6f938-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f938-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f938-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="6f938-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f938-106">Parameters</span></span>

<span data-ttu-id="6f938-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="6f938-107">*eventID* </span></span>  
<span data-ttu-id="6f938-108">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="6f938-108">The specified event.</span></span>

<span data-ttu-id="6f938-109">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="6f938-109">*meshFilename* </span></span>  
<span data-ttu-id="6f938-110">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde os dados de malha são gravados.</span><span class="sxs-lookup"><span data-stu-id="6f938-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="6f938-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="6f938-111">*requestCallback* </span></span>  
<span data-ttu-id="6f938-112">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="6f938-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="6f938-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="6f938-113">*requestCookie* </span></span>  
<span data-ttu-id="6f938-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="6f938-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="6f938-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="6f938-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="6f938-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6f938-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f938-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f938-117">Return value</span></span>

<span data-ttu-id="6f938-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f938-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f938-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f938-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f938-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f938-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6f938-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f938-121">Header</span></span></p></td><td><span data-ttu-id="6f938-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6f938-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6f938-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="6f938-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6f938-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="6f938-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
