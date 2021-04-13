---
description: Contém sinalizadores que indicam quais funcionalidades foram alteradas na sessão de mídia, com base na apresentação atual.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Atributo MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370657"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_Atributo de Delta de evento MF \_ SESSIONCAPS \_

Contém sinalizadores que indicam quais funcionalidades foram alteradas na sessão de mídia, com base na apresentação atual.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo contém um bitmask que indica quais sinalizadores de funcionalidades foram alterados. Para obter uma lista de possíveis sinalizadores, consulte [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Os bits são definidos como 1 no bitmask por qualquer um dos seguintes motivos:

-   O bit de recursos correspondente foi alterado de 0 para 1.
-   O bit de recursos correspondente mudou de 1 para 0.
-   O bit de recursos correspondente permaneceu 1, mas os detalhes do recurso foram alterados. Por exemplo, a taxa de reprodução máxima foi alterada.

Esse atributo é usado com o evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .

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
</dt> </dl>

 

 




