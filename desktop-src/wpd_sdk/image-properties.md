---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de imagem.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propriedades da imagem (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753893"
---
# <a name="image-properties"></a><span data-ttu-id="1cb15-103">Propriedades da imagem</span><span class="sxs-lookup"><span data-stu-id="1cb15-103">Image Properties</span></span>

<span data-ttu-id="1cb15-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de imagem.</span><span class="sxs-lookup"><span data-stu-id="1cb15-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="1cb15-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1cb15-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="1cb15-106">VarType</span><span class="sxs-lookup"><span data-stu-id="1cb15-106">VarType</span></span>     | <span data-ttu-id="1cb15-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cb15-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb15-108">**\_BITDEPTH de imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="1cb15-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1cb15-109">**VT\_UI4**</span></span> | <span data-ttu-id="1cb15-110">A profundidade de bits da imagem.</span><span class="sxs-lookup"><span data-stu-id="1cb15-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="1cb15-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ status corrigido da cor da imagem WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="1cb15-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1cb15-112">**VT\_UI4**</span></span> | <span data-ttu-id="1cb15-113">Uma enumeração de [**\_ \_ \_ \_ valores de status corrigido de cor WPD**](wpd-color-corrected-status-values.md) que especifica se o arquivo foi corrigido por cores. Isso impede que vários dispositivos corrijam automaticamente a imagem durante o pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="1cb15-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="1cb15-114">**\_ \_ status cortado da imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="1cb15-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1cb15-115">**VT\_UI4**</span></span> | <span data-ttu-id="1cb15-116">Uma enumeração de [**\_ \_ \_ valores de status cortados WPD**](wpd-cropped-status-values.md) que especifica se o arquivo foi cortado. Isso impede que vários dispositivos cortem automaticamente a imagem durante o pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="1cb15-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="1cb15-117">**\_índice de \_ exposição de imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="1cb15-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1cb15-118">**VT\_UI4**</span></span> | <span data-ttu-id="1cb15-119">Um valor que identifica as configurações de velocidade do filme quando esta imagem foi capturada. As configurações correspondem às designações ISO de ASA/DIN.</span><span class="sxs-lookup"><span data-stu-id="1cb15-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="1cb15-120">Normalmente, um dispositivo dá suporte a valores enumerados discretos, mas o controle contínuo sobre um intervalo é possível.</span><span class="sxs-lookup"><span data-stu-id="1cb15-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="1cb15-121">Um valor de 0xFFFFFFFF corresponde à configuração ISO automática.</span><span class="sxs-lookup"><span data-stu-id="1cb15-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="1cb15-122">**\_tempo de \_ exposição da imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="1cb15-123">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1cb15-123">**VT\_UI4**</span></span> | <span data-ttu-id="1cb15-124">Identifica a velocidade do obturador do dispositivo quando esta imagem foi capturada. As unidades estão em segundos dimensionadas por 10000.</span><span class="sxs-lookup"><span data-stu-id="1cb15-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="1cb15-125">**\_FNUMBER de imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="1cb15-126">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1cb15-126">**VT\_UI4**</span></span> | <span data-ttu-id="1cb15-127">Identifica a configuração de abertura da lente quando esta imagem foi capturada. As unidades são iguais ao número f dimensionado por 100.</span><span class="sxs-lookup"><span data-stu-id="1cb15-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="1cb15-128">**\_ \_ resolução horizontal de imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="1cb15-129">**R8 de VT \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-129">**VT\_R8**</span></span>  | <span data-ttu-id="1cb15-130">Indica a resolução horizontal de uma imagem, em pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="1cb15-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1cb15-131">**\_ \_ resolução vertical da imagem WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="1cb15-132">**R8 de VT \_**</span><span class="sxs-lookup"><span data-stu-id="1cb15-132">**VT\_R8**</span></span>  | <span data-ttu-id="1cb15-133">Indica a resolução vertical de uma imagem, em pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="1cb15-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="1cb15-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cb15-134">Requirements</span></span>



| <span data-ttu-id="1cb15-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cb15-135">Requirement</span></span> | <span data-ttu-id="1cb15-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1cb15-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb15-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cb15-137">Header</span></span><br/> | <dl> <span data-ttu-id="1cb15-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb15-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb15-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cb15-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb15-140">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="1cb15-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




