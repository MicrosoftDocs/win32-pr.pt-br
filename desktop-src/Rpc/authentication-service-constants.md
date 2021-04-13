---
title: Constantes de Authentication-Service (rpcdce. h)
description: As constantes do serviço de autenticação representam os serviços de autenticação passados para várias funções de tempo de execução.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
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
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499690"
---
# <a name="authentication-service-constants"></a>Authentication-Service constantes

As constantes do serviço de autenticação representam os serviços de autenticação passados para várias funções de tempo de execução.

As constantes a seguir são valores válidos para o parâmetro *AuthnSvc* .



| Constante/valor                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ None**</dt> <dt>0</dt> </dl>                              | Sem autenticação.<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_ privado**</dt> <dt>1</dt> </dl>        | Use a autenticação de chave privada de DCE (ambiente de computação distribuída).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_**</dt> <dt>2</dt> </dl>           | Autenticação de chave pública do DCE (reservada para uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ Dec \_ público**</dt> <dt>4</dt> </dl>           | Autenticação de chave pública DEC (reservada para uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Negotiate**</dt> <dt>9</dt> </dl>  | Use o [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate). Esse SSP negocia entre o uso dos provedores de suporte de segurança de protocolo NTLM e Kerberos (SSP).<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ Authn \_ WinNT**</dt> <dt>10</dt> </dl>                          | Use o [SSP do Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Use o [SSP do Schannel](/windows/desktop/SecAuthN/secure-channel). Esse SSP dá suporte ao protocolo SSL, à tecnologia de comunicação privada (PCT) e ao protocolo TLS.<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Use o [SSP do Microsoft Kerberos](/windows/desktop/SecAuthN/microsoft-kerberos).<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ Authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Usar a autenticação de senha distribuída (DPA).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ Authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Protocolo de autenticação SSP usado para a rede da Microsoft (MSN).<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ Authn \_ Digest**</dt> <dt>21</dt> </dl>                       | Windows XP ou posterior: usar o [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ Nego de \_ extensão C Authn**</dt> <dt>30</dt> </dl> | Windows 7 ou posterior: reservado. Não usar<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ Authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Esse SSP fornece um wrapper compatível com SSPI para o protocolo de nível de transporte do MSMQ (fila de mensagens da Microsoft).<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ Authn \_ padrão**</dt> <dt>0xFFFFFFFF</dt> </dl>            | Use o serviço de autenticação padrão.<br/>                                                                                                                                   |



## <a name="remarks"></a>Comentários

Especifique \_ o RPC C \_ Authn \_ None para desativar a autenticação para chamadas de procedimento remoto feitas em um identificador de associação. Quando você especifica \_ \_ o padrão RPC c Authn \_ , a biblioteca de tempo de execução RPC usa o \_ serviço de autenticação RPC c \_ Authn \_ WinNT para chamadas de procedimento remoto feitas usando o identificador de associação.

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

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

