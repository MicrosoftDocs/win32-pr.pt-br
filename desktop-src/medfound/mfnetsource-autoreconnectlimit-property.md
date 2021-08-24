---
description: O número de vezes que a fonte de rede tenta se reconectar ao servidor e retomar o streaming se a conexão for perdida.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: MFNETSOURCE_AUTORECONNECTLIMIT propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f526e9ff0274438b696996c1143620ec367fa7b086a479a066d0ba9c283f95a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604536"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a>Propriedade MFNETSOURCE \_ AUTORECONNECTLIMIT

O número de vezes que a fonte de rede tenta se reconectar ao servidor e retomar o streaming se a conexão for perdida.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**DWORD** (armazenado como **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ AUTORECONNECTLIMIT** define o GUID dessa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um **objeto IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

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

[Recursos de origem de rede](network-source-features.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




