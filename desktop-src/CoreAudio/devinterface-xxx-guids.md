---
description: Os \_ GUIDs do DEVINTERFACE xxx são usados para representar os GUIDs para interfaces de dispositivo.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: GUIDs de DEVINTERFACE_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752796"
---
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="366c2-103">\_GUIDs do DEVINTERFACE xxx</span><span class="sxs-lookup"><span data-stu-id="366c2-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="366c2-104">Os \_ GUIDs do DEVINTERFACE xxx são usados para representar os GUIDs para interfaces de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="366c2-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="366c2-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_captura de áudio DEVINTERFACE \_**</span><span class="sxs-lookup"><span data-stu-id="366c2-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="366c2-106">Especifica a cadeia de caracteres de consulta usada para enumerar todos os dispositivos de captura de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="366c2-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="366c2-107">Esse valor é retornado por [**MediaDevice:: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span><span class="sxs-lookup"><span data-stu-id="366c2-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="366c2-108">Passar esse valor para [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) ativa a interface solicitada no dispositivo de captura de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="366c2-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="366c2-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_renderização de áudio DEVINTERFACE \_**</span><span class="sxs-lookup"><span data-stu-id="366c2-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="366c2-110">Especifica a cadeia de caracteres de consulta usada para enumerar todos os dispositivos de processamento de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="366c2-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="366c2-111">Esse valor é retornado por [**MediaDevice:: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span><span class="sxs-lookup"><span data-stu-id="366c2-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="366c2-112">Passar esse valor para [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) ativa a interface solicitada no dispositivo de processamento de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="366c2-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="366c2-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_entrada MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="366c2-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="366c2-114">Especifica a cadeia de caracteres de consulta usada para enumerar todos os objetos [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) no sistema.</span><span class="sxs-lookup"><span data-stu-id="366c2-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="366c2-115">Esse valor é retornado por [**MidiInPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="366c2-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="366c2-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_saída de Midi DEVINTERFACE \_**</span><span class="sxs-lookup"><span data-stu-id="366c2-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="366c2-117">Especifica a cadeia de caracteres de consulta usada para enumerar todos os objetos [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) no sistema.</span><span class="sxs-lookup"><span data-stu-id="366c2-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="366c2-118">Esse valor é retornado por [**MidiOutPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="366c2-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="366c2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="366c2-119">Requirements</span></span>



| <span data-ttu-id="366c2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="366c2-120">Requirement</span></span> | <span data-ttu-id="366c2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="366c2-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="366c2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="366c2-122">Header</span></span><br/> | <dl> <span data-ttu-id="366c2-123"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="366c2-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 

