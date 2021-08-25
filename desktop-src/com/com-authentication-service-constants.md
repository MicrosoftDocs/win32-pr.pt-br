---
title: Constantes do serviço de autenticação (RpcDce. h)
description: Define os serviços de autenticação identificando o pacote de segurança que fornece o serviço, como NTLMSSP, Kerberos ou Schannel.
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14cf6f0ab42b03d028d52df8160cad286e8c37af3988d8ca3b9736dad538012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993776"
---
# <a name="authentication-service-constants"></a>Constantes do serviço de autenticação

Define os serviços de autenticação identificando o pacote de segurança que fornece o serviço, como NTLMSSP, Kerberos ou Schannel.



| Constante/valor                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ None**</dt> <dt>0</dt> </dl>                              | Sem autenticação.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_ privado**</dt> <dt>1</dt> </dl>        | Autenticação de chave privada DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_**</dt> <dt>2</dt> </dl>           | Autenticação de chave pública do DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ Dec \_ público**</dt> <dt>4</dt> </dl>           | Autenticação de chave pública DEC. Reservado para uso futuro.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Negotiate**</dt> <dt>9</dt> </dl>  | Provedor de suporte de segurança do Snego.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ Authn \_ WinNT**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Provedor de suporte de segurança Schannel. Esse serviço de autenticação dá suporte a SSL 2,0, SSL 3,0, TLS e PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Provedor de suporte de segurança Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ Authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Provedor de suporte de segurança DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ Authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Provedor de suporte de segurança do MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ \_ \_ Kernel b Authn**</dt> <dt>20</dt> </dl>                       | Provedor de suporte de segurança de kernel.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ Authn \_ Digest**</dt> <dt>21</dt> </dl>                       | Provedor de suporte de segurança Digest.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ Nego de \_ extensão C Authn**</dt> <dt>30</dt> </dl> | Provedor de suporte de segurança do extensor NEGO.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ Authn \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Provedor de suporte de segurança do PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ Authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Provedor de suporte de segurança do MQ.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ Authn \_ padrão**</dt> <dt>0xffffffffl</dt> </dl>           | O serviço de autenticação padrão do sistema. Quando esse valor é especificado, o COM usa seu algoritmo normal de negociação ampla de segurança para escolher um serviço de autenticação. Para obter mais informações, consulte [negociação de cobertura de segurança](security-blanket-negotiation.md). <br/> |



## <a name="remarks"></a>Comentários

Essas constantes são usadas no [**serviço de \_ autenticação \_ exclusivo**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) e nas estruturas de [**\_ \_ informações de autenticação exclusivas**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) . A estrutura de **\_ \_ serviço de autenticação exclusiva** é passada pelo servidor para a função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e pode ser recuperada pela função [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Um ponteiro para uma **única estrutura de \_ \_ informações de autenticação** é passado pelo cliente para **CoInitializeSecurity**. Para obter mais informações sobre os pacotes de segurança identificados por esses valores, como NTLMSSP e Kerberos, consulte [com e pacotes de segurança](com-and-security-packages.md).

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

 

