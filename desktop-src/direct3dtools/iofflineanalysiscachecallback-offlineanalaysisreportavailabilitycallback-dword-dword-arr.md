---
description: Uma função de retorno de chamada usada para notificar o host sobre quais quadros têm relatórios de análise offline disponíveis.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IOfflineAnalysisCacheCallback:: OfflineAnalaysisReportAvailabilityCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763860"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="f72b2-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>Método IOfflineAnalysisCacheCallback:: OfflineAnalaysisReportAvailabilityCallback</span><span class="sxs-lookup"><span data-stu-id="f72b2-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="f72b2-104">Uma função de retorno de chamada usada para notificar o host sobre quais quadros têm relatórios de análise offline disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f72b2-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f72b2-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="f72b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f72b2-106">Parameters</span></span>

<span data-ttu-id="f72b2-107">*numFramesWithReports* </span><span class="sxs-lookup"><span data-stu-id="f72b2-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="f72b2-108">O número de quadros em count0 \_ framesWithReports.</span><span class="sxs-lookup"><span data-stu-id="f72b2-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="f72b2-109">*count0 \_ framesWithReports* </span><span class="sxs-lookup"><span data-stu-id="f72b2-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="f72b2-110">Uma matriz que contém os números de quadro dos quadros que têm relatórios de análise offline disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f72b2-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="f72b2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f72b2-111">Return value</span></span>

<span data-ttu-id="f72b2-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f72b2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f72b2-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f72b2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72b2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72b2-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f72b2-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f72b2-115">Header</span></span></p></td><td><span data-ttu-id="f72b2-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f72b2-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f72b2-117"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="f72b2-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f72b2-118">**IOfflineAnalysisCacheCallback**</span><span class="sxs-lookup"><span data-stu-id="f72b2-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
