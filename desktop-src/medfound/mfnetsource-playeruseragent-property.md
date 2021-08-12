---
description: O valor da segunda parte do campo &\# 0034;cs(User-Agent)&0034; que a fonte de rede usa para registro em \# log.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: MFNETSOURCE_PLAYERUSERAGENT propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b431780345c8b297bf154813a9713b5b158ecc99cc4384294ee983b8066ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243418"
---
# <a name="mfnetsource_playeruseragent-property"></a>Propriedade MFNETSOURCE \_ PLAYERUSERAGENT

O valor da segunda parte do campo "cs(User-Agent)" que a fonte de rede usa para registro em log. Os aplicativos podem definir essa propriedade como qualquer valor de cadeia de caracteres.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Cadeia de caracteres largos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PLAYERUSERAGENT** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Registro em log do cliente](client-logging.md)
</dt> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[**MFNETSOURCE \_ BROWSERUSERAGENT**](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




