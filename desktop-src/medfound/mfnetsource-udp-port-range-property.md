---
description: O intervalo de portas UDP válidas que a fonte de rede pode usar para receber conteúdo de streaming.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: MFNETSOURCE_UDP_PORT_RANGE propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74edcc229e9aad77de189b1dc5eb96b6a0050f366ee9df566c787b1de860bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874583"
---
# <a name="mfnetsource_udp_port_range-property"></a>Propriedade MFNETSOURCE \_ UDP \_ PORT \_ RANGE

O intervalo de portas UDP válidas que a fonte de rede pode usar para receber conteúdo de streaming. O valor dessa propriedade é uma cadeia de caracteres com o formato " *m*–*n* " em que *m* e *n* são números de porta.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ UDP \_ PORT \_ RANGE** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

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

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




