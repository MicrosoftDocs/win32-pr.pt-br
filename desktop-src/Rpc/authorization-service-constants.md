---
title: Authorization-Service constantes (Rpcdce.h)
description: As constantes do serviço de autorização representam os serviços de autorização passados para várias funções de tempo de executar.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027b32acb8b38ac1359cee96f68542da94f48d3bdf7d454d631bf0a8eff1092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023426"
---
# <a name="authorization-service-constants"></a>Authorization-Service constantes

As constantes do serviço de autorização representam os serviços de autorização passados para várias funções de tempo de executar.

As constantes a seguir são valores válidos para *o parâmetro AuthzSvc.* A maioria dos aplicativos acha \_ RPC C \_ AUTHZ \_ NÃO suficiente.



| Constante/valor                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NONE**</dt> <dt>0</dt> </dl>                   | O servidor não executa nenhuma autorização.<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NAME**</dt> <dt>1</dt> </dl>                   | O servidor executa a autorização com base no nome principal do cliente.<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | O servidor executa a verificação de autorização usando as informações de PAC (certificado de atributo de privilégio DCE) do cliente, que são enviadas ao servidor com cada chamada de procedimento remoto feita usando o alça de associação. Em geral, o acesso é verificado em listas de controle de acesso DCE[(ACLs).](/windows/desktop/api/winnt/ns-winnt-acl)<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DEFAULT**</dt> <dt>0xffffffff</dt> </dl> | O servidor usa o serviço de autorização padrão para o SSP atual.<br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

