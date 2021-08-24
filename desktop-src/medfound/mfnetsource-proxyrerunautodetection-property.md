---
description: Especifica se o localizador de proxy padrão deve forçar a detecção automática de proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: MFNETSOURCE_PROXYRERUNAUTODETECTION propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3351766302952390bbe67ea2d86cd76e93b9267328fe2c07e2656a38b3fd2906
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713986"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a>Propriedade MFNETSOURCE \_ PROXYRERUNAUTODETECTION

Especifica se o localizador de proxy padrão deve forçar a detecção automática de proxy.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Booliana (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYSETTINGS** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy. Para definir a propriedade , passe um ponteiro **IPropertyStore** no parâmetro *pProxyConfig* da [**função MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) No modo de detecção automática, o localizador de proxy usa o mecanismo de detecção de proxy WinInet. Para forçar a detecção automática, de definido o valor como 0.

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

 

 




