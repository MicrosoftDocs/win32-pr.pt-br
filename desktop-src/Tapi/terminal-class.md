---
description: Os GUIDs de classe de terminal identificam um terminal específico por recursos.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Classe terminal (Tapi3if. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d67d7668f9e4e16ad357408c8e9087fce870a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789840"
---
# <a name="terminal-class"></a>Classe terminal

Os GUIDs de classe de terminal identificam um terminal específico por recursos.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**\_FILEPLAYBACKTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminal de reprodução de arquivo.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**\_FILERECORDINGTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminal de gravação de arquivo.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**\_FILERECORDINGTRACK CLSID**
</dt> <dd> <dl> <dt>



Faixa de gravação de arquivo.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**\_HANDSETTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Aparelho telefônico.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**\_HEADSETTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Conjunto de cabeçalho.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**\_MEDIASTREAMTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminal de fluxo de mídia, criado dinamicamente.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**\_MICROPHONETERMINAL CLSID**
</dt> <dd> <dl> <dt>



Phone.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**\_SPEAKERPHONETERMINAL CLSID**
</dt> <dd> <dl> <dt>



Telefone do palestrante.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**\_SPEAKERSTERMINAL CLSID**
</dt> <dd> <dl> <dt>



falantes.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**\_VIDEOINPUTTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminal de entrada de vídeo.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**\_VIDEOWINDOWTERM CLSID**
</dt> <dd> <dl> <dt>



Janela de exibição de vídeo, criada dinamicamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

A versão do **BSTR** das classes terminal é designada principalmente para o uso de aplicativos Visual Basic. (Por exemplo, eles são retornados como os elementos da coleção obtidas com [**Get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses).)

-   Cadeia de caracteres de CLSID de BSTR \_ \_ HandsetTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ HeadsetTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ MediaStreamTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ MicrophoneTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ SpeakerphoneTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ SpeakersTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ VideoInputTerminal
-   Cadeia de caracteres de CLSID de BSTR \_ \_ VideoWindowTerm

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                |
| parâmetro<br/>       | <dl> <dt>Tapi3if. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITTerminalSupport:: createterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal:: obter \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

