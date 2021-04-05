---
title: Alteração do dispositivo do ponteiro
description: Valores que podem ser passados no parâmetro wParam da mensagem de WM_POINTERDEVICECHANGE.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918819"
---
# <a name="pointer-device-change"></a><span data-ttu-id="b48c1-103">Alteração do dispositivo do ponteiro</span><span class="sxs-lookup"><span data-stu-id="b48c1-103">Pointer Device Change</span></span>

<span data-ttu-id="b48c1-104">Valores que podem ser passados no parâmetro *wParam* da mensagem de [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="b48c1-104">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="b48c1-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="b48c1-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-106">0x001</span><span class="sxs-lookup"><span data-stu-id="b48c1-106">0x001</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-107">Um novo dispositivo está anexado.</span><span class="sxs-lookup"><span data-stu-id="b48c1-107">A new device is attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span><span class="sxs-lookup"><span data-stu-id="b48c1-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-109">0x002</span><span class="sxs-lookup"><span data-stu-id="b48c1-109">0x002</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-110">Um dispositivo foi desanexado.</span><span class="sxs-lookup"><span data-stu-id="b48c1-110">A device has been detached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span><span class="sxs-lookup"><span data-stu-id="b48c1-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-112">0x004</span><span class="sxs-lookup"><span data-stu-id="b48c1-112">0x004</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-113">Orientação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b48c1-113">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span><span class="sxs-lookup"><span data-stu-id="b48c1-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-115">0x008</span><span class="sxs-lookup"><span data-stu-id="b48c1-115">0x008</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-116">Orientação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b48c1-116">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span><span class="sxs-lookup"><span data-stu-id="b48c1-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-118">0x010</span><span class="sxs-lookup"><span data-stu-id="b48c1-118">0x010</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-119">Orientação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b48c1-119">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span><span class="sxs-lookup"><span data-stu-id="b48c1-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-121">0x020</span><span class="sxs-lookup"><span data-stu-id="b48c1-121">0x020</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-122">Orientação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b48c1-122">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b48c1-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-124">0x040</span><span class="sxs-lookup"><span data-stu-id="b48c1-124">0x040</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-125">O modo de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="b48c1-125">The default display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span><span class="sxs-lookup"><span data-stu-id="b48c1-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-127">0x080</span><span class="sxs-lookup"><span data-stu-id="b48c1-127">0x080</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-128">Modo de exibição centralizado.</span><span class="sxs-lookup"><span data-stu-id="b48c1-128">Centered display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="b48c1-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-130">0x100</span><span class="sxs-lookup"><span data-stu-id="b48c1-130">0x100</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-131">A alteração em Exibir para o mapeamento de digitalizador.</span><span class="sxs-lookup"><span data-stu-id="b48c1-131">The change in display to digitizer mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span><span class="sxs-lookup"><span data-stu-id="b48c1-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-133">0x200</span><span class="sxs-lookup"><span data-stu-id="b48c1-133">0x200</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-134">Resolução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b48c1-134">Display resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span><span class="sxs-lookup"><span data-stu-id="b48c1-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-136">0x400</span><span class="sxs-lookup"><span data-stu-id="b48c1-136">0x400</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-137">A origem de exibição.</span><span class="sxs-lookup"><span data-stu-id="b48c1-137">The display origin.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b48c1-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="b48c1-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48c1-139">0x800</span><span class="sxs-lookup"><span data-stu-id="b48c1-139">0x800</span></span>
</dt> <dt>



<span data-ttu-id="b48c1-140">A taxa de proporção de exibição.</span><span class="sxs-lookup"><span data-stu-id="b48c1-140">The display aspect ratio.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b48c1-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b48c1-141">Requirements</span></span>



| <span data-ttu-id="b48c1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b48c1-142">Requirement</span></span> | <span data-ttu-id="b48c1-143">Valor</span><span class="sxs-lookup"><span data-stu-id="b48c1-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b48c1-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b48c1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b48c1-145">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-145">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b48c1-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b48c1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b48c1-147">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b48c1-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b48c1-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="b48c1-149"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="b48c1-149"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48c1-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="b48c1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48c1-151">Constantes</span><span class="sxs-lookup"><span data-stu-id="b48c1-151">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="b48c1-152">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="b48c1-152">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





