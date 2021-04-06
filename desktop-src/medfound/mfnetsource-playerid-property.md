---
description: O valor do campo &\# 0034; c-playerid&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: Propriedade MFNETSOURCE_PLAYERID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011400"
---
# <a name="mfnetsource_playerid-property"></a>\_Propriedade MFNETSOURCE playerid

O valor do campo "c-playerid" que a fonte de rede usa para registro em log. Os aplicativos podem definir essa propriedade como qualquer valor de cadeia de caracteres.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

LPWStr do VT \_

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ playerid** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

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

 

 




