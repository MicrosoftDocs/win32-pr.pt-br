---
description: Especifica o tipo de contêiner de um arquivo codificado.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: Atributo MF_TRANSCODE_CONTAINERTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781208"
---
# <a name="mf_transcode_containertype-attribute"></a>\_Atributo ContainerType de transcodificação MF \_

Especifica o tipo de contêiner de um arquivo codificado. Os tipos de contêiner têm suporte pelo Media Foundation.

## <a name="data-type"></a>Tipo de dados

**GUID**

Os valores possíveis para os tipos de contêiner fornecidos pelo Media Foundation são descritos na tabela a seguir.



| Valor                                                                                                                                                                                                                                                                 | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**MFTranscodeContainerType \_ ASF**</dt> </dl>             | Contêiner de arquivo ASF.<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG4**</dt> </dl>     | Contêiner de arquivo MP4.<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**MFTranscodeContainerType \_ mp3**</dt> </dl>             | Contêiner de arquivo MP3.<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**MFTranscodeContainerType \_ 3GP**</dt> </dl>             | contêiner de arquivos 3GP. <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**MFTranscodeContainerType \_ AC3**</dt> </dl>             | Contêiner de arquivos AC3. <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**MFTranscodeContainerType \_ ADTS**</dt> </dl>         | Contêiner de arquivos ADTS. <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG2**</dt> </dl>     | Contêiner de arquivo MPEG2. <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ FMPEG4**</dt> </dl> | Contêiner de arquivos FMPEG4. <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**\_Onda MFTranscodeContainerType**</dt> </dl>         | Contêiner de arquivo WAVE.<br/> Com suporte no Windows 8.1 e posterior.<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**\_AVI MFTranscodeContainerType**</dt> </dl>             | Contêiner de arquivo AVI.<br/> Com suporte no Windows 8.1 e posterior.<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**MFTranscodeContainerType \_ Amr**</dt> </dl>             | Contêiner de arquivo AMR. <br/>                                                    |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentários

Esse atributo é usado com o recurso de transcodificação rápida e o objeto gravador do coletor.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

### <a name="fast-transcode"></a>Transcodificação rápida

O aplicativo deve definir o atributo de contêiner no perfil de transcodificação antes de criar a topologia de transcodificação. O construtor de topologias analisa esse atributo e carrega o coletor de mídia apropriado no pipeline. Para mais informações, consulte os seguintes tópicos:

-   [**IMFTranscodeProfile:: getcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**IMFTranscodeProfile:: setcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>Gravador do coletor

Esse atributo pode ser usado para configurar o tipo de contêiner de arquivo para o gravador de coletor. Para obter mais informações, consulte [atributos do gravador do coletor](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificação](transcode-api.md)
</dt> </dl>

 

 




