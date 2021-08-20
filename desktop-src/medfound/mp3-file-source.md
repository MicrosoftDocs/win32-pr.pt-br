---
description: A fonte de arquivo MP3 analisa os arquivos MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origem de arquivo MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c95e54319fb189fa3bcc366b554b4d6555b2f4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479832"
---
# <a name="mp3-file-source"></a>Origem de arquivo MP3

A fonte de arquivo MP3 analisa os arquivos MP3.

A origem do arquivo MP3 gera buffers que contêm quadros de áudio MPEG-1. Ele não decodifica o áudio.

## <a name="file-extensions-and-mime-types"></a>Extensões de arquivo e tipos MIME

A origem do arquivo MP3 é a fonte de mídia padrão para a seguinte extensão de nome de arquivo:

-   .mp3

Também é a fonte de mídia padrão para os tipos MIME a seguir.

-   áudio/MPEG
-   áudio/x-mp3
-   áudio/x-MPEG

## <a name="media-types"></a>Tipos de mídia

O tipo de mídia oferecido pela origem do arquivo MP3 contém os seguintes atributos.



| Atributo                                                                                    | Descrição                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                                    | Igual a **MFMediaType \_ Audio**.                                                                                                                   |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | Igual a **MFAudioFormat \_ mp3** ou **MFAudioFormat \_ MPEG**.                                                                                        |
| [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Número médio de bytes por segundo.                                                                                                                |
| [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)             | Igual a 1.                                                                                                                                        |
| [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | Número de canais de áudio.                                                                                                                          |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)      | Número de amostras de áudio por segundo.                                                                                                                |
| [**dados de usuário do MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                                      | Contém a parte de uma estrutura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) que aparece após o membro **WFX** da estrutura. |



 

## <a name="interfaces"></a>Interfaces

A origem do arquivo MP3 expõe as seguintes interfaces por meio de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Além disso, ele expõe as seguintes interfaces por meio de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):




| GUID de Serviço | Interface | 
|--------------|-----------|
| <strong>MF_METADATA_PROVIDER_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a> | 
| <strong>MF_PROPERTY_HANDLER_SERVICE</strong> | <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a><blockquote>[!Note]<br />Consulte <a href="shell-metadata-providers.md">provedores de metadados do Shell</a>.</blockquote><br /><br /> | 
| <strong>MF_RATE_CONTROL_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a> | 
| <strong>MF_RATE_CONTROL_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fontes de mídia e coletores](media-sources-and-sinks.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
