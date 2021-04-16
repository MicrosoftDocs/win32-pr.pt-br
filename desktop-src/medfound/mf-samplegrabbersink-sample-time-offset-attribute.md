---
description: Deslocamento entre o carimbo de data/hora de cada exemplo recebido pelo exemplo de apoio e a hora em que o exemplo de amostra apresenta o exemplo.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Atributo MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750148"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>\_Atributo de \_ deslocamento de tempo de exemplo MF SAMPLEGRABBERSINK \_ \_

Deslocamento entre o carimbo de data/hora de cada exemplo recebido pelo exemplo de apoio e a hora em que o exemplo de amostra apresenta o exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) que é retornado pela função [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Esse atributo habilita a função de retorno de chamada do exemplo para receber amostras anteriores à hora da apresentação.

Quando o complemento de exemplo recebe um novo exemplo, ele apresenta a amostra no tempo *t* − *deslocamento*, em que *t* é o carimbo de data/hora no exemplo e *deslocamento* é o valor desse atributo. Se esse atributo não for definido, o valor padrão será zero.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFSampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




