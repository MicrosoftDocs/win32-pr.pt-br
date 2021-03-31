---
description: O valor do campo &\# 0034; c-playerversion&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Propriedade MFNETSOURCE_PLAYERVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663211"
---
# <a name="mfnetsource_playerversion-property"></a>\_Propriedade MFNETSOURCE PLAYERVERSION

O valor do campo "c-playerversion" usado pela fonte de rede para registro em log. Os aplicativos podem definir essa propriedade como o número de versão do aplicativo.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**LONGLONG**

VT \_ i8

**hVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PLAYERVERSION** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [resolvedor de origem](source-resolver.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Log de cliente](client-logging.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




