---
description: Especifica se o localizador de proxy deve usar um servidor proxy para endereços locais.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Propriedade MFNETSOURCE_PROXYBYPASSFORLOCAL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646573"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>\_Propriedade MFNETSOURCE PROXYBYPASSFORLOCAL

Especifica se o localizador de proxy deve usar um servidor proxy para endereços locais.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Booliano (**longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy. Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . O valor deve ser definido como 0 se o servidor proxy for usado para endereços locais; caso contrário, um valor diferente de zero configurará o localizador de proxy padrão para ignorar o servidor proxy para endereços locais.

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

 

 




