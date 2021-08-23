---
description: Especifica o protocolo de transporte usado pela fonte de rede.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: Propriedade MFNETSOURCE_TRANSPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933c4051cd3d008082c3b7811fcd88f8b118e51a9e864d947750813c11883b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663466"
---
# <a name="mfnetsource_transport-property"></a>\_Propriedade de transporte MFNETSOURCE

Especifica o protocolo de transporte usado pela fonte de rede. O valor dessa propriedade é um membro da enumeração de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**LONG**

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

O **\_ transporte constante MFNETSOURCE** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Esta propriedade é somente para leitura. Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




