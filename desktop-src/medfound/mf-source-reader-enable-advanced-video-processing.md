---
description: Habilita o processamento de vídeo avançado pelo leitor de origem, incluindo conversão de espaço de cor, desentrelaçamento, redimensionamento de vídeo e conversão de taxa de quadros.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Atributo MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501637"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>\_Leitor de origem MF \_ \_ habilitar atributo de \_ \_ processamento de vídeo avançado \_

Habilita o processamento de vídeo avançado pelo [leitor de origem](source-reader.md), incluindo conversão de espaço de cor, desentrelaçamento, redimensionamento de vídeo e conversão de taxa de quadros.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o leitor de origem poderá inserir um processador de vídeo no pipeline de processamento, que habilita os seguintes tipos de conversão de formato:

-   Conversão de espaço de cor (YUV para RGB-32)
-   Desentrelaçamento
-   Redimensionamento de vídeo
-   Conversão de taxa de quadros

Se esse atributo for **true**, o atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) deverá ser **false**.

O leitor de origem procura por processadores de vídeo que estão registrados na categoria MFT, categoria do **\_ \_ \_ processador de vídeo** , incluindo MFTs que são registrados para o processo local. (Consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) para obter mais informações sobre o registro local de MFTs.) O leitor de origem usa o XVP (processador de vídeo transcodificar) se nenhum outro processador de vídeo adequado for encontrado.

O aplicativo especifica o tipo de saída desejado chamando [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype). Quando o leitor de origem configura o processador de vídeo, ele tenta corresponder os seguintes atributos do tipo de saída:

-   Taxa de quadros[( \_ \_ \_ taxa de quadros MF MT](mf-mt-frame-rate-attribute.md))
-   Tamanho do quadro[( \_ \_ \_ tamanho do quadro MF MT](mf-mt-frame-size-attribute.md))
-   Modo entrelaçamento[( \_ \_ \_ modo de entrelaçamento MF MT](mf-mt-interlace-mode-attribute.md))
-   Taxa de proporção de pixel (taxa de proporção de[ \_ \_ pixel \_ \_ MF MT](mf-mt-pixel-aspect-ratio-attribute.md))
-   Subtipo ([ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md))

Esse atributo é semelhante ao [leitor de origem MF habilitar o atributo de \_ \_ \_ \_ \_ processamento de vídeo](mf-source-reader-enable-video-processing.md) , mas oferece as seguintes vantagens:

-   Há suporte para uma maior variedade de conversões de formato.
-   Os aplicativos podem registrar seus próprios conversores.
-   Algumas conversões podem ser executadas em hardware usando a GPU.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




