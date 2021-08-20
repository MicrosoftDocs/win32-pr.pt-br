---
description: A tabela a seguir descreve os principais tipos de mídia.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Tipos principais (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3764bffabb85b3b054fc7589d4eae9677adbc8835d0e4aa3029d31834eb887c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153238"
---
# <a name="major-types"></a>Tipos principais

A tabela a seguir descreve os principais tipos de mídia.



| GUID                                                                                                                                                                                                                                  | Descrição                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**AnalogAudio de MEDIATYPE \_**</dt> </dl>         | Áudio analógico.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**AnalogVideo de MEDIATYPE \_**</dt> </dl>         | Vídeo analógico.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**Áudio de MEDIATYPE \_**</dt> </dl>                                 | Sonoro. Consulte [subtipos de áudio](audio-subtypes.md).<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**AUXLine21Data de MEDIATYPE \_**</dt> </dl> | Linha 21 dados. Usado por legendas ocultas. Consulte [**linha 21 tipos de mídia**](line-21-media-types.md).<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**\_Arquivo MediaType**</dt> </dl>                                     | Grupo. (Obsoleto)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE \_ intercalado**</dt> </dl>         | Áudio e vídeo intercalados. Usado para vídeo digital (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**LMRT de MEDIATYPE \_**</dt> </dl>                                                                      | Obsoleto. Não use.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**MIDI de MEDIATYPE \_**</dt> </dl>                                     | Formato MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**MEDIATYPE \_ MPEG2 \_ PES**</dt> </dl>                                                      | Pacotes. MPEG-2 PES. Consulte [tipos de mídia MPEG-2](mpeg-2-media-types.md).<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**Seções de MEDIATYPE \_ MPEG2 \_**</dt> </dl>                                       | Dados da seção MPEG-2. Consulte [tipos de mídia MPEG-2](mpeg-2-media-types.md).<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**ScriptCommand de MEDIATYPE \_**</dt> </dl> | Data é um comando de script, usado por legendas ocultas.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**Fluxo de MEDIATYPE \_**</dt> </dl>                             | Fluxo de bytes sem carimbos de data/hora. Consulte [**subtipos de fluxo**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**Texto de MEDIATYPE \_**</dt> </dl>                                     | Text.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**Código de pamídia de MEDIATYPE \_**</dt> </dl>                     | Dados de código de pafica. observação: DirectShow não fornece nenhum filtro que ofereça suporte a esse tipo de mídia.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**\_fluxo de URL de MediaType \_**</dt> </dl>                                                   | Obsoleto. Não use.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**VBI de MEDIATYPE \_**</dt> </dl>                                                                         | Dados de intervalo em branco vertical (VBI) (para televisão). O mesmo que KSDATAFORMAT \_ tipo \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**Vídeo de MEDIATYPE \_**</dt> </dl>                                 | Vídeo. Consulte [subtipos de vídeo](video-subtypes.md).<br/>                                               |



## <a name="remarks"></a>Comentários

O GUID de subtipo define o formato. Para alguns formatos, o GUID do subtipo pode ser MEDIASUBTYPE \_ nenhum, o que significa que o formato não requer um subtipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 




