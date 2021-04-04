---
title: Visão geral da API do SSO EAPHost
description: Fornece uma visão geral das APIs do EAPHost que dão suporte ao SSO (logon único).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007499"
---
# <a name="sso-eaphost-api-overview"></a>Visão geral da API do SSO EAPHost

Este tópico fornece uma visão geral das APIs do EAPHost que dão suporte ao SSO (logon único). Para cenários de SSO específicos, consulte [cenários do SSO EAPHost](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>Enumerações EAPHost

As seguintes enumerações dão suporte ao SSO.



| Nome                                                                    | Finalidade                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_tipo de \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Define um conjunto de possíveis tipos de campo de entrada disponíveis ao consultar as credenciais do usuário.    |
| [**\_tipo de \_ dados de interface do usuário interativa EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Especifica os tipos de dados de contexto de interface do usuário interativa fornecidos para determinadas chamadas à API do suplicante. |



 

## <a name="eaphost-structures"></a>Estruturas EAPHost

As seguintes estruturas de dados dão suporte ao SSO.



| Nome                                                                     | Finalidade                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dados do \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contém os dados associados a um único campo de entrada.                                                                                                                         |
| [**\_matriz de \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contém um conjunto de estruturas de [**dados de campo de \_ entrada de configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) que contêm coletivamente os dados de campo de entrada do usuário obtidos do usuário. |
| [**\_dados de \_ interface do usuário interativa EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contém informações de configuração para componentes de interface do usuário interativa gerados em um suplicante EAP.                                                                                   |
| [**Req. de \_ credenciais EAP \_**](eap-cred-req.md)                                   | Contém as credenciais EAP antigas e novas para operações de alteração de credencial.                                                                                               |
| [**\_resp de credenciais EAP \_**](eap-cred-resp.md)                                 | Contém as credenciais EAP antigas e novas para operações de alteração de credencial.                                                                                               |
| [**Req. de \_ expiração de credenciais EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contém as credenciais EAP antigas e novas para operações de expiração de credenciais.                                                                                                 |
| [**\_resp de \_ expiração de credenciais EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contém as credenciais EAP antigas e novas para operações de expiração de credenciais.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>APIs de mesmo nível (suplicante) do EAPHost

As funções suplicantes a seguir dão suporte a SSO.

As funções [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) e [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) são exclusivas do SSO.



| Nome                                                                                                             | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Pedido chamado |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Obtém os campos de entrada para componentes interativos da interface do usuário a serem gerados no suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Permite que o usuário determine que tipo de credenciais é exigido pelos métodos para executar a autenticação em um cenário de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Converte as informações do usuário em um BLOB do usuário que pode ser consumido por funções de tempo de execução do EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Obtém um BLOB de credenciais que pode ser usado para iniciar a autenticação a partir da entrada do usuário recebida pela IU do SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | O suplicante usa o sinalizador de **\_ pré- \_ \_ logon do sinalizador EAP** para indicar que o EAPHost deve fornecer SSO. Se o código de ação [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) for retornado, o EAPHost chamará [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e, em seguida, chamará [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Se o código de ação [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) não for retornado, o EAPHost continuará com a sequência de chamadas normal e não SSO. Para obter mais informações, consulte [sequência de chamadas à API suplicante](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>APIs do método par do EAPHost

As funções pares a seguir dão suporte ao SSO.

As funções [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) e [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) são exclusivas do SSO.



| Nome                                                                                                      | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Pedido chamado |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define a implementação de uma API do método EAP que fornece os campos de entrada para que os componentes da interface do usuário interativa sejam gerados no suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define a implementação de uma função específica de método EAP que obtém os campos de entrada de credencial de SSO EAP para esse método EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte as informações do usuário em um BLOB do usuário que pode ser consumido por funções de tempo de execução do EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define a implementação de uma função de método EAP que obtém os dados de BLOB do usuário fornecidos pela interface de usuário do SSO interativo gerada no suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | O sinalizador de **\_ pré- \_ \_ logon do sinalizador EAP** indica que o EAPHost deve fornecer SSO. Em um cenário de SSO, se o código de ação **EapPeerResponseInvokeUI** for retornado, o EAPHost chamará [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e, em seguida, chamará [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Se o código de ação **EapPeerResponseInvokeUI** não for retornado, o EAPHost continuará com a sequência de chamadas normal e não SSO. Para obter mais informações, consulte [sequência de chamadas da API do método par](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Cenários do SSO EAPHost](why-eaphost-sso.md)
</dt> </dl>

 

