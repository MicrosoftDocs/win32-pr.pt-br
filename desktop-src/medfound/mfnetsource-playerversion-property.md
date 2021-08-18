---
description: O valor do campo &\# 0034;c-playerversion&0034; que a fonte de rede usa para \# registro em log.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71828db44eca7c4318dbdb11e7934871911b06dbc4547f83723a9944f139ae26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738965"
---
# <a name="mfnetsource_playerversion-property"></a>Propriedade PLAYERVERSION MFNETSOURCE \_

O valor do campo "c-playerversion" que a fonte de rede usa para registro em log. Os aplicativos podem definir essa propriedade como o número de versão do aplicativo.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**Longlong**

VT \_ I8

**hVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PLAYERVERSION** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Resolvedor de origem](source-resolver.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Registro em log do cliente](client-logging.md)
</dt> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




