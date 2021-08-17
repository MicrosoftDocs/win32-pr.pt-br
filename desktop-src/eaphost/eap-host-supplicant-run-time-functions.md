---
title: Funções Run-Time do suplicante EAPHost
description: Saiba mais sobre as funções de tempo de execução do suplicante do EAPHost, como EapHostPeerBeginSession e EapHostPeerGetResult.
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97481347535de03cb1d3c04f341f382c270f0ae89482060e9952c38cfbdc5b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785324"
---
# <a name="eaphost-supplicant-run-time-functions"></a>Funções Run-Time do suplicante EAPHost

As funções de tempo de execução da API suplicante EAP são as seguintes.



| Função                                                                     | Descrição                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | Inicia uma sessão de autenticação EAP.                                                                                                                                                                                |
| [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | Interrompe todos os retornos de chamada futuros para o [**NotificationHandler**](/previous-versions/windows/desktop/api) fornecido pelo suplicante de chamada para EAPHost em uma chamada anterior para [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession). |
| [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | Encerra uma sessão de autenticação EAP atual entre o EAPHost e o suplicante de chamada.                                                                                                                          |
| [**EapHostPeerFreeEapError**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | Libera toda a memória específica de erro EAP retornada pelas APIs EAPHost.                                                                                                                                                        |
| [**EapHostFreeRuntimeMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | Libera o espaço de memória usado por APIs de tempo de execução.                                                                                                                                                                         |
| [**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | Obtém o status de autenticação EAP atual do suplicante do EAPHost.                                                                                                                                             |
| [**EapHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | Solicita informações de identidade dos métodos internos.                                                                                                                                                                |
| [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | Obtém uma matriz de atributos de autenticação EAP do EAPHost.                                                                                                                                                      |
| [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | Obtém o resultado de autenticação para a sessão de autenticação EAP especificada.                                                                                                                                      |
| [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | Obtém um pacote do EAPHost para enviar ao autenticador.                                                                                                                                                          |
| [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | Obtém o contexto da interface do usuário para o suplicante do EAPHost que é usado nas APIs do [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) para o suplicante.                             |
| [**EapHostPeerInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | Inicializa o EAPHost para o suplicante. [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) e [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) devem ser chamados como um par.                                      |
| [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | Transfere o pacote EAP para EAPHost depois de ter recebido um pacote EAP do servidor.                                                                                                                             |
| [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | Fornece atributos de autenticação EAP atualizados para o EAPHost.                                                                                                                                                           |
| [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | Fornece um contexto de interface do usuário novo ou atualizado para o método EAP par carregado no EAPHost.                                                                                                                           |
| [**EapHostPeerUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Unitializes EapHost para o suplicante. [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) e [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) devem ser chamados como um par.                                      |



 

 

 




