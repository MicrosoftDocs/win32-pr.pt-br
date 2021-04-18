---
description: Quantidade máxima de dados que os buffers de origem de rede, em milissegundos.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: Propriedade MFNETSOURCE_MAXBUFFERTIMEMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788939"
---
# <a name="mfnetsource_maxbuffertimems-property"></a>\_Propriedade MFNETSOURCE MAXBUFFERTIMEMS

Quantidade máxima de dados que os buffers de origem de rede, em milissegundos.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**DWORD** (armazenado como **longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ MAXBUFFERTIMEMS** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

O valor padrão dessa propriedade é 40.000 milissegundos.

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

 

 




