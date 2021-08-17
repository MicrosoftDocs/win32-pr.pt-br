---
description: Especifica se o MpEG-4 File Sink filtra o SPS (conjunto de parâmetros de sequência) e as NALUs do PPS (conjunto de parâmetros de imagem).
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b939302999fc7e095abbc97aed5910976972c860440a2c865248949e0f052aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104622"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>Atributo MF \_ MPEG4SINK \_ SPSPPS \_ PASSTHROUGH

Especifica se o [**MpEG-4 File Sink**](mpeg-4-file-sink.md) filtra o SPS (conjunto de parâmetros de sequência) e as NALUs do PPS (conjunto de parâmetros de imagem).

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Comentários

O [**Sink de Arquivos MPEG-4**](mpeg-4-file-sink.md) grava os parâmetros SPS e PPS na caixa de descrição de exemplo do arquivo MP4. Por padrão, ele filtra as NALUs SPS e PPS do fluxo de vídeo. Para substituir esse comportamento, de definir o atributo \_ MF MPEG4SINK \_ SPSPPS \_ PASSTHROUGH como **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




