---
description: Duração máxima de streaming acelerado, em milissegundos, quando a origem da rede usa o transporte UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Propriedade MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011697"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a>\_Propriedade MFNETSOURCE MAXUDPACCELERATEDSTREAMINGDURATION

Duração máxima de streaming acelerado, em milissegundos, quando a origem da rede usa o transporte UDP.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**DWORD** (armazenado como **longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Para o transporte UDP, essa propriedade substitui a propriedade [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) se o valor dessa propriedade for menor.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

O valor padrão dessa propriedade é 8.000 milissegundos.

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

[Recursos de origem da rede](network-source-features.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




