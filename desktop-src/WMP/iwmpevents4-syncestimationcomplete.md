---
title: Método IWMPEvents4 SyncEstimationComplete
description: O evento SyncEstimationComplete ocorre quando uma estimativa de tamanho, iniciada anteriormente pelo IWMPSyncDevice3 estimateSyncSize, é concluída.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Método SyncEstimationComplete Windows Media Player
- Método SyncEstimationComplete Windows Media Player, interface IWMPEvents4
- Interface IWMPEvents4 Windows Media Player, método SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640117"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="ba97e-106">Método IWMPEvents4:: SyncEstimationComplete</span><span class="sxs-lookup"><span data-stu-id="ba97e-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="ba97e-107">O evento **SyncEstimationComplete** ocorre quando uma estimativa de tamanho, iniciada anteriormente por [**IWMPSyncDevice3:: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), é concluída.</span><span class="sxs-lookup"><span data-stu-id="ba97e-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba97e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba97e-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="ba97e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba97e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba97e-110">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba97e-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba97e-111">Ponteiro para a interface [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) que representa o dispositivo para o qual a estimativa de tamanho foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="ba97e-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="ba97e-112">*hrResult* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba97e-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba97e-113">Um valor que indica o êxito ou a falha da estimativa.</span><span class="sxs-lookup"><span data-stu-id="ba97e-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="ba97e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ba97e-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="ba97e-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ba97e-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="ba97e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba97e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ba97e-117">A estimativa foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ba97e-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="ba97e-118"><dt>**E \_ anular**</dt></span><span class="sxs-lookup"><span data-stu-id="ba97e-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="ba97e-119">A estimativa foi anulada.</span><span class="sxs-lookup"><span data-stu-id="ba97e-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ba97e-120">*lEstimatedUsedSpace* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba97e-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba97e-121">O espaço estimado (em bytes) que seria usado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba97e-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="ba97e-122">*lEstimatedSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba97e-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba97e-123">O tamanho estimado (em bytes) dos dados a serem sincronizados.</span><span class="sxs-lookup"><span data-stu-id="ba97e-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba97e-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba97e-124">Return value</span></span>

<span data-ttu-id="ba97e-125">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ba97e-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba97e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba97e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba97e-127">**Interface IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="ba97e-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="ba97e-128">**IWMPSyncDevice3::estimateSyncSize**</span><span class="sxs-lookup"><span data-stu-id="ba97e-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





