---
description: O valor do campo &\# 0034; c-hostexever&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Propriedade MFNETSOURCE_HOSTVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461180"
---
# <a name="mfnetsource_hostversion-property"></a>\_Propriedade MFNETSOURCE HOSTVERSION

O valor do campo "c-hostexever" usado pela fonte de rede para registro em log. Os aplicativos podem definir essa propriedade como o número de versão do aplicativo host. O aplicativo host é o arquivo. exe identificado pelo campo c-hostexe.



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

 

 




