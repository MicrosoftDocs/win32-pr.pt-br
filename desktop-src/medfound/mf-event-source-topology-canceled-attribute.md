---
description: Especifica se a origem do sequenciador cancelou uma topologia.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Atributo MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755500"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>\_Atributo de topologia de origem de evento MF \_ \_ \_ cancelado

Especifica se a [origem do sequenciador](sequencer-source.md) cancelou uma topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo é usado com os seguintes eventos:

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Se esse atributo estiver presente e for diferente de zero, significa que o segmento de apresentação terminou porque a origem do sequenciador cancelou a topologia. Caso contrário, o segmento de apresentação terminou normalmente.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Eventos de origem do Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




