---
title: Sequência de chamada da API de Método Par
description: Saiba mais sobre a sequência de chamada da API de método par. Consulte uma lista que demonstra a sequência de chamadas feitas por um EAPHost em um método par de EAP.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042784"
---
# <a name="peer-method-api-call-sequence"></a>Sequência de chamada da API de Método Par

Este tópico fornece a sequência de chamada específica para a API de método par. Durante uma sessão de autenticação EAP típica, o EAPHost faz várias chamadas em métodos EAP para implementar a API de método par EAPHost.

A lista a seguir demonstra a sequência de chamadas feitas por EAPHost em um método par de EAP.

-   Carrega a DLL de método par de EAP usada para a autenticação.
-   Chama [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) no método para obter uma lista de ponteiros para funções implementadas na DLL. As chamadas de função subsequentes pelo par EAPHost (cliente) são assumidas como implementadas na DLL.
-   Chama [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) para instruir a Biblioteca de Métodos EAP a se preparar para pelo menos uma sessão de autenticação usando esse método par.
-   Chama [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) para estabelecer uma sessão de autenticação exclusiva.
-   Chama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) para obter a identidade a ser usada para autenticação. Se a identidade não estiver disponível ou se o usuário tiver que fornecer informações adicionais, o EAPHost chamará [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Essa função obtém as informações de contexto da caixa de diálogo da interface do usuário que serão ativas no suplicant. Depois que o usuário enviar as informações de identidade, a identidade do usuário será definida com uma chamada para [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)e obtida por uma chamada para **EapPeerGetIdentity**.
-   Repete as etapas a seguir até [**que EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) indique que um resultado de autenticação está disponível.
    -   Chama [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) com o ponteiro de um pacote de solicitação para passar para o suplicant.
    -   Chama **EapPeerGetResponsePacket** para recuperar o pacote de resposta a ser enviado ao autenticador.
    -   Opcionalmente, se os atributos de EAP precisam ser recuperados ou enviados durante a sessão de autenticação, EAPHost chama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) [**e EapPeerSetResponseAttributes,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) respectivamente.
-   Quando o autenticador envia um código de ação que indica que a autenticação está concluída, O EAPHost chama [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) e obtém os resultados da autenticação.
-   Chama [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) para encerrar a sessão de autenticação.
-   Chama [**EapPeerShutdown para**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) descarregar a DLL do método par.
-   Descarrega a Biblioteca de Métodos EAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequência de chamada de API flexível](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator Sequência de chamada da API de Método](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Sequências de chamada EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




