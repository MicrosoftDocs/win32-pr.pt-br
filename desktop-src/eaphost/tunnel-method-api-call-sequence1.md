---
title: Sequência de chamada da API do método de túnel
description: Saiba mais sobre a sequência de chamadas de API para métodos de túnel. Consulte uma visão geral e exiba recursos adicionais disponíveis.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294516"
---
# <a name="tunnel-method-api-call-sequence"></a>Sequência de chamada da API do método de túnel

Este tópico aborda a sequência de chamadas de API para métodos de túnel

## <a name="tunnel-method-call-sequence-overview"></a>Visão geral da sequência de chamada do método de túnel

Quando o suplicante recebe solicitação para dados de usuário e identidade de usuário, normalmente ocorre o seguinte fluxo de chamada de API.

-   O suplicante chama EapHostPeerProcessReceivedPacket no EapHost para processar o pacote recebido do autenticador.
-   Ao processar esse pacote, o EAPHost o determina como pacote IdentityRequest e chama o [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) no método de túnel para obter a identidade do usuário a ser usada para autenticação.
-   Se o método de túnel precisar obter a identidade do usuário a partir do método interno, ele chamará [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) no EAPHost interno que, por sua vez, chamará [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) no método interno.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Interação do usuário com o fluxo de chamadas da API dos métodos de túnel

Em determinados casos, quando a identidade não está disponível ou quando o usuário deve fornecer informações adicionais, o método EAP gera uma caixa de diálogo de interface do usuário no suplicante.

Nesses casos, a seqüência de chamada a seguir normalmente ocorre para obter informações diretamente do usuário.

-   O método EAP de túnel retorna o código de ação para invocar a interface do usuário para EapHost. O suplicante chama [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)para obter as informações de contexto da interface do usuário atual para a caixa de diálogo interface do usuário.
-   Em seguida, o suplicante chama [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Essa função usa as informações de contexto da interface do usuário para gerar uma interface de usuários interativa que é usada para obter informações de credenciais do usuário. O processo da interface do usuário carrega Eappcfg.dll e obtém os ponteiros para EapPeerInvokeInteractiveUI e EapPeerFreeMemory.
    > [!Note]  
    > O processo de interface do usuário normalmente coleta a interface do usuário ou manipula a interface do usuário interativa e é separado do processo suplicante. Separar os dois processos não é um requisito do EAPHost, mas isso tem a vantagem de permitir que o processo da interface do usuário interaja com a área de trabalho.

     

-   O EapHost chama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) no método de túnel para obter informações de identidade do usuário.
-   Para obter a identidade do usuário do método interno, o método de túnel chama [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) no EAPHost interno.
-   O EAPHost interno chama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) no método interno para invocar a IU de identidade do usuário.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fornece uma nova ou atualizada informações de contexto de interface do usuário para o método EAP peer carregado no EAPHost depois que a interface do usuário é gerada.

O diagrama a seguir explica a sequência de chamadas de API para métodos de túnel

![sequência de chamadas de API de métodos de túnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequência de chamadas EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Sequência de chamadas da API suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Referência de API do suplicante EAPHost](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




