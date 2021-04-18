---
description: Especifica uma lista delimitada por ponto-e-vírgula dos servidores de mídia que podem aceitar conexões de aplicativos cliente sem usar um servidor proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: Propriedade MFNETSOURCE_PROXYEXCEPTIONLIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814458"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a>\_Propriedade MFNETSOURCE PROXYEXCEPTIONLIST

Especifica uma lista delimitada por ponto-e-vírgula dos servidores de mídia que podem aceitar conexões de aplicativos cliente sem usar um servidor proxy.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

LPWStr do VT \_

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy. Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . O localizador de proxy não executa a detecção de proxy para esses endereços.

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

 

 




