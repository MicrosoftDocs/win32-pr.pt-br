---
title: Interface INapCertRelyingParty (NapCertRelyingParty. h)
description: As partes confiáveis do certificado devem usar o para se comunicar com o NapAgent.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- INapCertRelyingParty da interface NAP
- INapCertRelyingParty interface NAP, descrita
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d2a68c6ce910fa63588df1fa7bc1834f6ed537a2a2c9b85f24d383497a8d463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368605"
---
# <a name="inapcertrelyingparty-interface"></a>Interface INapCertRelyingParty

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapCertRelyingParty** fornece métodos que as partes confiáveis de certificado devem usar para se comunicar com o NapAgent.

## <a name="members"></a>Membros

A interface **INapCertRelyingParty** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapCertRelyingParty** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapCertRelyingParty** tem esses métodos.



| Método                                                                                                        | Descrição                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**INapCertRelyingParty::GetSubscribedRelyingParties**](inapcertrelyingparty-getsubscribedrelyingparties.md) | Obtém uma lista de terceiras partes confiáveis que se inscreveram.<br/>                 |
| [**INapCertRelyingParty::SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)               | Assina um servidor de certificado de integridade já registrado (HCS).<br/> |
| [**INapCertRelyingParty::UnSubscribeCertByGroup**](inapcertrelyingparty-unsubscribecertbygroup.md)           | Cancela a assinatura de um servidor HCS.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

