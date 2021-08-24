---
description: Contém informações sobre o perfil de conexão 802.1 X usado no momento para autenticação 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Estrutura de ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500e714b6f0728104987f53ff0a8c0e7083c1af5996679a78a986b5674d54514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684886"
---
# <a name="onex_connection_profile-structure"></a>Estrutura de perfil de \_ conexão Onex \_

A estrutura de **\_ \_ perfil de conexão Onex** contém informações sobre o perfil de conexão 802.1 x usado atualmente para autenticação 802.1 x.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

A versão desta estrutura **de \_ \_ perfil de conexão Onex** .

</dd> <dt>

**dwTotalLen**
</dt> <dd>

O comprimento, em bytes, dessa estrutura **de \_ \_ perfil de conexão Onex** .

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwOneXSupplicantFlags** .

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

Indica se a estrutura de **\_ \_ perfil de conexão Onex** contém dados válidos no membro **suplicante** .

</dd> <dt>

**fauthMode**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **AuthMode** .

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwHeldPeriod** .

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwAuthPeriod** .

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwStartPeriod** .

</dd> <dt>

**fMaxStart**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwMaxStart** .

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwMaxAuthFailures** .

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwNetworkAuthTimeout** .

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **bAllowLogonDialogs** .

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwNetworkAuthWithUITimeout** .

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **bUserBasedVLan** .

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

Um conjunto de sinalizadores 802.1 X que podem estar presentes no perfil. Esses sinalizadores são reservados para uso interno pelo módulo de autenticação 802.1 X.

</dd> <dt>

**suplicable**
</dt> <dd>

O elemento suplicamode no esquema 802.1 X que especifica o método de transmissão usado para EAPOL-Start mensagens. Para obter mais informações, consulte o [**elemento suplicante (Onex)**](onexschema-supplicantmode-onex-element.md) no esquema 802.1 x.



| Valor                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start mensagens não são transmitidas. Válido somente para perfis de LAN com fio.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | O cliente determina quando enviar EAPOL-Start pacotes com base na capacidade de rede. EAPOL-Start mensagens são enviadas somente quando necessário. Válido somente para perfis de LAN com fio.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start mensagens são transmitidas conforme especificado pelo 802.1 X. Válido para perfis de LAN com e sem fio.<br/>                                                             |



 

</dd> <dt>

**AuthMode**
</dt> <dd>

O elemento AuthMode no esquema 802.1 X que especifica o tipo de credenciais usado para autenticação 802.1 X. Para obter mais informações, consulte o [**elemento AuthMode (Onex)**](onexschema-authmode-onex-element.md) no esquema 802.1 x.



| Valor                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Use as credenciais do computador ou do usuário. Quando um usuário faz logon, as credenciais do usuário são usadas para autenticação. Quando nenhum usuário está conectado, as credenciais do computador são usadas.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Use somente as credenciais do computador.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Usar somente as credenciais do usuário.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Use somente credenciais de convidado (vazias).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | As credenciais a serem usadas não estão especificadas.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

O elemento heldPeriod no esquema 802.1 X que especifica o período de tempo, em segundos, no qual um cliente não tentará realizar a autenticação novamente após uma tentativa de autenticação com falha. Para obter mais informações, consulte o [**elemento heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) no esquema 802.1 x.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

O elemento authPeriod no esquema 802.1 X que especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador. Se uma resposta não for recebida dentro do período especificado, o cliente assumirá que não há um autenticador presente na rede. Para obter mais informações, consulte o [**elemento authPeriod (Onex)**](onexschema-authperiod-onex-element.md) no esquema 802.1 x.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

O elemento startPeriod no esquema 802.1 X que especifica o período de tempo, em segundos, a aguardar antes de um EAPOL-Start ser enviado. Uma mensagem de EAPOL-Start é enviada para iniciar o processo de autenticação 802.1 X. Para obter mais informações, consulte o [**elemento startPeriod (Onex)**](onexschema-startperiod-onex-element.md) no esquema 802.1 x.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

O elemento maxStart no esquema 802.1 X que especifica o número máximo de EAPOL-Start mensagens enviadas. Depois que o número máximo de mensagens de EAPOL-Start tiver sido enviado, o cliente assumirá que não há um autenticador presente na rede. Para obter mais informações, consulte o [**elemento maxStart (Onex)**](onexschema-maxstart-onex-element.md) no esquema 802.1 x.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

O elemento maxAuthFailures no esquema 802.1 X que especifica o número máximo de falhas de autenticação permitidas para um conjunto de credenciais. Para obter mais informações, consulte o elemento [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) no esquema 802.1 x.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

