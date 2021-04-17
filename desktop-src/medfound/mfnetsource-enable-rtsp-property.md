---
description: Especifica se o transporte RTSP (Real-Time Streaming Protocol) está habilitado na origem da rede.
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: Propriedade MFNETSOURCE_ENABLE_RTSP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac191e6e244a8e341fef0dccd274293f09846aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812085"
---
# <a name="mfnetsource_enable_rtsp-property"></a>MFNETSOURCE \_ habilitar a \_ Propriedade RTSP

Especifica se o transporte RTSP (Real-Time Streaming Protocol) está habilitado na origem da rede.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Booliano (**longo**)

\_I4 VT

**lVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ habilitar \_ RTSP** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para configurar a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

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

[Protocolos com suporte](supported-protocols.md)
</dt> </dl>

 

 




