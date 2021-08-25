---
description: Especifica se o transporte TCP está habilitado para a origem da rede.
ms.assetid: ba655505-dcac-4cea-8ad5-ccd1b55ee9d4
title: Propriedade MFNETSOURCE_ENABLE_TCP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcd5fe37ab423bd48af8aad45bdbb5c2b09b2d9b4b59fd40d85429d1fa1913ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954797"
---
# <a name="mfnetsource_enable_tcp-property"></a>MFNETSOURCE \_ habilitar a \_ Propriedade TCP

Especifica se o transporte TCP está habilitado para a origem da rede.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Booliano (**longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




