---
title: Constantes de autorização (RpcDce. h)
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
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645202"
---
# <a name="authorization-constants"></a>Constantes de autorização

Define o que o servidor autoriza.



| Constante/valor                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt> </dl>                   | O servidor não executa nenhuma autorização. Atualmente, o RPC \_ c \_ Authn \_ WinNT, o RPC \_ c \_ Authn \_ GSS \_ Schannel e o RPC \_ c \_ Authn \_ GSS \_ Kerberos todos usam somente RPC \_ c \_ AUTHZ \_ None.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt> </dl>                   | O servidor executa a autorização com base no nome principal do cliente. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | O servidor executa a verificação de autorização usando as informações de PAC (certificado de atributo de privilégio) do cliente DCE, que são enviadas para o servidor com cada chamada de procedimento remoto feita usando o identificador de associação. Geralmente, o acesso é verificado em relação às ACLs (listas de controle de acesso) do DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ padrão**</dt> , <dt>0xFFFFFFFF</dt> </dl> | O DCOM pode escolher o nível de autorização usando seu algoritmo normal de negociação ampla de segurança. Para obter mais informações, consulte [negociação de cobertura de segurança](security-blanket-negotiation.md).<br/>                                                                                           |



## <a name="remarks"></a>Comentários

Essas constantes são usadas por métodos da interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Eles são usados na estrutura [**de \_ \_ serviço de autenticação exclusiva**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , que é recuperada pela função [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Eles também são usados na estrutura [**de \_ \_ informações de autenticação exclusiva**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , que, por sua vez, é membro da estrutura [**exclusiva da \_ \_ lista de autenticação**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) . Essa estrutura, que é uma lista de serviços de autenticação, os serviços de autorização que eles executam e as informações de autenticação para cada serviço, são passadas para a função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e o método [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**\_informações de autenticação exclusiva \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**\_serviço de autenticação exclusivo \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

