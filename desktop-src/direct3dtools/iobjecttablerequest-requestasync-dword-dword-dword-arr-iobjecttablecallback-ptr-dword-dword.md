---
description: Solicitações para obter informações especificadas da tabela de objetos para o evento especificado.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IObjectTableRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645956"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="fbf50-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>Método IObjectTableRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="fbf50-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="fbf50-104">Solicitações para obter informações especificadas da tabela de objetos para o evento especificado.</span><span class="sxs-lookup"><span data-stu-id="fbf50-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbf50-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fbf50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbf50-106">Parameters</span></span>

<span data-ttu-id="fbf50-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="fbf50-107">*eventID* </span></span>  
<span data-ttu-id="fbf50-108">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="fbf50-108">The specified event.</span></span>

<span data-ttu-id="fbf50-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="fbf50-109">*numColumns* </span></span>  
<span data-ttu-id="fbf50-110">O número de colunas (campos) de informações a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="fbf50-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="fbf50-111">*\_colunas count1* </span><span class="sxs-lookup"><span data-stu-id="fbf50-111">*count1\_columns* </span></span>  
<span data-ttu-id="fbf50-112">As colunas especificadas (campos).</span><span class="sxs-lookup"><span data-stu-id="fbf50-112">The specified columns (fields).</span></span>

<span data-ttu-id="fbf50-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="fbf50-113">*requestCallback* </span></span>  
<span data-ttu-id="fbf50-114">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="fbf50-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fbf50-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="fbf50-115">*requestCookie* </span></span>  
<span data-ttu-id="fbf50-116">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="fbf50-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fbf50-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="fbf50-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fbf50-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="fbf50-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbf50-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbf50-119">Return value</span></span>

<span data-ttu-id="fbf50-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fbf50-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbf50-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbf50-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf50-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf50-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbf50-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbf50-123">Header</span></span></p></td><td><span data-ttu-id="fbf50-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fbf50-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fbf50-125"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="fbf50-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fbf50-126">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="fbf50-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
