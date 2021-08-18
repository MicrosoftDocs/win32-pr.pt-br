---
description: Especifica se a topologia de segmento atual está vazia.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: MF_EVENT_SOURCE_FAKE_START atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b026811330443a3fb5e7c9671a7f6a3de8580985b6be4c6ba149a2d4dc196325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973765"
---
# <a name="mf_event_source_fake_start-attribute"></a>Atributo MF \_ EVENT \_ SOURCE FAKE \_ \_ START

Especifica se a topologia de segmento atual está vazia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Esse atributo é usado com o [evento MESourceStarted.](mesourcestarted.md)

A origem do sequenciador define esse atributo **como TRUE se** a topologia de segmento atual estiver vazia. Se esse atributo for **TRUE,** a reprodução ainda não foi iniciada. O valor padrão desse atributo é **FALSE.**

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

 

 




