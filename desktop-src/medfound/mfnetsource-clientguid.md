---
description: Identificador exclusivo pelo qual o servidor identifica o cliente.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Propriedade MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090855"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




