---
description: Armazena o nome do host e a porta do servidor proxy usado pela fonte de rede.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Propriedade MFNETSOURCE_PROXYINFO (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780389"
---
# <a name="mfnetsource_proxyinfo-property"></a>\_Propriedade MFNETSOURCE PROXYINFO

Armazena o nome do host e a porta do servidor proxy usado pela fonte de rede.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

LPWStr do VT \_

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYINFO** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Esta propriedade é somente para leitura. Para obter o valor da propriedade da origem da rede, chame **IPropertyStore:: GetValue** e passe a estrutura **PROPERTYKEY** no parâmetro *Key* . O membro **fmtid** de **PROPERTYKEY** deve ser definido como a propriedade GUID.

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

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Suporte de proxy para fontes de rede](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




