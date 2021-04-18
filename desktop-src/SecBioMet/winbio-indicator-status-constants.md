---
title: Constantes de WINBIO_INDICATOR_STATUS (WinBio \_ Types. h)
description: Definir uma luz do indicador.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800094"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="d79c6-103">Constantes de status do \_ indicador WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d79c6-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="d79c6-104">Os valores a seguir podem ser usados para definir uma luz do indicador.</span><span class="sxs-lookup"><span data-stu-id="d79c6-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="d79c6-105">Por padrão, os sensores não terão uma luz acesa, mas os aplicativos podem usar esses valores para habilitar ou desabilitar luzes indicadoras.</span><span class="sxs-lookup"><span data-stu-id="d79c6-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="d79c6-106">O valor de **\_ \_ status do sensor WINBIO** fornece mais detalhes sobre o status de uma luz do indicador em.</span><span class="sxs-lookup"><span data-stu-id="d79c6-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="d79c6-107">Para obter mais informações, consulte as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="d79c6-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="d79c6-108">**SensorAdapterSetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="d79c6-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="d79c6-109">**SensorAdapterGetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="d79c6-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="d79c6-110">**SensorAdapterQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="d79c6-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="d79c6-111">Constante</span><span class="sxs-lookup"><span data-stu-id="d79c6-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="d79c6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d79c6-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="d79c6-113"><dt>**\_indicador \_ de WINBIO em**</dt></span><span class="sxs-lookup"><span data-stu-id="d79c6-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="d79c6-114">A luz do indicador do sensor está acesa.</span><span class="sxs-lookup"><span data-stu-id="d79c6-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="d79c6-115"><dt>**indicador de WINBIO \_ \_ desativado**</dt></span><span class="sxs-lookup"><span data-stu-id="d79c6-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="d79c6-116">A luz do indicador do sensor está desativada.</span><span class="sxs-lookup"><span data-stu-id="d79c6-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d79c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d79c6-117">Requirements</span></span>



| <span data-ttu-id="d79c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d79c6-118">Requirement</span></span> | <span data-ttu-id="d79c6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d79c6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d79c6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d79c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d79c6-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d79c6-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d79c6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d79c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d79c6-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d79c6-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d79c6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d79c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d79c6-125"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d79c6-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d79c6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d79c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79c6-127">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="d79c6-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





