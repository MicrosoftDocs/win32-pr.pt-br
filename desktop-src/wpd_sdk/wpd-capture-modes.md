---
description: O \_ tipo de enumeração de modos de captura WPD \_ descreve o modo de captura de tempo de uma captura de imagem ainda.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Enumeração de WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798483"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="51ac7-103">Enumeração de modos de \_ captura WPD \_</span><span class="sxs-lookup"><span data-stu-id="51ac7-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="51ac7-104">O tipo de enumeração de **\_ \_ modos de captura WPD** descreve o modo de captura de tempo de uma captura de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="51ac7-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ac7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51ac7-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="51ac7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="51ac7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51ac7-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**\_modo de captura WPD \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="51ac7-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="51ac7-108">O modo de captura não foi definido.</span><span class="sxs-lookup"><span data-stu-id="51ac7-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="51ac7-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**modo de captura do WPD \_ \_ \_ normal**</span><span class="sxs-lookup"><span data-stu-id="51ac7-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="51ac7-110">Nenhum modo de atraso ou intermitência deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="51ac7-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51ac7-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_intermitência do \_ modo de captura WPD \_**</span><span class="sxs-lookup"><span data-stu-id="51ac7-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="51ac7-112">Especifica que um número definido de imagens deve ser capturado com um intervalo definido entre eles.</span><span class="sxs-lookup"><span data-stu-id="51ac7-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="51ac7-113">O número de imagens a serem capturadas e o atraso de tempo entre elas são especificados pelo [ \_ número de \_ \_ intermitência \_ de imagem](still-image-properties.md) e pelas propriedades de [ \_ \_ \_ \_ intervalo de intermitência de imagem ainda](still-image-properties.md) mais específicas.</span><span class="sxs-lookup"><span data-stu-id="51ac7-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="51ac7-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_modo de captura WPD \_ \_ TIMELAPSE**</span><span class="sxs-lookup"><span data-stu-id="51ac7-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="51ac7-115">A captura de imagem deve usar a fotografia de tempo.</span><span class="sxs-lookup"><span data-stu-id="51ac7-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="51ac7-116">O número de imagens e o intervalo entre elas são descritos pelas propriedades de [ \_ \_ \_ \_ intervalo](still-image-properties.md) de [ \_ \_ \_ TIMELAPSE \_ de imagem WPD](still-image-properties.md) e WPD ainda.</span><span class="sxs-lookup"><span data-stu-id="51ac7-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51ac7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="51ac7-117">Remarks</span></span>

<span data-ttu-id="51ac7-118">Essa enumeração é usada pela propriedade [do \_ \_ modo de \_ captura \_ de imagem WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="51ac7-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ac7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ac7-119">Requirements</span></span>



| <span data-ttu-id="51ac7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51ac7-120">Requirement</span></span> | <span data-ttu-id="51ac7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="51ac7-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ac7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51ac7-122">Header</span></span><br/> | <dl> <span data-ttu-id="51ac7-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="51ac7-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ac7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="51ac7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ac7-125">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="51ac7-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="51ac7-126">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="51ac7-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




