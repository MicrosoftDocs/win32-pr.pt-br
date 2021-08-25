---
description: As constantes de tipo de mídia são definidas abaixo.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: TAPIMEDIATYPE_ constantes (Tapi3.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a702f5a061629f3fd8daa5ad742c65af12c43bbd92eec6896b143e4bd6a403c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866876"
---
# <a name="tapimediatype_-constants"></a>Constantes TAPIMEDIATYPE \_

Os seguintes tipos de mídia são definidos:



| Constante/valor                                                                                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_ AUDIO**</dt> <dt>0x8</dt> </dl>                    | Um fluxo de mídia de áudio que está entrando ou saindo do computador. Um fluxo de mídia de entrada normalmente seria tocado em alto-falantes ou enviado para um dispositivo de dispositivo de dispositivo e um fluxo de saída normalmente seria capturado por meio de um microfone ou dispositivo de handset.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ VÍDEO**</dt> <dt>0x8000</dt> </dl>                 | Um fluxo de mídia de vídeo que está entrando ou saindo do computador. Um fluxo de mídia de entrada normalmente seria renderizado em uma janela de vídeo e um fluxo de mídia de saída normalmente seria capturado com uma câmera de vídeo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ DataMODEM**</dt> <dt>0x10</dt> </dl>       | Um fluxo de mídia de dados associado a um modem de dados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Um fluxo de mídia de dados associado a um fax de protocolo G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_ MULTITRACK**</dt> <dt>0x10000</dt> </dl> | Um fluxo está em um terminal multitrack.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**Fluxo único \_ do MEDIATYPE RTP \_ \_**</dt> </dl>     | Esse GUID é usado entre um terminal fornecido pelo aplicativo e o fluxo do MSP. Se o pino do terminal dá suporte a esse tipo de mídia, o fluxo trocará dados RTP brutos com o terminal. Esse modo tem suporte apenas pelos fluxos de vídeo no MSP H323 e no MSP ipConf para Windows 2000 SP1 ou superior.<br/> **Header:** Declarado em ipmsp.h. O header ipmsp.h não está disponível no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                              |
| Cabeçalho<br/>       | <dl> <dt>Tapi3.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITQOSEvent::get \_ MediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat::get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::put \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport::get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

