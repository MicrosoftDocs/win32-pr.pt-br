---
title: WMDM_FORMATCODE enumeração
description: O tipo de enumeração WMDM FORMATCODE define uma lista de códigos de formato que descrevem os tipos de conteúdo transferidos de e para \_ um dispositivo.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b09a388926a0f5fc11e24fc17fe4693b710e04aa321202e9cf31890d60d6642
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862906"
---
# <a name="wmdm_formatcode-enumeration"></a>Enumeração WMDM \_ FORMATCODE

O **tipo de enumeração WMDM \_ FORMATCODE** define uma lista de códigos de formato que descrevem os tipos de conteúdo transferidos de e para um dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ NOTUSED**
</dt> <dd>

Nenhum código de formato é usado.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**
</dt> <dd>

Código de formato que pode ser usado para consultar todas as imagens.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM \_ FORMATCODE \_ INDEFINIDO**
</dt> <dd>

Código de formato usado para consultar todos os objetos indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**ASSOCIAÇÃO WMDM \_ FORMATCODE \_**
</dt> <dd>

Código de formato usado para definir um link entre dois objetos.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM \_ FORMATCODE \_ SCRIPT**
</dt> <dd>

Formatar código para um arquivo de script.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**EXECUTÁVEL WMDM \_ FORMATCODE \_**
</dt> <dd>

Formatar código para um arquivo executável.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM \_ FORMATCODE \_ TEXT**
</dt> <dd>

Formatar código para um arquivo de texto.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ FORMATCODE \_ HTML**
</dt> <dd>

Formatar código para um arquivo HTML.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**
</dt> <dd>

Código de formato usado para representar o formato de ordem de impressão digital.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**
</dt> <dd>

Código de formato usado para representar o formato de arquivo de intercâmbio de áudio.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ WAVE**
</dt> <dd>

Código de formato usado para um arquivo WAV.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ FORMATCODE \_ MP3**
</dt> <dd>

Código de formato usado para um arquivo MP3.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ FORMATCODE \_ AVI**
</dt> <dd>

Código de formato usado para um arquivo AVI.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**
</dt> <dd>

Código de formato usado para um arquivo MPEG.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**
</dt> <dd>

Código de formato usado para representar um arquivo ASF (Advanced Systems Format).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ RESERVADO \_ PRIMEIRO**
</dt> <dd>

Código de formato que é o primeiro em um intervalo reservado para PTP (Picture Transfer Protocol).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ RESERVADO POR \_ ÚLTIMO**
</dt> <dd>

Formate o código que é o último em um intervalo reservado para PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**IMAGEM DO WMDM \_ FORMATCODE \_ \_ INDEFINIDA**
</dt> <dd>

Código de formato usado para representar e imagem de um tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ EXIF**
</dt> <dd>

Formatar código para um arquivo EXIF. Também usado para imagens JPEG não cobertas por WMDM \_ FORMATCODE \_ IMAGE \_ JP2 ou WMDM \_ FORMATCODE \_ IMAGE \_ JPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ TIFFEP**
</dt> <dd>

Código de formato usado para imagens do tipo Formato de Arquivo de Imagem Marcada para Fotografia Eletrônica (TIFF/EP)

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ FLASHPIX**
</dt> <dd>

Código de formato para um arquivo do tipo FPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ BMP**
</dt> <dd>

Formatar código para um arquivo do tipo BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ CIFF**
</dt> <dd>

Formate o código para uma imagem no formato de arquivo de imagem da câmera.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ GIF**
</dt> <dd>

Formatar código para um arquivo GIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ JFIF**
</dt> <dd>

Formatar código para um arquivo do tipo JFIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ PCD**
</dt> <dd>

Formate o código para uma imagem do tipo cd de foto.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ PICT**
</dt> <dd>

Formate o código para uma imagem do tipo PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ PNG**
</dt> <dd>

Formatar código para uma imagem do tipo PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ TIFF**
</dt> <dd>

Formate o código para um arquivo do tipo TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ TIFFIT**
</dt> <dd>

Formate o código para uma imagem do tipo Formato de Arquivo de Imagem Marcada com tecnologia de imagem.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ JP2**
</dt> <dd>

Formate o código para uma imagem jpeg200.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**IMAGEM JPX DO WMDM \_ \_ FORMATCODE \_**
</dt> <dd>

Formate o código para uma imagem criada em JPEG200, usando o registro estendido de imagem ainda. A extensão de nome de arquivo geralmente é .jpf ou .jpx.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**IMAGEM DO WMDM \_ FORMATCODE \_ RESERVADA \_ \_ PRIMEIRO**
</dt> <dd>

Formate o código que é o primeiro em um intervalo reservado para uma referência de imagem no PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ RESERVED \_ LAST**
</dt> <dd>

