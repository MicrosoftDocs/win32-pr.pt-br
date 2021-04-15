---
description: Solicitações para cancelar a análise offline em uma solicitação de análise offline.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IOfflineAnalysisRequest:: CancelOfflineAnalysisAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456569"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="a348f-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>Método IOfflineAnalysisRequest:: CancelOfflineAnalysisAsync</span><span class="sxs-lookup"><span data-stu-id="a348f-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="a348f-104">Solicitações para cancelar a análise offline em uma solicitação de análise offline.</span><span class="sxs-lookup"><span data-stu-id="a348f-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a348f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a348f-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="a348f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a348f-106">Parameters</span></span>

<span data-ttu-id="a348f-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="a348f-107">*cookie* </span></span>  
<span data-ttu-id="a348f-108">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="a348f-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="a348f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a348f-109">Return value</span></span>

<span data-ttu-id="a348f-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a348f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a348f-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a348f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a348f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a348f-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a348f-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a348f-113">Header</span></span></p></td><td><span data-ttu-id="a348f-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a348f-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a348f-115"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="a348f-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a348f-116">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="a348f-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
