---
description: Especifica se o coletor de arquivos MPEG-4 filtra o conjunto de parâmetros de sequência (SPS) e o conjunto de parâmetros de imagem (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Atributo MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661575"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>\_Atributo de passagem MF MPEG4SINK \_ SPSPPS \_

Especifica se o [**coletor de arquivos MPEG-4**](mpeg-4-file-sink.md) filtra o conjunto de parâmetros de sequência (SPS) e o conjunto de parâmetros de imagem (PPS) NALUs.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Comentários

O [**coletor de arquivos MPEG-4**](mpeg-4-file-sink.md) grava os parâmetros SPS e PPS na caixa de descrição de exemplo do arquivo MP4. Por padrão, ele filtra o SPS e o PPS NALUs do fluxo de vídeo. Para substituir esse comportamento, defina o \_ atributo de passagem MF MPEG4SINK \_ SPSPPS \_ como **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




