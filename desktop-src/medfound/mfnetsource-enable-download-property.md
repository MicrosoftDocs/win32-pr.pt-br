---
description: Especifica se todos os protocolos de download estão habilitados.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: Propriedade MFNETSOURCE_ENABLE_DOWNLOAD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7749dcdf15c099284a73cf6c55c1d753825230126e77a972e906b280a0b09a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738975"
---
# <a name="mfnetsource_enable_download-property"></a>MFNETSOURCE \_ habilitar a \_ propriedade de download

Especifica se todos os protocolos de download estão habilitados.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Booliano (**longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ habilitar \_ Download** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para a [configuração de uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




