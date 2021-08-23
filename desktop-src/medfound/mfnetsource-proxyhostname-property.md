---
description: Especifica o nome do host do servidor proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82746763c937bdca388782cb0882b536c0b9e93b660e0f8e0a04426e5b48a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663666"
---
# <a name="mfnetsource_proxyhostname-property"></a>Propriedade MFNETSOURCE \_ PROXYHOSTNAME

Especifica o nome do host do servidor proxy.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYHOSTNAME** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar o localizador de proxy padrão ao criar o objeto de localizador de proxy. Para definir a propriedade , passe um ponteiro **IPropertyStore** no parâmetro *pProxyConfig* da [**função MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Essa propriedade deve ser definida pelo aplicativo quando o localizador de proxy está configurado para operar no modo manual.

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

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Suporte a proxy para fontes de rede](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




