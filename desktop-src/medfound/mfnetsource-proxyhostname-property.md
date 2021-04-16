---
description: Especifica o nome do host do servidor proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: Propriedade MFNETSOURCE_PROXYHOSTNAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768309"
---
# <a name="mfnetsource_proxyhostname-property"></a>\_Propriedade MFNETSOURCE PROXYHOSTNAME

Especifica o nome do host do servidor proxy.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

LPWStr do VT \_

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYHOSTNAME** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar o localizador de proxy padrão ao criar o objeto de localizador de proxy. Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Essa propriedade deve ser definida pelo aplicativo quando o localizador de proxy estiver configurado para operar no modo manual.

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

 

 




