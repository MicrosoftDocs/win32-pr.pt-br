---
description: Solicitações para executar um experimento (captura) no processo especificado.
MS-HAID: vspixengine.IRunExperimentCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IRunExperimentCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C00034DF-5F51-49A2-B49A-62F98EA48F46
api_name:
- IRunExperimentCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ac6838e7103970d588814bdc5a39e9e26fd4a33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105785216"
---
# <a name="span-idvspixengineirunexperimentcallback_resultcallback_dwordspanirunexperimentcallbackresultcallback-method"></a><span data-ttu-id="52625-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>Método IRunExperimentCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="52625-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>IRunExperimentCallback::ResultCallback method</span></span>

<span data-ttu-id="52625-104">Solicitações para executar um experimento (captura) no processo especificado.</span><span class="sxs-lookup"><span data-stu-id="52625-104">Requests to run an experiment (capture) on the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="52625-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52625-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD processId
);
```

## <a name="parameters"></a><span data-ttu-id="52625-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52625-106">Parameters</span></span>

<span data-ttu-id="52625-107">*processId* </span><span class="sxs-lookup"><span data-stu-id="52625-107">*processId* </span></span>  
<span data-ttu-id="52625-108">O processo especificado.</span><span class="sxs-lookup"><span data-stu-id="52625-108">The specified process.</span></span>

## <a name="return-value"></a><span data-ttu-id="52625-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52625-109">Return value</span></span>

<span data-ttu-id="52625-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="52625-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52625-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52625-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="52625-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52625-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="52625-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52625-113">Header</span></span></p></td><td><span data-ttu-id="52625-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="52625-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="52625-115"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="52625-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="52625-116">**IRunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="52625-116">**IRunExperimentCallback**</span></span>](/windows/desktop/direct3dtools/irunexperimentcallback)

 

 
