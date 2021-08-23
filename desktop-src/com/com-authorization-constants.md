---
title: Constantes de autorização (RpcDce.h)
description: Define o que o servidor autoriza.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb89786a0c27c66177bc29861fdcf53a9341f73e498b5627e1cb826e83f61cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048664"
---
# <a name="authorization-constants"></a>Constantes de autorização

Define o que o servidor autoriza.



| Constante/valor                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NONE**</dt> <dt>0</dt> </dl>                   | O servidor não executa nenhuma autorização. Atualmente, rpc \_ C \_ AUTHN \_ WINNT, RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL e RPC C \_ \_ AUTHN \_ GSS \_ KERBEROS usam apenas RPC C \_ \_ AUTHZ \_ NONE.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NAME**</dt> <dt>1</dt> </dl>                   | O servidor executa a autorização com base no nome principal do cliente. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | O servidor executa a verificação de autorização usando as informações de PAC (certificado de atributo de privilégio DCE) do cliente, que são enviadas ao servidor com cada chamada de procedimento remoto feita usando o alçamento de associação. Em geral, o acesso é verificado nas ACLs (listas de controle de acesso) do DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DEFAULT**</dt> <dt>0xffffffff</dt> </dl> | O DCOM pode escolher o nível de autorização usando seu algoritmo de negociação normal de confiança de segurança. Para obter mais informações, consulte [Negociação de garantia de segurança.](security-blanket-negotiation.md)<br/>                                                                                           |



## <a name="remarks"></a>Comentários

Essas constantes são usadas por métodos da interface [**IClientSecurity.**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) Eles são usados na estrutura [**SOLE \_ AUTHENTICATION \_ SERVICE,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) que é recuperada pela [**função CoQueryAuthenticationServices.**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) Eles também são usados na estrutura [**DE INFORMAÇÕES DE \_ AUTENTICAÇÃO \_ EXCLUSIVA,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) que, por sua vez, é membro da estrutura [**LISTA DE \_ \_ AUTENTICAÇÃO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) EXCLUSIVA. Essa estrutura, que é uma lista de serviços de autenticação, os serviços de autorização que eles executam e as informações de autenticação para cada serviço, é passada para a função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e o método [**IClientSecurity::SetBlanket.**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Coinitializesecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**Iclientsecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**INFORMAÇÕES DE \_ AUTENTICAÇÃO \_ EXCLUSIVA**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**SERVIÇO DE \_ AUTENTICAÇÃO \_ EXCLUSIVA**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

