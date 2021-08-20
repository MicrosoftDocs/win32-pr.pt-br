---
title: Implementando o mecanismo LEAP do EAPHost
description: Descreve o mecanismo EAPHost que permite que terceiros escrevam módulos LEAP (Lightweight Extensible Authentication Protocol) para Windows.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b98deca674b74a33151a73f65620cf038a12c6e8f3fedd0816567a26aa4fcd86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719953"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>Implementando o mecanismo LEAP do EAPHost

Este tópico descreve o mecanismo EAPHost que permite que terceiros escrevam módulos LEAP (Lightweight Extensible Authentication Protocol) para Windows. O LEAP é um método de autenticação herdado, criado pela Cisco, de acordo com a [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016). Para obter mais informações sobre o LEAP, consulte [Cisco LEAP Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018).

## <a name="eaphost-authentication-process"></a>Processo de autenticação do EAPHost

O processo de autenticação normal do EAPHost ocorre da seguinte maneira:

-   O autenticador envia uma solicitação para autenticar o par. Por exemplo, o aplicativo chama [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) com a configuração do EAPHost e os dados do usuário.
-   O par envia um pacote de resposta em resposta a uma solicitação válida. Por exemplo, uma chamada bem-sucedida retorna um identificador de sessão de **\_ \_ identificador de sessão EAP** .
-   O autenticador envia um pacote de solicitação adicional e o par responde com uma resposta. Por exemplo, o aplicativo chama [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) para obter pacotes EAP recebidos pelo EAPHost em toda a sessão. Cada pacote é processado por uma chamada para [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket).
-   [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) sempre retornará um código de ação. O suplicante deve então chamar a função correspondente ao código de ação.
-   A sequência de solicitações e respostas continua desde que seja necessário. Por exemplo, o aplicativo pode chamar [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) para solicitar os atributos de EAP disponíveis e o par responde com [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) para retorná-los.
-   Após uma solicitação inicial, uma nova solicitação não poderá ser enviada até que uma resposta válida seja recebida.
-   A conversa continua até que o autenticador não possa autenticar o par; nesse caso, a implementação do autenticador deve transmitir uma falha de EAP. Por exemplo, respostas inaceitáveis para uma ou mais solicitações farão com que o autenticador transmita uma falha de EAP de código 4.
-   Como alternativa, a conversa de autenticação pode continuar até que o autenticador determine que a autenticação bem-sucedida tenha ocorrido; nesse caso, o autenticador deve transmitir um êxito de EAP (código 3).
-   Se o resultado indica êxito ou falha, o aplicativo chama [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) para encerrar a sessão. No caso de falha, a nova autenticação pode ser tentada abrindo outra sessão com o EAPHost e fornecendo a mesma identidade ou uma nova.

### <a name="leap-authentication-process"></a>Processo de autenticação LEAP

O processo de autenticação LEAP difere do processo de autenticação normal do EAPhost da seguinte maneira:

-   A autenticação EAP é iniciada pelo servidor (autenticador). O LEAP, por outro lado, é iniciado pelo cliente (par).
    -   Portanto, ao escrever um módulo LEAP, você deve sempre garantir que o pacote de solicitação de desafio do método par e a resposta EAP do servidor EAP sempre devem ter a mesma ID de pacote do pacote de êxito EAP do servidor.

    <!-- -->

    -   Em contraste, os pacotes de solicitação e resposta EAPHost e com êxito normalmente têm IDs diferentes.
        > [!Note]  
        > Cada solicitação de EAP tem um campo de tipo para indicar o que está sendo solicitado. Assim como ocorre com o pacote de solicitação, cada pacote de resposta EAP contém um campo tipo, que corresponde ao campo tipo da solicitação. Os exemplos incluem solicitação de identidade e pacotes de solicitação de desafio.

         

-   No caso de falha com o EAPHost, a nova autenticação pode ser tentada abrindo outra sessão com o EAPHost e fornecendo a mesma identidade ou uma nova identidade.

### <a name="leap-authenticator-method-implementation"></a>implementação do método LEAP Authenticator

Ao desenvolver um método de autenticador LEAP, verifique o seguinte:

-   Os métodos do autenticador LEAP devem retornar o código de ação [**\_ \_ \_ \_ Enviar resposta do autenticador do método EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) após a primeira fase de autenticação (autenticação de mesmo nível) bem-sucedida. Em seguida, quando [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) é chamado, ele deve retornar um [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) válido com um código EAP de [**EapCodeSuccess**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode).
-   Os métodos do autenticador LEAP devem retornar o código de ação do [**\_ \_ autenticador \_ \_ do método EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) se a primeira fase da autenticação de mesmo nível não for bem-sucedida.
-   Os métodos do autenticador LEAP devem retornar o pacote de resposta de autenticação final com o código de ação [](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) do resultado da [**\_ resposta de \_ autenticador \_ \_ do método EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) quando EapMethodAuthenticatorSendPacket é chamado. Em seguida, em chamadas subsequentes para [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) , o **\_ \_ identificador de sessão EAP** deve ser retornado para identificar a sessão autenticada.
-   

### <a name="leap-peer-method-implementation"></a>Implementação do método de par LEAP

Ao desenvolver um método de par bissexto, verifique o seguinte

-   Os métodos de par LEAP devem retornar o código de ação [**EapPeerMethodResponseActionSend**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) após a primeira fase de autenticação (autenticação de mesmo nível) bem-sucedida.
-   Os métodos de pares LEAP devem retornar o código de ação [**EapPeerMethodResponseActionResult**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) depois que a 2ª fase de autenticação for bem-sucedida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequência de chamadas EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> </dl>

 

 




