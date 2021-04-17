---
description: Indica se a estabilização de vídeo foi aplicada a um quadro de vídeo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Atributo MFSampleExtension_VideoDSPMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772660"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>\_Atributo MFSampleExtension VideoDSPMode

Indica se a estabilização de vídeo foi aplicada a um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**MFVideoDSPMode** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

O [**estabilização de vídeo MFT**](video-stabilization-mft.md) define esse atributo nos exemplos de saída que ele produz. O valor do atributo é um valor de enumeração [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Se o valor for **MFVideoDSPMode \_ estabilização**, isso significa que a MFT aplicou a estabilização de imagem ao quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> <dt>

[**Estabilização de Vídeo MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




