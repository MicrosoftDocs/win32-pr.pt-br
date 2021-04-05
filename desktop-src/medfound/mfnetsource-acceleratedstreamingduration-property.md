---
description: Duração do streaming acelerado para a fonte de rede, em milissegundos.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Propriedade MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827413"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>\_Propriedade MFNETSOURCE ACCELERATEDSTREAMINGDURATION

Duração do streaming acelerado para a fonte de rede, em milissegundos.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**DWORD** (armazenado como **longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um objeto **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Essa propriedade se aplica ao recurso de início rápido do Windows Media Services, que reproduz conteúdo rapidamente sem aguardar o buffer inicial longo. Ao usar o início rápido, o servidor que executa o Windows Media Services enviará alguns dados no início do conteúdo a uma taxa mais rápida do que a especificada pela taxa de bits do conteúdo.

O valor padrão dessa propriedade é 10.000 milissegundos.

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

 

 




