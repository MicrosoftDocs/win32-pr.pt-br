---
description: Especifica o status de uma topologia durante a reprodução.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: Atributo MF_EVENT_TOPOLOGY_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781540"
---
# <a name="mf_event_topology_status-attribute"></a>\_Atributo de \_ status da topologia de evento MF \_

Especifica o status de uma topologia durante a reprodução.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da enumeração [**MF \_ TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) .

Esse atributo é usado com o evento [MESessionTopologyStatus](mesessiontopologystatus.md) .

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

 

 




