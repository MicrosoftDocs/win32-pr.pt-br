---
description: Uma solicitação assíncrona para obter informações resumidas sobre um log de gráficos.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ISummaryRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105802051"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="34ba9-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>Método ISummaryRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="34ba9-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="34ba9-104">Uma solicitação assíncrona para obter informações resumidas sobre um log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="34ba9-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ba9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34ba9-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="34ba9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34ba9-106">Parameters</span></span>

<span data-ttu-id="34ba9-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="34ba9-107">*requestCallback* </span></span>  
<span data-ttu-id="34ba9-108">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="34ba9-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="34ba9-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="34ba9-109">*requestCookie* </span></span>  
<span data-ttu-id="34ba9-110">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="34ba9-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="34ba9-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="34ba9-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="34ba9-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="34ba9-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="34ba9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34ba9-113">Return value</span></span>

<span data-ttu-id="34ba9-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="34ba9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34ba9-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34ba9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ba9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34ba9-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="34ba9-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34ba9-117">Header</span></span></p></td><td><span data-ttu-id="34ba9-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="34ba9-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="34ba9-119"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="34ba9-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="34ba9-120">**ISummaryRequest**</span><span class="sxs-lookup"><span data-stu-id="34ba9-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
