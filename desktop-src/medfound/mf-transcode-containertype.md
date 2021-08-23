---
description: Especifica o tipo de contêiner de um arquivo codificado.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: MF_TRANSCODE_CONTAINERTYPE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c56b0332c43f10fa61b34f47191e3946a4813b3670249a8d858317067c38d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604686"
---
# <a name="mf_transcode_containertype-attribute"></a>Atributo MF \_ TRANSCODE \_ CONTAINERTYPE

Especifica o tipo de contêiner de um arquivo codificado. Os tipos de contêiner são suportados por Media Foundation.

## <a name="data-type"></a>Tipo de dados

**GUID**

Os valores possíveis para os tipos de contêiner fornecidos Media Foundation são descritos na tabela a seguir.



| Valor                                                                                                                                                                                                                                                                 | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**MFTranscodeContainerType \_ ASF**</dt> </dl>             | Contêiner de arquivo ASF.<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG4**</dt> </dl>     | Contêiner de arquivo MP4.<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**MFTranscodeContainerType \_ MP3**</dt> </dl>             | Contêiner de arquivo MP3.<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**MFTranscodeContainerType \_ 3GP**</dt> </dl>             | Contêiner de arquivo de 3GP. <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**MFTranscodeContainerType \_ AC3**</dt> </dl>             | Contêiner de arquivo AC3. <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**MFTranscodeContainerType \_ ADTS**</dt> </dl>         | Contêiner de arquivo do ADTS. <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG2**</dt> </dl>     | Contêiner de arquivo MPEG2. <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ FMPEG4**</dt> </dl> | Contêiner de arquivo FMPEG4. <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**MFTranscodeContainerType \_ WAVE**</dt> </dl>         | Contêiner de arquivo WAVE.<br/> Com suporte no Windows 8.1 e posterior.<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**MFTranscodeContainerType \_ AVI**</dt> </dl>             | Contêiner de arquivo AVI.<br/> Com suporte no Windows 8.1 e posterior.<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**MFTranscodeContainerType \_ AMR**</dt> </dl>             | Contêiner de arquivo AMR. <br/>                                                    |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetGUID.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)

Para definir esse atributo, chame [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentários

Esse atributo é usado com o recurso Transcódigo Rápido e o objeto de autor do sink.

A constante GUID para esse atributo é exportada de mfuuid.lib.

### <a name="fast-transcode"></a>Fast Transcode

O aplicativo deve definir o atributo de contêiner no perfil de transcódigo antes de criar a topologia de transcódigo. O construtor de topologia analisa esse atributo e carrega o sink de mídia apropriado no pipeline. Para obter mais informações, consulte estes tópicos:

-   [**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>Sink Writer

Esse atributo pode ser usado para configurar o tipo de contêiner de arquivo para o sink writer. Para obter mais informações, consulte [Sink Writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificar](transcode-api.md)
</dt> </dl>

 

 




