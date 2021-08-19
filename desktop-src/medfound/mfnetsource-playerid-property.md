---
description: O valor do campo &\# 0034;c-playerid&0034; que a fonte de rede usa para \# registro em log.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: MFNETSOURCE_PLAYERID propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1fc9afc79dec48a3ee19b007d2d1e04c0ccc35ab9a2bdd04c6699cd1ff65fea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874610"
---
# <a name="mfnetsource_playerid-property"></a>Propriedade PLAYERID MFNETSOURCE \_

O valor do campo "c-playerid" que a fonte de rede usa para registro em log. Os aplicativos podem definir essa propriedade como qualquer valor de cadeia de caracteres.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PLAYERID** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Registro em log do cliente](client-logging.md)
</dt> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




