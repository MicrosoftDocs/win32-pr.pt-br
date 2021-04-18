---
description: O número de vezes que a fonte de rede tentou reconectar-se à rede.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Propriedade MFNETSOURCE_AUTORECONNECTPROGRESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785922"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>\_Propriedade MFNETSOURCE AUTORECONNECTPROGRESS

O número de vezes que a fonte de rede tentou reconectar-se à rede.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**DWORD** (armazenado como **longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Esta propriedade é somente para leitura. Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Recursos de origem da rede](network-source-features.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




