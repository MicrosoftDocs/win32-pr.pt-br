---
description: O \_ tipo de enumeração de modos de medição de exposição WPD \_ \_ descreve o modo de medição a ser usado ao estimar a exposição da captura de imagem ainda por um dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Enumeração de WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757640"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="15b91-103">\_Enumeração de \_ modos de medição de exposição WPD \_</span><span class="sxs-lookup"><span data-stu-id="15b91-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="15b91-104">O tipo de enumeração de **\_ modos de \_ medição \_ de exposição WPD** descreve o modo de medição a ser usado ao estimar a exposição da captura de imagem ainda por um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b91-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b91-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="15b91-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="15b91-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="15b91-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_modo de medição de exposição WPD \_ \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="15b91-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="15b91-108">O modo de medição é indefinido.</span><span class="sxs-lookup"><span data-stu-id="15b91-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="15b91-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_média do \_ modo de medição de exposição WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15b91-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="15b91-110">Use a exposição em média na imagem completa.</span><span class="sxs-lookup"><span data-stu-id="15b91-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="15b91-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ média ponderada do modo de medição de exposição do \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="15b91-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="15b91-112">Use uma exposição média, com o centro da imagem, dado mais peso.</span><span class="sxs-lookup"><span data-stu-id="15b91-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="15b91-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**\_ \_ \_ \_ vários pontos do modo de medição de exposição WPD \_**</span><span class="sxs-lookup"><span data-stu-id="15b91-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="15b91-114">Use uma técnica de média de vários pontos.</span><span class="sxs-lookup"><span data-stu-id="15b91-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="15b91-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_ \_ \_ ponto central do modo de medição de \_ exposição WPD \_**</span><span class="sxs-lookup"><span data-stu-id="15b91-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="15b91-116">Use uma técnica de média de pontos centrais.</span><span class="sxs-lookup"><span data-stu-id="15b91-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15b91-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="15b91-117">Remarks</span></span>

<span data-ttu-id="15b91-118">Indica o modo de medição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b91-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="15b91-119">Essa enumeração é usada pela propriedade [de \_ \_ modo de \_ \_ medição \_ de exposição de imagem WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="15b91-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="15b91-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15b91-120">Requirements</span></span>



| <span data-ttu-id="15b91-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="15b91-121">Requirement</span></span> | <span data-ttu-id="15b91-122">Valor</span><span class="sxs-lookup"><span data-stu-id="15b91-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b91-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15b91-123">Header</span></span><br/> | <dl> <span data-ttu-id="15b91-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="15b91-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b91-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="15b91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b91-126">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="15b91-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




