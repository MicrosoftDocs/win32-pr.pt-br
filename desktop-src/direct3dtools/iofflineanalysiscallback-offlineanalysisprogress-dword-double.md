---
description: Uma função de retorno de chamada usada para notificar o host do progresso da análise offline.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IOfflineAnalysisCallback:: OfflineAnalysisProgress'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370321"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="58014-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>Método IOfflineAnalysisCallback:: OfflineAnalysisProgress</span><span class="sxs-lookup"><span data-stu-id="58014-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="58014-104">Uma função de retorno de chamada usada para notificar o host do progresso da análise offline.</span><span class="sxs-lookup"><span data-stu-id="58014-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="58014-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58014-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="58014-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58014-106">Parameters</span></span>

<span data-ttu-id="58014-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="58014-107">*cookie* </span></span>  
<span data-ttu-id="58014-108">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="58014-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="58014-109">*andamento* </span><span class="sxs-lookup"><span data-stu-id="58014-109">*progress* </span></span>  
<span data-ttu-id="58014-110">A porcentagem de progresso.</span><span class="sxs-lookup"><span data-stu-id="58014-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="58014-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58014-111">Return value</span></span>

<span data-ttu-id="58014-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="58014-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58014-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58014-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="58014-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58014-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="58014-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58014-115">Header</span></span></p></td><td><span data-ttu-id="58014-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="58014-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="58014-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="58014-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="58014-118">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="58014-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
