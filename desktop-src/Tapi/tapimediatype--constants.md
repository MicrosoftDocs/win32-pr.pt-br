---
description: As constantes do tipo de mídia são definidas abaixo.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Constantes de TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782897"
---
# <a name="tapimediatype_-constants"></a>\_Constantes TAPIMEDIATYPE

Os seguintes tipos de mídia estão definidos:



| Constante/valor                                                                                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_**</dt> <dt>0X8</dt> de áudio </dl>                    | Um fluxo de mídia de áudio que está entrando ou saindo do computador. Um fluxo de mídia inserido normalmente seria reproduzido em alto-falantes ou enviado a um dispositivo de monofone, e um fluxo de saída normalmente seria capturado por meio de um microfone ou dispositivo de monofone.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_**</dt> <dt>0X8000</dt> de vídeo </dl>                 | Um fluxo de mídia de vídeo que está entrando ou saindo do computador. Um fluxo de mídia inserido normalmente seria renderizado em uma janela de vídeo e um fluxo de mídia de saída normalmente seria capturado com uma câmera de vídeo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ Datamodens**</dt> <dt>0x10</dt> </dl>       | Um fluxo de mídia de dados associado a um modem de dados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Um fluxo de mídia de dados que está associado a um fax de protocolo G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_ MULTITRACK**</dt> <dt>0x10000</dt> </dl> | Um fluxo está em um terminal multitrack.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**\_ \_ Fluxo único de MediaType RTP \_**</dt> </dl>     | Esse GUID é usado entre um terminal fornecido pelo aplicativo e o fluxo do MSP. Se o PIN do terminal der suporte a esse tipo de mídia, o fluxo irá trocar dados brutos do RTP pelo terminal. Esse modo é suportado apenas pelos fluxos de vídeo no H323 MSP e no IPConf MSP para Windows 2000 SP1 ou superior.<br/> **Cabeçalho:** Declarado em ipmsp. h. O cabeçalho ipmsp. h não está disponível no no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                              |
| parâmetro<br/>       | <dl> <dt>Tapi3. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITQOSEvent:: obter \_ MediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat:: obter \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::p UT \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo:: obter \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport:: obter \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport:: createterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

