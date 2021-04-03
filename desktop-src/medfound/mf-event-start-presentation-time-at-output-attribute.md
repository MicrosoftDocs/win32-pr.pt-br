---
description: A hora da apresentação na qual os coletores de mídia processarão o primeiro exemplo da nova topologia.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Atributo MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828924"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>\_ \_ \_ Hora de início da apresentação do evento MF \_ \_ no \_ atributo de saída

A hora da apresentação na qual os coletores de mídia processarão o primeiro exemplo da nova topologia.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="remarks"></a>Comentários

Se qualquer objeto de pipeline na topologia anterior tiver dado buffer, esse valor será um pouco menor do que o valor no atributo de [**deslocamento de tempo de \_ apresentação de evento \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , pois os coletores devem renderizar os dados armazenados em buffer.

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




