---
description: O valor do campo &\# 0034; c-hostexever&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Propriedade MFNETSOURCE_HOSTVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5f78a277de4fc5b0609be31f21f684357806dbb8609657a930cdc4816b1e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243456"
---
# <a name="mfnetsource_hostversion-property"></a>\_Propriedade MFNETSOURCE HOSTVERSION

O valor do campo "c-hostexever" usado pela fonte de rede para registro em log. Os aplicativos podem definir essa propriedade como o número de versão do aplicativo host. O aplicativo host é o arquivo .exe identificado pelo campo c-hostexe.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**LONGLONG**

VT \_ i8

**hVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ HOSTVERSION** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Log de cliente](client-logging.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




