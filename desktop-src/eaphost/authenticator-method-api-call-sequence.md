---
title: Sequência de chamada da API do método Authenticator
description: Saiba mais sobre a sequência de chamadas da API do método autenticador. Consulte uma lista que demonstra a sequência de chamadas feitas por um EAPHost em um método de autenticador EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bb5c7d64bfe6e38ebb97550dc76fe8ffcae8176
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366716"
---
# <a name="authenticator-method-api-call-sequence"></a>Sequência de chamada da API do método Authenticator

Este tópico fornece a sequência de chamada específica para a API do método autenticador. Durante uma sessão de autenticação EAP típica, o EAPHost faz várias chamadas em um método EAP que implementam as APIs do método de autenticador EAPHost.

A lista a seguir demonstra a sequência de chamadas feitas pelo EAPHost em um método de autenticador EAP.

-   O autenticador EAP primeiro carrega a DLL do método EAP usado para a autenticação específica em um servidor de diretivas de rede (NPS) ou em outro servidor de autenticação.
-   Chama [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) no método com uma estrutura de [**\_ tipo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) preenchida para obter uma lista de ponteiros para funções implementadas na dll. As chamadas de função subsequentes pelos métodos de autenticador (servidor) são presumidas para serem implementadas na DLL.
-   Chama [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) para instruir a biblioteca de métodos EAP a se preparar para pelo menos uma sessão de autenticação usando esse método autenticador.
-   Chama [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) para estabelecer uma sessão de autenticação exclusiva.
-   Repete as etapas a seguir até que [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) indique que um resultado de autenticação está disponível.
    -   Chama [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) com um ponteiro para um pacote de solicitação para passar para o suplicante.
    -   Chama [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) para recuperar o pacote de resposta enviado pelo suplicante. Essa função retorna um código de **\_ ação de \_ \_ resposta \_ do autenticador de método EAP** que indica a próxima ação que o autenticador deve executar na sessão de autenticação EAP.
    -   Se o código de ação [for \_ resposta do autenticador do método EAP \_ \_ \_ responder](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), ele indicará que o método EAP tem os atributos disponíveis para o autenticador recuperar e passar para o método par. O autenticador chama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) para obter os vários atributos de autenticação EAP do método de autenticador EAP. Depois que o autenticador processa os atributos, ele chama [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) , que fornece atributos de autenticação EAP atualizados para definir no método de autenticador EAP. Essa função retorna um código de **\_ ação de \_ \_ resposta \_ do autenticador de método EAP** que determina a ação subsequente.
-   Se o código de ação [for \_ \_ resultado da \_ resposta \_ do autenticador do método EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), ele indicará que o autenticador determinou os resultados da sessão de autenticação e que esses resultados estão disponíveis para o EAPHost. O autenticador chama [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) e obtém os resultados da sessão de autenticação.
-   Isso é seguido por uma chamada para [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) para encerrar a sessão de autenticação.
-   Por fim, é feita uma chamada para [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) para descarregar a DLL do método autenticador.
-   Descarrega a biblioteca de métodos EAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ação de \_ resposta do autenticador do método EAP \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Sequência de chamadas da API suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Sequência de chamada da API do método par](peer-method-api-call-sequence.md)
</dt> <dt>

[Sequências de chamada EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




