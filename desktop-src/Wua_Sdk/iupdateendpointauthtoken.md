---
description: Fornece os métodos que o WUA pode usar para coletar informações sobre o token de ponto de extremidade.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interface IUpdateEndpointAuthToken (UpdateEndpointAuth.h)
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
ms.openlocfilehash: 7b5afa1e9039b7f210dfbf71c8bceff4a7b438b413844a7a7e55dec0fd9fea8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855756"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interface IUpdateEndpointAuthToken

Fornece os métodos que o WUA pode usar para coletar informações sobre o token de ponto de extremidade.

## <a name="members"></a>Membros

A interface **IUpdateEndpointAuthToken** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthToken** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUpdateEndpointAuthToken** tem esses métodos.



| Método                                                                                | Descrição                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Obtém o identificador do serviço a ser autenticado.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Obtém a chave usada para assinar mensagens de saída entre o computador cliente e o serviço.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Obtém os dados XML (enviados pela transmissão) que representam o token. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Obtém o formato XML de uma referência anexada ao token.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Obtém o formato XML de uma referência desassogada ao token.<br/>                                                     |
| [**Tokentype**](iupdateendpointauthtoken-tokentype.md)                               | Obtém o tipo do token de ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1.1. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]<br/>                |
| Cabeçalho<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
