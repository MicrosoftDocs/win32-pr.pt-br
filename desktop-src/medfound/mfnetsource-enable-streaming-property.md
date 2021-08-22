---
description: Especifica se todos os protocolos de streaming estão habilitados.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: MFNETSOURCE_ENABLE_STREAMING propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fae2b127a52bbea9e8d122ec9ad219c61010068b07696b44cce49cc7546c9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463696"
---
# <a name="mfnetsource_enable_streaming-property"></a>Propriedade MFNETSOURCE \_ ENABLE \_ STREAMING

Especifica se todos os protocolos de streaming estão habilitados.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

Booliana (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ ENABLE \_ STREAMING** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para [a Configuração de uma Fonte de Mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




