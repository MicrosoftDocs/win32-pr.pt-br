---
description: Indica se a estabilização de vídeo foi aplicada a um quadro de vídeo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode atributo (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95776fd7b8e130b9538e98843ca72d69980978b6f954747fadca939b8d3c5922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554926"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>Atributo VideoDSPMode MFSampleExtension \_

Indica se a estabilização de vídeo foi aplicada a um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**MFVideoDSPMode** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

O [**Estabilização de Vídeo MFT**](video-stabilization-mft.md) define esse atributo nos exemplos de saída que ele produz. O valor do atributo é um valor de enumeração [**MFVideoDSPMode.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) Se o valor for **Estabilização de \_ MFVideoDSPMode,** isso significa que a estabilização de imagem aplicada por MFT ao quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Exemplos de mídia](media-samples.md)
</dt> <dt>

[**Estabilização de Vídeo MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




