---
description: Especifica se o protocolo HTTP está habilitado na origem da rede.
ms.assetid: dcc4db5c-0274-4a8a-89a4-66cda62e1520
title: MFNETSOURCE_ENABLE_HTTP propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d033594e223b8219f168e86d82ef02012bfafd4be9d758a438d042356735f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874762"
---
# <a name="mfnetsource_enable_http-property"></a>Propriedade MFNETSOURCE \_ ENABLE \_ HTTP

Especifica se o protocolo HTTP está habilitado na origem da rede.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Booliana (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ ENABLE \_ HTTP** define o GUID dessa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede no Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




