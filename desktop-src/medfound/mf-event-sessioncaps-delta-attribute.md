---
description: Contém sinalizadores que indicam quais recursos foram alterados na Sessão de Mídia, com base na apresentação atual.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714836"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>Atributo DELTA \_ \_ MF EVENT SESSIONCAPS \_

Contém sinalizadores que indicam quais recursos foram alterados na Sessão de Mídia, com base na apresentação atual.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo contém uma máscara de bits que indica quais sinalizadores de funcionalidades foram alterados. Para obter uma lista de possíveis sinalizadores, consulte [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Os bits são definidos como 1 na máscara de bits por qualquer um dos seguintes motivos:

-   O bit de funcionalidades correspondentes foi alterado de 0 para 1.
-   O bit de funcionalidades correspondentes foi alterado de 1 para 0.
-   O bit de funcionalidades correspondentes ficou 1, mas os detalhes da funcionalidade foram alterados. Por exemplo, a taxa de reprodução máxima foi alterada.

Esse atributo é usado com o [evento MESessionCapabilitiesChanged.](mesessioncapabilitieschanged.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