O tempo, em segundos, para aguardar a conclusão da autenticação 802.1 X antes de o logon normal continuar. Esse valor é usado em cenários de logon único (SSO). Esse valor usa como padrão 10 segundos em um perfil 802.1 X. Para obter mais informações, consulte o [**elemento maxDelay (logon único)**](onexschema-maxdelay-singlesignon-element.md) no esquema 802.1 x.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

O tempo de duração máximo, em segundos, para aguardar uma conexão caso uma caixa de diálogo de interface do usuário que requer entrada do usuário seja exibida durante o SSO por logon.

no Windows Vista com SP1 e posterior, esse valor é codificado para 10 minutos e não é configurável. na versão Windows Vista para fabricação, esse valor usa como padrão 60 segundos em um perfil 802.1 x e foi controlado pelo elemento **maxDelayWithAdditionalDialogs** no esquema.

no Windows Vista com SP1 e posterior, o elemento **maxDelayWithAdditionalDialogs** no esquema 802.1 x é ignorado e preterido.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Um valor que especifica se as caixas de diálogo EAP devem ser exibidas ao usar o SSO pré-logon. Para obter mais informações, consulte o elemento **allowAdditionalDialogs** no esquema 802.1 x.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

O elemento userBasedVirtualLan no esquema 802.1 X que especifica se a VLAN (LAN virtual) usada pelo dispositivo muda com base nas credenciais do usuário. Alguns dispositivos de NAS (servidor de acesso à rede) alteram a VLAN após a autenticação de um usuário. Quando userBasedVirtualLan for TRUE, o NAS poderá alterar a VLAN de um dispositivo após a autenticação de um usuário. Para obter mais informações, consulte o [**elemento userBasedVirtualLan (logon único)**](onexschema-userbasedvirtuallan-singlesignon-element.md) no esquema 802.1 x.

</dd> </dl>

## <a name="remarks"></a>Comentários

a estrutura do **\_ \_ perfil de conexão ONEX** é usada pelo módulo 802.1 x, um novo componente de configuração sem fio com suporte no Windows Vista e posterior.

Os [**\_ dados de \_ atualização \_ do resultado Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contêm informações sobre uma alteração de status para a autenticação 802.1 x. A estrutura de dados de atualização de resultado de Onex é retornada quando o membro de **notificação** da estrutura de [**\_ \_ dados de notificação**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) de WLAN é  **802.1x de origem de notificação de WLAN \_ \_ \_** e o membro NotificationCode da estrutura de **dados de \_ notificação \_ de WLAN** para notificação recebida é OneXNotificationTypeResultUpdate. **\_ \_ \_** Para essa notificação, o membro **pData** da estrutura **de \_ \_ dados de notificação de WLAN** aponta para uma estrutura de **\_ \_ \_ dados de atualização de resultado de Onex** que contém informações sobre a alteração do status de autenticação 802.1 x.

Se o membro **fOneXAuthParams** na estrutura [**de \_ \_ \_ dados de atualização de resultado de Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) for definido, o membro **authParams** da estrutura de **\_ \_ \_ dados de atualização do resultado de Onex** conterá uma estrutura de [**\_ \_ Blob variável de Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) com uma estrutura de [**\_ \_ parâmetros de autenticação Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) inserida a partir do membro **dwOffset** do **\_ \_ BLOB da variável Onex**. O membro **oneXConnProfile** da estrutura **de \_ \_ parâmetros de autenticação Onex** contém uma estrutura de **\_ \_ Blob variável de Onex** com uma estrutura de **\_ \_ perfil de conexão Onex** inserida a partir do membro **dwOffset** do **\_ \_ BLOB da variável Onex**.

A estrutura do **\_ \_ perfil de conexão Onex** não está definida em um arquivo de cabeçalho público.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre a arquitetura do ACM](about-the-acm-architecture.md)
</dt> <dt>

[Esquema OneX](onexschema-schema.md)
</dt> <dt>

[**Elemento AuthMode (OneX)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**Elemento authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**Elemento heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**Elemento maxStart (OneX)**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**Elemento startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**Elemento suplicable (OneX)**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**Elemento userBasedVirtualLan (logon único)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**\_parâmetros de autenticação Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**\_tipo de notificação Onex \_**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**\_dados de \_ atualização de resultados de Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**Elemento de esquema OneX**](onexschema-onex-element.md)
</dt> <dt>

[**\_BLOB da variável de Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**\_dados de notificação da WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
