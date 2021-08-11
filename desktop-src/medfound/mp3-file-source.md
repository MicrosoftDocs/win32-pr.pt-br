---
description: A origem do arquivo MP3 analisado arquivos MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origem do arquivo MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b5649f1bdbc9d9b3dfa0af2f04878dfa64852af85ff8e829d4d2d4c4d20d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240101"
---
# <a name="mp3-file-source"></a>Origem do arquivo MP3

A origem do arquivo MP3 analisado arquivos MP3.

A origem do arquivo MP3 saída buffers que contêm quadros de áudio MPEG-1. Ele não decodifica o áudio.

## <a name="file-extensions-and-mime-types"></a>Extensões de arquivo e tipos MIME

A origem do arquivo MP3 é a fonte de mídia padrão para a seguinte extensão de nome de arquivo:

-   .mp3

Também é a fonte de mídia padrão para os seguintes tipos MIME.

-   audio/mpeg
-   audio/x-mp3
-   audio/x-mpeg

## <a name="media-types"></a>Tipos de mídia

O tipo de mídia oferecido pela origem do arquivo MP3 contém os atributos a seguir.



| Atributo                                                                                    | Descrição                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                                    | Igual a **MFMediaType \_ Audio**.                                                                                                                   |
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)                                           | Igual a **MFAudioFormat \_ MP3** ou **MFAudioFormat \_ MPEG.**                                                                                        |
| [**BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Número médio de bytes por segundo.                                                                                                                |
| [**ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT**](mf-mt-audio-block-alignment-attribute.md)             | Igual a 1.                                                                                                                                        |
| [**CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | Número de canais de áudio.                                                                                                                          |
| [**AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)      | Número de amostras de áudio por segundo.                                                                                                                |
| [**MF \_ MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md)                                      | Contém a parte de uma [**estrutura MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) que aparece após o **membro wfx** da estrutura. |



 

## <a name="interfaces"></a>Interfaces

A origem do arquivo MP3 expõe as seguintes interfaces por [**meio de QueryInterface:**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Além disso, ele expõe as seguintes interfaces por meio [**de IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID de Serviço</th>
<th>Interface</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>Ipropertystore</strong></a>
<blockquote>
[!Note]<br />
Consulte <a href="shell-metadata-providers.md">Provedores de Metadados do Shell.</a>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Fontes de mídia e sinks](media-sources-and-sinks.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Resolvedor de Origem](source-resolver.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