Código de formato que é o último em um intervalo reservado para uma referência de imagem no PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**
</dt> <dd>

Formatar código quando o firmware for indefinido.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP** 
</dt> <dd>

Formate o código para uma imagem bitmap de protocolo de aplicativo sem fio (.wbmp).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR** 
</dt> <dd>

Formatar código para uma imagem de foto HD

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**FORMATO WMDMCODE \_ \_ WINDOWSIMAGEFORMAT**
</dt> <dd>

Formate o código para Windows formato de imagem.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**
</dt> <dd>

Formatar código para um arquivo de áudio de tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**
</dt> <dd>

Formate o código para um Windows WMA (Media Audio).

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**FORMATCODE \_ OGG DO WMDM \_**
</dt> <dd>

Formatar código para um arquivo de áudio codificado em Vorbis em um contêiner Ogg.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**
</dt> <dd>

Formate o código para um arquivo AAC (Codificação de Áudio Avançado).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**FORMATCODE \_ WMDM \_ UDÍVEL**
</dt> <dd>

Formatar código para um arquivo Udível.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**
</dt> <dd>

Formate o código para um arquivo DOC (Free Lossless Audio Codec).

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP** 
</dt> <dd>

Formate o código para um arquivo codec de QCELP (Previsão Linear Animada pelo Código Qualcomm).

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ FORMATCODE \_ AMR** 
</dt> <dd>

Formate o código para um arquivo de codec de áudio de várias taxas (AMR) adaptável.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**\_FORMATCODE WMDM \_ UNDEFINEDVIDEO**
</dt> <dd>

Formate o código de um arquivo de vídeo com um tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**
</dt> <dd>

