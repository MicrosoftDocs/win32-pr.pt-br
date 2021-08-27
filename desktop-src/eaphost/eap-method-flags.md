---
title: Sinalizadores de método EAP (Eaptypes. h)
description: Os sinalizadores de método EAP são usados nas funções suplicante, autenticador e par para especificar comportamentos de uma sessão de autenticação EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91acce3b3829c947bfb6e705ad7e1f07b938a986bc6f6845a4c10a54b4f1992c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094406"
---
# <a name="eap-method-flags"></a>Sinalizadores de método EAP

Os sinalizadores de método EAP são usados nas funções suplicante, autenticador e par para especificar comportamentos de uma sessão de autenticação EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Sinalizador EAP \_ Reserved1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_sinalizador EAP \_ não \_ interativo**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Não exibir uma interface do usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_logon do sinalizador EAP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



os dados do usuário foram obtidos do logon Windows.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_visualização do sinalizador EAP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Mostrar a interface do usuário de credenciais antes de autenticar, mesmo que as credenciais armazenadas em cache estejam presentes.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ SINALIZADOR \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_autenticação do \_ computador do sinalizador EAP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Usar autenticação no nível do computador; não definir esse sinalizador indica que a autenticação de nível de usuário está sendo usada.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_acesso de \_ convidado do sinalizador EAP \_**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Indica uma solicitação para fornecer acesso de convidado.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Sinalizador EAP \_ Reserved3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ SINALIZADOR \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_ \_ retomada \_ do sinalizador EAP da \_ hibernação**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Indica que esta é a primeira chamada após a atividade do computador ter sido retomada de um período de hibernação.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ SINALIZADOR \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Sinalizador EAP \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ autenticação completa do sinalizador EAP \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Indica que os métodos de túnel devem executar uma autenticação completa em vez de uma versão abreviada, como [EAP protegido (PEAP) reconexão rápida](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**o \_ sinalizador \_ EAP \_ prefere \_ credenciais Alt**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que as credenciais passadas para [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) são preferenciais para todas as outras formas de recuperação de credencial, mesmo que os dados de configuração passados para a função atual solicitem um modo diferente de recuperação de credencial.

> [!Note]  
> Esse sinalizador só é usado pelo [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Sinalizador EAP \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**\_alteração do \_ estado de integridade do sinalizador EAP peer \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Indica que a causa da nova autenticação é um retorno de chamada NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ); A NAP iniciou a sessão de autenticação porque o estado de integridade foi alterado. Esse sinalizador deve ser enviado somente quando essa função é chamada por um retorno de chamada [*NotificationHandler*](/previous-versions/windows/desktop/api) específico de NAP fornecido por uma chamada anterior para essa função.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_ \_ interface do usuário suprimir sinalizador EAP \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Continue a autenticação com as informações disponíveis. Se a autenticação não puder continuar, falhará.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_pré- \_ \_ logon do sinalizador EAP**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que o EAPHost deve fornecer SSO (logon único). Para obter mais informações, consulte [SSO e PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_autenticação de \_ usuário do sinalizador EAP \_**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica a autenticação de nível de usuário para métodos herdados que não podem definir o **\_ sinalizador EAP \_ \_ auth**.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_sinalizador EAP \_ confg \_ ReadOnly**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Indica que a configuração pode ser exibida, mas não atualizada.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Sinalizador EAP \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Não use. Reservado para uso futuro.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes do EAPHost comuns](common-eap-host-error-constants.md)
</dt> </dl>

