---
title: Sequência de chamada da API do método par
description: Saiba mais sobre a sequência de chamadas da API do método par. Consulte uma lista que demonstra a sequência de chamadas feitas por um EAPHost em um método EAP peer.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac9be0f6de228fd5b1ebf2d2c28320baf76e914
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084900"
---
# <a name="peer-method-api-call-sequence"></a>Sequência de chamada da API do método par

Este tópico fornece a sequência de chamada específica para a API do método par. Durante uma sessão de autenticação EAP típica, o EAPHost faz várias chamadas em métodos EAP para implementar a API do método par do EAPHost.

A lista a seguir demonstra a sequência de chamadas feitas pelo EAPHost em um método EAP peer.

-   Carrega a DLL do método EAP peer usado para a autenticação.
-   Chama [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) no método para obter uma lista de ponteiros para funções implementadas na dll. Presume-se que as chamadas de função subsequentes do par (cliente) EAPHost sejam implementadas na DLL.
-   Chama [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) para instruir a biblioteca de métodos EAP a se preparar para pelo menos uma sessão de autenticação usando esse método par.
-   Chama [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) para estabelecer uma sessão de autenticação exclusiva.
-   Chama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) para obter a identidade a ser usada para autenticação. Se a identidade não estiver disponível ou se o usuário precisar fornecer informações adicionais, o EAPHost chamará [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Essa função obtém as informações de contexto para a caixa de diálogo da interface do usuário que será gerada no suplicante. Depois que o usuário tiver enviado as informações de identidade, a identidade do usuário será definida com uma chamada para [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)e obtida por uma chamada para **EapPeerGetIdentity**.
-   Repete as etapas a seguir até que [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) indique que um resultado de autenticação está disponível.
    -   Chama [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) com o ponteiro de um pacote de solicitação para passar para o suplicante.
    -   Chama **EapPeerGetResponsePacket** para recuperar o pacote de resposta a ser enviado ao autenticador.
    -   Opcionalmente, se os atributos EAP precisarem ser recuperados ou enviados durante a sessão de autenticação, o EAPHost chamará [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) e [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) , respectivamente.
-   Quando o autenticador envia um código de ação que indica que a autenticação está concluída, o EAPHost chama [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) e obtém os resultados da autenticação.
-   Chama [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) para encerrar a sessão de autenticação.
-   Chama [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) para descarregar a DLL do método par.
-   Descarrega a biblioteca de métodos EAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequência de chamadas da API suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Sequência de chamada da API do método Authenticator](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Sequências de chamada EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




