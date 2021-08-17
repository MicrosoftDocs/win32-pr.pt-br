---
description: Deslocamento entre o carimbo de data/hora em cada amostra recebida pelo grabber de exemplo e a hora em que o grabber de exemplo apresenta o exemplo.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad8086d7820a9f7c642fb049af8696521f675be3f7606ff19166a4570ee8000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875980"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>Atributo MF \_ SAMPLEGRABBERSINK \_ SAMPLE \_ TIME \_ OFFSET

Deslocamento entre o carimbo de data/hora em cada amostra recebida pelo grabber de exemplo e a hora em que o grabber de exemplo apresenta o exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornado pela [**função MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Esse atributo permite que a função de retorno de chamada do grabber de exemplo receba amostras anteriores à hora da apresentação.

Quando o grabber de exemplo recebe um novo exemplo, ele apresenta o exemplo no momento *t* − *deslocamento*, em que *t* é o carimbo de data/hora no exemplo e *offset* é o valor desse atributo. Se esse atributo não estiver definido, o valor padrão será zero.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFSampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




