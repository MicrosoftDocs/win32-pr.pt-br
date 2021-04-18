---
description: O \_ tipo de enumeração dos modos de programas de exposição WPD \_ \_ descreve um modo de exposição a ser usado ao capturar imagens com um dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Enumeração de WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758487"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="d6b4a-103">\_Enumeração de \_ modos de programas de exposição WPD \_</span><span class="sxs-lookup"><span data-stu-id="d6b4a-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="d6b4a-104">O tipo de enumeração dos **\_ modos de \_ programas \_ de exposição WPD** descreve um modo de exposição a ser usado ao capturar imagens com um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6b4a-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="d6b4a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d6b4a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d6b4a-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_modo de programa de exposição WPD \_ \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-108">O modo de exposição não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_manual do \_ modo de programa de exposição WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-110">O aplicativo deve especificar todas as configurações de exposição.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_modo de \_ programa de exposição \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-112">Use um modo de exposição automática definido pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_prioridade de \_ abertura do modo de programa de exposição WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-114">Um modo de exposição automatizada que indica que o valor de abertura da lente deve permanecer fixo, mas a velocidade do obturador deve ser determinada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_prioridade de \_ \_ \_ obturador do modo de programa de exposição WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-116">Um modo de exposição automatizada que indica que a velocidade do obturador deve permanecer fixa, mas que a abertura da lente deve ser determinada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_modo de programa de exposição WPD \_ \_ \_ Creative**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-118">Um modo de exposição automatizada que tenta maximizar a profundidade do campo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_ação do \_ modo de programa de exposição WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-120">Um modo de exposição automatizada que tenta maximizar a velocidade do obturador.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4a-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**\_modo de programa de exposição WPD \_ \_ \_ retrato**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="d6b4a-122">Um modo de exposição automatizada que especifica uma profundidade relativamente superficial do campo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6b4a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6b4a-123">Remarks</span></span>

<span data-ttu-id="d6b4a-124">Indica o modo do programa de exposição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="d6b4a-125">Essa enumeração é usada pela propriedade [de \_ \_ modo do \_ \_ programa de \_ exposição de imagem WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b4a-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b4a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6b4a-126">Requirements</span></span>



| <span data-ttu-id="d6b4a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6b4a-127">Requirement</span></span> | <span data-ttu-id="d6b4a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d6b4a-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b4a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6b4a-129">Header</span></span><br/> | <dl> <span data-ttu-id="d6b4a-130"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6b4a-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b4a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6b4a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b4a-132">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




