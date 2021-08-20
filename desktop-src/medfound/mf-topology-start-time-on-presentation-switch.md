---
description: Especifica a hora de início para apresentações na fila após a primeira apresentação.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c691871593705f29875a7cfca9675e236bed329c81c6d886a37646bd6208dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875356"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>HORA DE INÍCIO DA TOPOLOGIA DO MF \_ NO atributo SWITCH DE \_ \_ \_ \_ \_ APRESENTAÇÃO

Especifica a hora de início para apresentações na fila após a primeira apresentação.

## <a name="data-type"></a>Tipo de dados

**INT64 armazenado** como **UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se A

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Quando o aplicativo enfilra a primeira apresentação na Sessão de Mídia, o aplicativo especifica a hora de início no parâmetro *pvarStartPosition* do método [**IMFMediaSession::Start.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) No entanto, para quaisquer apresentações subsequentes, a hora de início é dada pelo atributo MF \_ TOPOLOGY \_ START TIME ON PRESENTATION SWITCH na \_ \_ \_ \_ topologia. A hora de início é especificada em unidades de 100 nanossegundos, em relação ao início da apresentação. Por exemplo, se o valor for 50000000, a reprodução iniciará 5 segundos na apresentação. Se esse atributo não estiver definido, a hora de início padrão será zero.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




