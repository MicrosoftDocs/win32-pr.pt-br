---
description: Fornece os métodos que o WUA pode usar para coletar informações sobre o token de ponto de extremidade.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interface IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461164"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interface IUpdateEndpointAuthToken

Fornece os métodos que o WUA pode usar para coletar informações sobre o token de ponto de extremidade.

## <a name="members"></a>Membros

A interface **IUpdateEndpointAuthToken** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthToken** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUpdateEndpointAuthToken** tem esses métodos.



| Método                                                                                | Descrição                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Obtém o identificador do serviço a ser autenticado.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Obtém a chave usada para assinar mensagens de saída entre o computador cliente e o sercvice.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Obtém os dados XML (enviados pela transmissão) que representam o token. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Obtém o formato XML de uma referência anexada ao token.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Obtém o formato XML de uma referência desanexada ao token.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Obtém o tipo do token do ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1,1. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>                |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
