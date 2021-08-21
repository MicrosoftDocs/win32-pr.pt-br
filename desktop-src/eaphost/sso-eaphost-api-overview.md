---
title: Visão geral da API do SSO EAPHost
description: Fornece uma visão geral das APIs do EAPHost que suportam SSO (logon único).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a38c6dd35dd2506f8aa26412b09db0f9c9951241bd0f017ed5e55d7f5484b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085870"
---
# <a name="sso-eaphost-api-overview"></a>Visão geral da API do SSO EAPHost

Este tópico fornece uma visão geral das APIs do EAPHost que suportam SSO (logon único). Para cenários de SSO específicos, consulte [Cenários de SSO EAPHost.](why-eaphost-sso.md)

## <a name="eaphost-enumerations"></a>Enumerações EAPHost

As enumerações a seguir são suportadas por SSO.



| Nome                                                                    | Finalidade                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**TIPO DE CAMPO \_ DE ENTRADA DE \_ \_ CONFIGURAÇÃO DE \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Define um conjunto de possíveis tipos de campo de entrada disponíveis ao consultar credenciais de usuário.    |
| [**TIPO DE \_ DADOS DA INTERFACE DO USUÁRIO INTERATIVA \_ \_ DO \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Especifica os tipos de dados de contexto de interface do usuário interativos fornecidos para determinadas chamadas à API flexíveis. |



 

## <a name="eaphost-structures"></a>Estruturas EAPHost

As estruturas de dados a seguir são suportadas por SSO.



| Nome                                                                     | Finalidade                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DADOS DO CAMPO \_ DE ENTRADA DE \_ \_ CONFIGURAÇÃO DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contém os dados associados a um único campo de entrada.                                                                                                                         |
| [**MATRIZ DE CAMPOS \_ DE \_ ENTRADA DE \_ CONFIGURAÇÃO DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contém um conjunto de estruturas de DADOS DE CAMPO DE ENTRADA DE CONFIGURAÇÃO [**\_ \_ \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) que contêm coletivamente os dados de campo de entrada do usuário obtidos do usuário. |
| [**DADOS \_ \_ INTERATIVOS DA INTERFACE DO USUÁRIO DO EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contém informações de configuração para componentes interativos da interface do usuário gerados em um componente de EAP.                                                                                   |
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                   | Contém as credenciais EAP novas e antigas para operações de alteração de credencial.                                                                                               |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                 | Contém as credenciais EAP novas e antigas para operações de alteração de credencial.                                                                                               |
| [**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contém as credenciais de EAP novas e antigas para operações de expiração de credencial.                                                                                                 |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contém as credenciais de EAP novas e antigas para operações de expiração de credencial.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>APIs de par EAPHost (supplicant)

As funções de suporte a seguir são suportadas por SSO.

As [**funções EapHostPeerQueerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) [**e EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) são exclusivas do SSO.



| Nome                                                                                                             | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Ordem chamada |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Obtém os campos de entrada para componentes interativos da interface do usuário a serem gerados no suplílico.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Permite que o usuário determine que tipo de credenciais são exigidas pelos métodos para executar a autenticação em um cenário de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Converte informações do usuário em um BLOB de usuário que pode ser consumido por funções de tempo de executar EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Obtém um BLOB de credenciais que pode ser usado para iniciar a autenticação da entrada do usuário recebida pela interface do usuário do SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | O suplicant usa o sinalizador **PRE \_ \_ \_ LOGON** do SINALIZADOR de EAP para indicar que o EAPHost deve fornecer SSO. Se o código de ação [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) for retornado, EAPHost chamará [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e [**chamará EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Se o [código de ação EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) não for retornado, o EAPHost prosseguirá com a sequência de chamada regular, não SSO. Para obter mais informações, consulte [Supplicant API Call Sequence](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>APIs de método par EAPHost

As funções de par a seguir são suportadas por SSO.

As [**funções EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) [**e EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) são exclusivas do SSO.



| Nome                                                                                                      | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Ordem chamada |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define a implementação de uma API de método EAP que fornece os campos de entrada para componentes interativos da interface do usuário a serem gerados no suplicant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define a implementação de uma função específica do método EAP que obtém os campos de entrada de credencial de SSO do EAP para esse método EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte informações do usuário em um BLOB de usuário que pode ser consumido por funções de tempo de executar EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define a implementação de uma função de método EAP que obtém os dados de BLOB do usuário fornecidos pela interface do usuário interativa do SSO gerado no suplicant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | O **sinalizador PRE \_ \_ \_ LOGON** do SINALIZADOR de EAP indica que o EAPHost deve fornecer SSO. Em um cenário de SSO, se o código de ação **EapPeerResponseInvokeUI** for retornado, o EAPHost [**chamará EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e [**chamará EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Se o **código de ação EapPeerResponseInvokeUI** não for retornado, o EAPHost prosseguirá com a sequência de chamada regular, não SSO. Para obter mais informações, consulte [Sequência de chamada da API de Método Par](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Cenários de SSO EAPHost](why-eaphost-sso.md)
</dt> </dl>

 

