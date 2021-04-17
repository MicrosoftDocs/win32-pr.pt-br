---
description: O \_ tipo de enumeração de modos flash WPD \_ descreve um modo flash para usar ao capturar imagens com um dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Enumeração de WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754464"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="eca29-103">\_Enumeração de \_ modos flash WPD</span><span class="sxs-lookup"><span data-stu-id="eca29-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="eca29-104">O tipo de enumeração de **\_ \_ modos flash WPD** descreve um modo flash para usar ao capturar imagens com um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eca29-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca29-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="eca29-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="eca29-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eca29-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_modo flash \_ WPD \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="eca29-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-108">Nenhum modo flash foi especificado.</span><span class="sxs-lookup"><span data-stu-id="eca29-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="eca29-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_modo flash \_ WPD \_ automático**</span><span class="sxs-lookup"><span data-stu-id="eca29-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-110">Especifica que o flash deve ser usado no modo automático, conforme especificado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eca29-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="eca29-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_modo flash \_ WPD \_ desativado**</span><span class="sxs-lookup"><span data-stu-id="eca29-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-112">Especifica que nenhum flash deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="eca29-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="eca29-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_preenchimento do \_ modo \_ flash WPD**</span><span class="sxs-lookup"><span data-stu-id="eca29-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-114">Especifica um flash de tipo de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="eca29-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="eca29-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_modo flash WPD, \_ \_ \_ olhos vermelhos \_ automáticos**</span><span class="sxs-lookup"><span data-stu-id="eca29-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-116">Especifica que o flash de redução de olho vermelho deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="eca29-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="eca29-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_preenchimento de \_ \_ olho vermelho \_ do modo flash WPD \_**</span><span class="sxs-lookup"><span data-stu-id="eca29-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-118">Especifica que o flash de preenchimento de olho vermelho deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="eca29-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="eca29-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ sincronização externa do modo do flash WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eca29-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="eca29-120">Especifica que o flash deve ser sincronizado com outros dispositivos flash externos.</span><span class="sxs-lookup"><span data-stu-id="eca29-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eca29-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="eca29-121">Remarks</span></span>

<span data-ttu-id="eca29-122">Essa enumeração é usada pela propriedade [de \_ \_ \_ \_ modo flash de imagem WPD ainda](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="eca29-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="eca29-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eca29-123">Requirements</span></span>



| <span data-ttu-id="eca29-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca29-124">Requirement</span></span> | <span data-ttu-id="eca29-125">Valor</span><span class="sxs-lookup"><span data-stu-id="eca29-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca29-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eca29-126">Header</span></span><br/> | <dl> <span data-ttu-id="eca29-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="eca29-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca29-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eca29-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca29-129">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="eca29-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




