---
description: As constantes do suporte de hardware do ENDPOINT \_ \_ \_ xxx são sinalizadores de suporte de hardware para um dispositivo de ponto de extremidade de áudio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Constantes de ENDPOINT_HARDWARE_SUPPORT_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089629"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="0ca97-103">Constantes de suporte de hardware de ponto de extremidade \_ \_ \_ xxx</span><span class="sxs-lookup"><span data-stu-id="0ca97-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="0ca97-104">As constantes do suporte de hardware do ENDPOINT \_ \_ \_ xxx são sinalizadores de suporte de hardware para um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="0ca97-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="0ca97-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="0ca97-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="0ca97-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ca97-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="0ca97-107"><dt>**Ponto de extremidade \_ \_ \_ Volume de suporte de hardware**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0ca97-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0ca97-108">O dispositivo de ponto de extremidade de áudio dá suporte a um controle de volume de hardware.</span><span class="sxs-lookup"><span data-stu-id="0ca97-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="0ca97-109"><dt>**Ponto de extremidade \_ \_Ativar/ \_ desativar suporte de hardware**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="0ca97-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="0ca97-110">O dispositivo de ponto de extremidade de áudio dá suporte a um controle de mudo de hardware.</span><span class="sxs-lookup"><span data-stu-id="0ca97-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="0ca97-111"><dt>**Ponto de extremidade \_ \_ \_ Medidor de suporte de hardware**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="0ca97-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="0ca97-112">O dispositivo de ponto de extremidade de áudio dá suporte a um medidor de pico de hardware.</span><span class="sxs-lookup"><span data-stu-id="0ca97-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="0ca97-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ca97-113">Remarks</span></span>

<span data-ttu-id="0ca97-114">Os métodos [**IAudioEndpointVolume:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) e [**IAudioMeterInformation:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usam as constantes de suporte de hardware de ponto de extremidade \_ \_ \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="0ca97-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="0ca97-115">Uma máscara de suporte de hardware indica quais funções um dispositivo de ponto de extremidade de áudio implementa no hardware.</span><span class="sxs-lookup"><span data-stu-id="0ca97-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="0ca97-116">A máscara pode ser 0 ou a combinação bit-a-OR de uma ou mais constantes de suporte de hardware de ponto de extremidade \_ \_ \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="0ca97-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="0ca97-117">Se um bit que corresponde a uma constante de suporte de hardware de ponto de extremidade em particular \_ \_ \_ for definido na máscara, o significado é que a função representada por essa constante é implementada no hardware pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ca97-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca97-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ca97-118">Requirements</span></span>



| <span data-ttu-id="0ca97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ca97-119">Requirement</span></span> | <span data-ttu-id="0ca97-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0ca97-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca97-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ca97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca97-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ca97-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0ca97-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ca97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca97-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ca97-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0ca97-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ca97-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca97-126"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca97-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca97-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ca97-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca97-128">Principais constantes de áudio</span><span class="sxs-lookup"><span data-stu-id="0ca97-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="0ca97-129">**IAudioEndpointVolume::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="0ca97-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="0ca97-130">**IAudioMeterInformation::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="0ca97-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




