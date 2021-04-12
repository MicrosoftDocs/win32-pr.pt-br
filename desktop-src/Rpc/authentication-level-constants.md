---
title: Constantes de Authentication-Level (rpcdce. h)
description: As constantes de nível de autenticação representam níveis de autenticação passados para várias funções de tempo de execução.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499691"
---
# <a name="authentication-level-constants"></a>Constantes em nível de autenticação

As constantes de nível de autenticação representam níveis de autenticação passados para várias funções de tempo de execução. Esses níveis são listados em ordem crescente de autenticação. Cada novo nível adiciona à autenticação fornecida pelo nível anterior. Se a biblioteca de tempo de execução RPC não oferecer suporte ao nível especificado, ela será automaticamente atualizada para o próximo nível de suporte mais alto.



| Constante                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**\_padrão de \_ nível de autenticação RPC C \_ \_**</dt> </dl>                    | Usa o nível de autenticação padrão para o serviço de autenticação especificado.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ nível \_ nenhum**</dt> </dl>                             | Não executa nenhuma autenticação.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**\_conexão em \_ nível de autenticação RPC C \_ \_**</dt> </dl>                    | Realiza a autenticação somente quando o cliente estabelece uma relação com um servidor.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**\_chamada de \_ nível de autenticação RPC C \_ \_**</dt> </dl>                             | Autentica somente no início de cada chamada de procedimento remoto quando o servidor recebe a solicitação. Não se aplica a chamadas de procedimento remoto feitas usando as sequências de protocolo baseadas em conexão (aquelas que começam com o prefixo "ncacn"). Se a sequência de protocolo em um identificador de associação for uma sequência de protocolo baseada em conexão e você especificar esse nível, essa rotina usará a \_ constante do PCT do nível de autenticação RPC C \_ \_ \_ .<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**\_PCT do \_ nível de autenticação RPC C \_ \_**</dt> </dl>                                | Autentica somente que todos os dados recebidos são do cliente esperado. Não valida os dados em si.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**\_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C**</dt> </dl> | Autentica e verifica se nenhum dos dados transferidos entre o cliente e o servidor foi modificado.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**\_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C**</dt> </dl>       | Inclui todos os níveis anteriores e garante que os dados de texto não criptografados só possam ser vistos pelo remetente e pelo destinatário. No caso local, isso envolve o uso de um canal seguro. No caso remoto, isso envolve a criptografia do valor do argumento de cada chamada de procedimento remoto.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Comentários

Independentemente do valor especificado pela constante, **Ncalrpc** sempre usa a privacidade do \_ PCT de nível de autenticação RPC C \_ \_ \_ \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





