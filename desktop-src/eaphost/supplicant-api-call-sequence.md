---
title: Sequência de chamadas da API suplicante
description: Saiba mais sobre a sequência de chamadas da API suplicante. Consulte uma visão geral da sequência de chamadas e exiba recursos adicionais disponíveis.
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917694"
---
# <a name="supplicant-api-call-sequence"></a>Sequência de chamadas da API suplicante

Este tópico fornece a sequência de chamada específica para a API suplicante.

## <a name="supplicant-api-call-sequence-overview"></a>Visão geral da sequência de chamadas da API suplicante

Quando o suplicante recebe um pacote EAP de um provedor, como um ponto de acesso, normalmente ocorre o seguinte fluxo de chamada à API suplicante.

-   O aplicativo chama [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) com dados de configuração e dados de usuário do EAPHost. Uma chamada bem-sucedida retorna um identificador de sessão de **\_ \_ identificador de sessão EAP** .
-   Cada pacote recebido pelo suplicante é processado por uma chamada para [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket). Em seguida, o suplicante chama a função correspondente ao código de ação retornado pela função.
-   Se o código de ação for **EapHostPeerResponseSend**, o suplicante chamará [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) para obter a resposta a ser enviada ao autenticador.
-   Se, durante a sessão, o código de ação retornado ao suplicante for **EapHostPeerResponseRespond**, ele indicará que os atributos EAP estão disponíveis. O suplicante então chama [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) para obtê-los. Esses atributos contêm dados complementares usados durante o processo de autenticação. Depois que o suplicante concluir o processamento dos atributos, ele chama [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) que atualiza os dados. Essa função retorna um código de ação que determina a próxima ação do suplicante.
-   Se o código de ação for **EapHostPeerResponseInvokeUI** , o suplicante gerará uma caixa de diálogo de interface do usuário para obter dados interativos do usuário, como credenciais ou informações de identidade. Confira interação do usuário com o fluxo de chamadas à API suplicante abaixo.
-   Se o código de ação for **EapHostPeerResponseResult**, isso indica que os resultados da sessão de autenticação estão disponíveis para o suplicante. O suplicante então chama [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) para obter os resultados. Independentemente de os resultados indicarem êxito ou falha, o suplicante chama [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession). No caso de falha, a nova autenticação pode ser tentada abrindo outra sessão com o EAPHost e fornecendo uma nova identidade ou tentando a autenticação com a identidade original novamente.

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a>Interação do usuário com o fluxo de chamadas da API suplicante

Em determinados casos, o suplicante precisa obter informações do usuário para continuar o processo de autenticação.

A lista a seguir demonstra a sequência de chamadas no suplicante e o processo de interface do usuário do EAPHost necessários para habilitar a entrada interativa.

1.  O suplicante Obtém o contexto da interface do usuário atual chamando [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext).
2.  O suplicante envia os dados de contexto da interface do usuário para o processo de interface do usuário do suplicante.
    > [!Note]  
    > O processo de interface do usuário, que normalmente coleta a interface do usuário ou manipula a interface do usuário interativa, é separado do processo suplicante. Separar os dois processos não é um requisito do EAPHost, mas isso tem a vantagem de permitir que o processo da interface do usuário interaja com a área de trabalho.

     

3.  Se o suplicante quiser renderizar a interface do usuário por si só, ele chamará a função [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) para obter os campos de entrada para que os componentes interativos da interface do usuário sejam gerados. Caso contrário, ele segue o modelo tradicional de invocar a interface de usuário interativa do método chamando [ **EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)
    > [!Note]  
    > Se [**a \_ operação do método EAP E \_ EAPHost \_ \_ \_ sem \_ suporte**](eap-related-error-and-information-constants.md) for retornada, o suplicante deverá seguir o modelo tradicional de invocar a interface de usuário interativa do método chamando [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui). Se houver um erro, [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) retornará um código de retorno diferente de **NULL**.

     

4.  Se o suplicante chama [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) ou [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) , o processo da interface do usuário passa os dados de contexto existentes e carrega Eappcfg.dll. A interface do usuário apropriada é gerada para coletar os novos dados. Os novos dados de contexto de interface do usuário, que agora podem conter entrada do usuário, são copiados e os dados de contexto antigos são liberados com uma chamada para [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory).
5.  O processo da interface do usuário retorna os novos dados de contexto para o suplicante, que chama [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) para defini-lo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequência de chamada da API do método par](peer-method-api-call-sequence.md)
</dt> <dt>

[Sequência de chamada da API do método Authenticator](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Sequência de chamadas EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Suplicantes do EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




