---
description: Especifica se a origem da rede armazena em cache o conteúdo.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: Propriedade MFNETSOURCE_CACHEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6954359ed91fe402d785fec9e63f470c31abc85432e519b2e06bcb1d679933dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113626"
---
# <a name="mfnetsource_cacheenabled-property"></a>\_Propriedade MFNETSOURCE CACHEENABLED

Especifica se a origem da rede armazena em cache o conteúdo.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Booliano (**longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ CACHEENABLED** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

O valor padrão dessa propriedade é **true**.

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
</dt> </dl>

 

 




