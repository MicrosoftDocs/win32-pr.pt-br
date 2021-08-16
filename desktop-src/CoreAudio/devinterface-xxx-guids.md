---
description: Os \_ GUIDs do DEVINTERFACE xxx são usados para representar os GUIDs para interfaces de dispositivo.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: GUIDs de DEVINTERFACE_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cef6a105ed8e34519a2ca0a06d9d4f43a7aa91495fae9f54eedfa44d79b043c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406789"
---
# <a name="devinterface_xxx-guids"></a>\_GUIDs do DEVINTERFACE xxx

Os \_ GUIDs do DEVINTERFACE xxx são usados para representar os GUIDs para interfaces de dispositivo.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_captura de áudio DEVINTERFACE \_**
</dt> <dd> <dl> <dt>



Especifica a cadeia de caracteres de consulta usada para enumerar todos os dispositivos de captura de áudio no sistema. Esse valor é retornado por [**MediaDevice:: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).

Passar esse valor para [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) ativa a interface solicitada no dispositivo de captura de áudio padrão.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_renderização de áudio DEVINTERFACE \_**
</dt> <dd> <dl> <dt>



Especifica a cadeia de caracteres de consulta usada para enumerar todos os dispositivos de processamento de áudio no sistema. Esse valor é retornado por [**MediaDevice:: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).

Passar esse valor para [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) ativa a interface solicitada no dispositivo de processamento de áudio padrão.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_entrada MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Especifica a cadeia de caracteres de consulta usada para enumerar todos os objetos [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) no sistema. Esse valor é retornado por [**MidiInPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_saída de Midi DEVINTERFACE \_**
</dt> <dd> <dl> <dt>



Especifica a cadeia de caracteres de consulta usada para enumerar todos os objetos [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) no sistema. Esse valor é retornado por [**MidiOutPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



 

