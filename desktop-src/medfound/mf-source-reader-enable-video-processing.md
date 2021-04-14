---
description: Habilita o processamento de vídeo pelo leitor de origem.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Atributo MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461081"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>\_Leitor de origem MF \_ \_ habilitar atributo de \_ processamento de vídeo \_

Habilita o processamento de vídeo pelo [leitor de origem](source-reader.md).

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                                                                                                                | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Diferente**</dt> </dl> | Habilite o processamento de vídeo.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Zero**</dt> </dl>             | Desabilite o processamento de vídeo. (Padrão)<br/> |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Se esse atributo for **true** (diferente de zero), o leitor de origem poderá executar o seguinte processamento de vídeo limitado em quadros de vídeo descompactados:

-   Conversão de YUV para RGB-32.
-   Desentrelaçamento.

Essas operações são executadas no software e não são otimizadas para reprodução. Esse recurso destina-se a aplicativos que processam um pequeno número de quadros, por exemplo, para criar uma miniatura de vídeo — ou aplicativos que não decodificam quadros em tempo real. A operação de desentrelaçamento interpola os dados de um único campo, portanto, ele tem perda.

Evite essa configuração se você estiver usando o Direct3D para exibir os quadros de vídeo, pois a GPU geralmente fornece melhores recursos de processamento de vídeo.

Se esse atributo for **true**, os seguintes atributos deverão ser **falsos**:

-   [\_Gerenciador de \_ D3D do leitor de origem MF \_ \_](mf-source-reader-d3d-manager.md)
-   [\_conversores do MF ReadWrite \_ Disable \_](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




