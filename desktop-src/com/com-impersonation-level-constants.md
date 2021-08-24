---
title: Constantes de nível de representação (RpcDce.h)
description: Especifica um nível de representação, que indica a quantidade de autoridade dada ao servidor quando ele está representando o cliente.
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc4b4a74871eb111b778d798587e53027053fe57cc8cda837a3aafb7c24d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048484"
---
# <a name="impersonation-level-constants"></a>Constantes de nível de representação

Especifica um nível de representação, que indica a quantidade de autoridade dada ao servidor quando ele está representando o cliente.



| Constante/valor                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ DEFAULT**</dt> <dt>0</dt> </dl>             | O DCOM pode escolher o nível de representação usando seu algoritmo de negociação normal de confiança de segurança. Para obter mais informações, consulte [Negociação de garantia de segurança.](security-blanket-negotiation.md)<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ C \_ IMP \_ NÍVEL \_ ANÔNIMO**</dt> <dt>1</dt> </dl>       | O cliente é anônimo ao servidor. O processo do servidor pode representar o cliente, mas o token de representação não conterá nenhuma informação e não poderá ser usado.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY**</dt> <dt>2</dt> </dl>          | O servidor pode obter a identidade do cliente. O servidor pode representar o cliente para verificação de ACL, mas não pode acessar objetos do sistema como o cliente. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE**</dt> <dt>3</dt> </dl> | O processo do servidor pode representar o contexto de segurança do cliente ao agir em nome do cliente. Esse nível de representação pode ser usado para acessar recursos locais, tais como arquivos. Ao representar nesse nível, o token de representação só pode ser passado por um limite de computador. O [serviço de autenticação Schannel](schannel.md) dá suporte apenas a esse nível de representação. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ DELEGATE**</dt> <dt>4</dt> </dl>          | O processo do servidor pode representar o contexto de segurança do cliente ao agir em nome do cliente. O processo do servidor também pode fazer chamadas de saída para outros servidores enquanto age em nome do cliente, usando a desajuste. O servidor pode usar o contexto de segurança do cliente em outros computador para acessar recursos locais e remotos como o cliente. Ao representar nesse nível, o token de representação pode ser passado por qualquer número de limites do computador.<br/> |



## <a name="remarks"></a>Comentários

[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea) falhará durante a representação no nível de identificação. A solução alternativa é representar, chamar [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken), reverter, chamar [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)e, por fim, chamar [**LookupAccountSid.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) Usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), o cliente define o nível de representação

Usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), o cliente define o nível de representação e a identidade do proxy que estarão disponíveis quando um servidor chamar [**CoImpersonateClient.**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient) A identidade que o servidor verá quando a representação ocorrer é descrita em [Desajuste.](cloaking.md) Observe que, ao fazer uma chamada durante a representação, o chamador normalmente receberá o token de processo do chamador, não o token de representação do chamador. Para receber o token de representação do chamador, o chamador deve habilitar a redução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Camuflagem](cloaking.md)
</dt> </dl>

 

