---
description: Contém um ponteiro para a interface IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Propriedade MFNETSOURCE_CREDENTIAL_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090854"
---
# <a name="mfnetsource_credential_manager-property"></a>Propriedade do Gerenciador de \_ credenciais MFNETSOURCE \_

Contém um ponteiro para a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Use essa propriedade para passar a implementação do aplicativo de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) para a fonte de rede.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Ponteiro **IUnknown**

VT \_ desconhecido

**punkVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ Credential \_ Manager** define o **GUID** para a chave de propriedade. O identificador de propriedade (PID) é zero.

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

[Autenticação de origem da rede](network-source-authentication.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




