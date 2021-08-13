---
description: A hora aproximada em que a sessão de mídia gerou um evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: Atributo MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6cbaa7d12cebe14b015c4d568b36b081930ef4b302797dba76fc728e92cf01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740020"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>\_Atributo de \_ \_ tempo de ocorrência de evento aprox \_ de sessão MF \_

A hora aproximada em que a sessão de mídia gerou um evento.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="remarks"></a>Comentários

Alguns eventos da sessão de mídia têm esse atributo. O valor fornece o tempo de apresentação aproximado quando o evento foi gerado.

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
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

 

 




