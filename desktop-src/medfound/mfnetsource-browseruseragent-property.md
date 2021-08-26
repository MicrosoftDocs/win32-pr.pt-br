---
description: O valor da primeira parte do &\# 0034; cs (User-Agent) &\# 0034; campo que a fonte de rede usa para registro em log.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: Propriedade MFNETSOURCE_BROWSERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf46fde925dbe2d94643a0843d105726f0976ba7a84f47773ef35e32ae8dfde7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954856"
---
# <a name="mfnetsource_browseruseragent-property"></a>\_Propriedade MFNETSOURCE BROWSERUSERAGENT

O valor da primeira parte do campo "cs (User-Agent)" que a fonte de rede usa para o registro em log. Os aplicativos podem definir essa propriedade como qualquer valor de cadeia de caracteres.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

LPWStr do VT \_

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ BROWSERUSERAGENT** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Log de cliente](client-logging.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[**MFNETSOURCE \_ PLAYERUSERAGENT**](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




