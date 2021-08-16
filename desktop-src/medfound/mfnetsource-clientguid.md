---
description: Identificador exclusivo pelo qual o servidor identifica o cliente.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Propriedade MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9585f5ac9cd69148272cb986746f6849aad4c3aa048b46baf2f75aeaba77c092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738985"
---
# <a name="mfnetsource_clientguid-property"></a>\_Propriedade MFNETSOURCE CLIENTGUID

Identificador exclusivo pelo qual o servidor identifica o cliente.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**GUID**

CLSID do VT \_

**puuid**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ CLIENTGUID** define o GUID da chave de propriedade. O identificador de propriedade (PID) é zero. Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Se não for definido ou definido como **GUID \_ NULL**, Microsoft Media Foundation gerará um GUID anônimo por sessão que garanta a privacidade do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




