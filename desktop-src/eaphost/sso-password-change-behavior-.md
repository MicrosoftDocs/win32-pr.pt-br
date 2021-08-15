---
title: Comportamento de alteração de senha de SSO
description: Fornece uma abordagem passo a passo para resolver o comportamento de alteração de senha de SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438dd41466809805f159fde4a2db698d11b1f7899e48e1f96ccce2c811111cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042794"
---
# <a name="sso-password-change-behavior"></a>Comportamento de alteração de senha de SSO

Este tópico fornece uma abordagem passo a passo para resolver o comportamento de alteração de senha de SSO.

## <a name="step-by-step-approach"></a>Abordagem passo a passo

A lista a seguir representa uma abordagem passo a passo para resolver o comportamento de alteração de senha de SSO.

-   Depois que o método EAP é notificado sobre uma alteração de senha, o método notifica o EAPHost; O EAPHost, por sua vez, notifica o suplicante retornando o código de ação, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   Depois de receber o código de ação [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) do EAPHost, o suplicante Obtém o contexto da interface do usuário do método EAP chamando a função [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) ; O EAPHost Obtém o contexto da interface do usuário do método EAP chamando a função de método correspondente
-   O suplicante passa o contexto da interface do usuário para o processo de interface do usuário (usando alguma forma de comunicação entre processos).
-   O processo da interface do usuário chama [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) no EAPHost.
-   O EAPHost coleta o contexto da interface do usuário chamando [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) no método EAP.
-   O método EAP fornece todas as informações de contexto da interface do usuário na estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , em que *DwDataType* é definido como *EapCredExpiryReq* e *PbUiData* aponta para uma estrutura do tipo req. do [**EAP de \_ credenciais \_**](eap-cred-req.md).
-   Ao preencher a estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , esse método EAP só preencherá o parâmetro *curCreds* e não definirá o sinalizador [**\_ \_ \_ \_ \_ \_ somente leitura das propriedades do campo de entrada da interface de usuário do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) na estrutura de **\_ \_ \_ \_ dados do campo de entrada de configuração EAP** .
    > [!Note]  
    > O [**sinalizador \_ \_ \_ \_ \_ \_ somente leitura das propriedades do campo de entrada da interface do usuário do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) é para os campos de membro que precisam ser alterados.

     

-   Depois de coletar o contexto de interface do usuário informtion, o processo da interface do usuário renderiza uma interface de usuário para coletar informações de alteração de senha. Essas informações são populadas no parâmetro *NewCreds* da estrutura de [**\_ \_ \_ req expiração de credenciais EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .
-   O processo da interface do usuário passa a estrutura [**\_ \_ resp de credenciais de EAP**](eap-cred-resp.md) de volta para o EAPHost por meio de [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   O processo de IU passa esse BLOB do usuário para o suplicante, e o suplicante continua com as funções de tempo de execução do EAPHost como de costume.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cenários do SSO EAPHost](why-eaphost-sso.md)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