formate o código de um arquivo de vídeo de mídia Windows (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**FORMATCODE do WMDM \_ \_**
</dt> <dd>

Formatar código para um arquivo MP4.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**\_FORMATCODE WMDM \_ MP2**
</dt> <dd>

Formate o código de um arquivo MP2.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3G2** 
</dt> <dd>

Código de formato para um formato de contêiner multimídia 3G2 (3GPP2). Um arquivo desse tipo pode conter áudio, vídeo ou texto.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD** 
</dt> <dd>

Formate o código de um arquivo de vídeo AVCHD (codificação de vídeo avançada alta definição).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSCTS** 
</dt> <dd>

Código de formato do padrão de formato ATSCTS (Comitê de sistemas de televisão avançado).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ FORMATCODE \_ DVBTS** 
</dt> <dd>

Formate o código para um vídeo MPEG-2 e MPEG-1 Layer II ou AC-3, áudio em um fluxo de transporte MPEG-2 em conformidade com DVB.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ undefinecollection**
</dt> <dd>

Código de formato para uma coleção de um tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTMULTIMEDIAALBUM**
</dt> <dd>

Formate o código de um álbum de multimídia em que o objeto contém as propriedades de um álbum de multimídia e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTIMAGEALBUM**
</dt> <dd>

Formate o código de um álbum de imagem em que o objeto contém as propriedades de um álbum de imagem e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTAUDIOALBUM**
</dt> <dd>

Formate o código de um álbum de áudio em que o objeto contém as propriedades de um álbum de áudio e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTVIDEOALBUM**
</dt> <dd>

Formate o código de um álbum de vídeo em que o objeto contém as propriedades de um álbum de vídeo e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**\_FORMATCODE WMDM \_ ABSTRACTAUDIOVIDEOPLAYLIST**
</dt> <dd>

Formate o código de uma playlist de áudio/vídeo em que o objeto contém as propriedades de uma lista de reprodução de áudio/vídeo e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**\_FORMATCODE WMDM \_ ABSTRACTCONTACTGROUP**
</dt> <dd>

Formate o código de um grupo de contatos em que o objeto contém as propriedades de um grupo de contatos e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**\_FORMATCODE WMDM \_ ABSTRACTMESSAGEFOLDER**
</dt> <dd>

Formate o código de uma pasta de mensagens em que o objeto contém as propriedades de uma pasta de mensagens e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**\_FORMATCODE WMDM \_ ABSTRACTCHAPTEREDPRODUCTION**
</dt> <dd>

Formate o código para uma produção com capítulo em que o objeto contém as propriedades de uma produção com capítulo e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**\_FORMATCODE WMDM \_ WPLPLAYLIST**
</dt> <dd>

formatar código para uma lista de reprodução formatada com Windows formatação de lista de reprodução de mídia.

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**\_FORMATCODE WMDM \_ M3UPLAYLIST**
</dt> <dd>

Formate o código de uma playlist com formatação M3U.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**\_FORMATCODE WMDM \_ MPLPLAYLIST**
</dt> <dd>

Formate o código de uma playlist com formatação MPL.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**\_FORMATCODE WMDM \_ ASXPLAYLIST**
</dt> <dd>

Formate o código de uma playlist com formatação ASX.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**\_FORMATCODE WMDM \_ PLSPLAYLIST**
</dt> <dd>

Formate o código de uma playlist com formatação PLS.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**\_FORMATCODE WMDM \_ UNDEFINEDDOCUMENT**
</dt> <dd>

Formatar código para um documento de tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**\_FORMATCODE WMDM \_ ABSTRACTDOCUMENT**
</dt> <dd>

Formate o código de um documento em que o objeto contém as propriedades de um documento e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**\_XMLDOCUMENT de FORMATCODE do WMDM \_**
</dt> <dd>

Formatar código para um documento XML.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**\_FORMATCODE WMDM \_ MICROSOFTWORDDOCUMENT**
</dt> <dd>

formate o código de um documento Microsoft Word.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**\_FORMATCODE WMDM \_ MHTCOMPILEDHTMLDOCUMENT**
</dt> <dd>

Formate o código de um documento HTML compilado.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**\_FORMATCODE WMDM \_ MICROSOFTEXCELSPREADSHEET**
</dt> <dd>

formate o código de uma planilha Microsoft Excel.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**\_FORMATCODE WMDM \_ MICROSOFTPOWERPOINTDOCUMENT**
</dt> <dd>

código de formato de um documento do Microsoft PowerPoint.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**\_FORMATCODE WMDM \_ UNDEFINEDMESSAGE**
</dt> <dd>

Código de formato para uma mensagem de tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**\_FORMATCODE WMDM \_ ABSTRACTMESSAGE**
</dt> <dd>

Formate o código de uma mensagem em que o objeto contém as propriedades de uma mensagem e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**\_FORMATCODE WMDM \_ UNDEFINEDCONTACT**
</dt> <dd>

Formatar código para um contato de tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**\_FORMATCODE WMDM \_ ABSTRACTCONTACT**
</dt> <dd>

Formate o código de um contato em que o objeto contém as propriedades de um contato e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**\_FORMATCODE WMDM \_ VCARD2**
</dt> <dd>

Formate o código de um cartão eletrônico com a formatação de vCard versão 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**\_FORMATCODE WMDM \_ VCARD3**
</dt> <dd>

Formate o código de um cartão eletrônico com a formatação de vCard versão 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**\_FORMATCODE WMDM \_ UNDEFINEDCALENDARITEM**
</dt> <dd>

Formatar código para um item de calendário eletrônico de tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**\_FORMATCODE WMDM \_ ABSTRACTCALENDARITEM**
</dt> <dd>

Formate o código de um item de calendário em que o objeto contém as propriedades de um item de calendário e, opcionalmente, dados. Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**\_FORMATCODE WMDM \_ VCALENDAR1**
</dt> <dd>

Formate o código de um item de calendário eletrônico com a formatação do vCalendar versão 1.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**\_FORMATCODE WMDM \_ VCALENDAR2**
</dt> <dd>

Formate o código de um item de calendário eletrônico com a formatação do vCalendar versão 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**\_FORMATCODE WMDM \_ UNDEFINEDWINDOWSEXECUTABLE**
</dt> <dd>

código de formato para um executável baseado em Windows de tipo indefinido.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**conversão de mídia do WMDM \_ FORMATCODE \_ \_**
</dt> <dd>

Formate o código de um objeto de conversão de mídia.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_seção WMDM FORMATCODE \_**
</dt> <dd>

Formate o código para uma seção de dados contida em outro objeto.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A** 
</dt> <dd>

Código de formato para um formato de contêiner multimídia 3G2A (3GPP2A).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para descobrir os formatos com suporte de um dispositivo, um aplicativo pode usar [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para consultar a propriedade de dispositivo **g \_ wszWMDMFormatsSupported** .

Para descobrir recursos de dispositivo para um formato específico, um aplicativo pode chamar [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).

Um aplicativo pode definir o código de formato ao criar um armazenamento no dispositivo, incluindo a propriedade **g \_ wszWMDMFormatCode** nos metadados passados no parâmetro *pMetaData* de uma chamada para [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).

Um aplicativo pode consultar o código de formato de um armazenamento chamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) e recuperando a propriedade **g \_ wszWMDMFormatCode** .

Se o dispositivo der suporte à definição do código de formato após a criação do armazenamento, um aplicativo poderá usar [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) para definir a propriedade **g \_ wszWMDMFormatCode** . Alguns dispositivos podem não permitir a alteração do código de formato depois que o armazenamento é criado no dispositivo. Portanto, a definição dessa propriedade junto com os metadados passados em [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) é altamente recomendável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Constantes de metadados**](metadata-constants.md)
</dt> </dl>

 

 





