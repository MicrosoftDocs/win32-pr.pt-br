---
description: Especifica o protocolo de controle usado pela fonte de rede.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: Propriedade MFNETSOURCE_PROTOCOL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae15ce40e7c049552cbb0f4916f5f4ff70ef6e55746528ebe0083eee69b22a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243318"
---
# <a name="mfnetsource_protocol-property"></a>\_Propriedade de protocolo MFNETSOURCE

Especifica o protocolo de controle usado pela fonte de rede. O valor dessa propriedade é um membro da enumeração de [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**LONG**

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

O **\_ protocolo MFNETSOURCE** constante define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Esta propriedade é somente para leitura. Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




