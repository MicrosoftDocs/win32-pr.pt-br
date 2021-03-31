---
title: Funções de Run-Time do método par do EAPHost
description: Saiba mais sobre as funções de tempo de execução da API do método par do EAPHost. Consulte uma lista de funções e exiba recursos adicionais disponíveis.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfde4adc8d509fcd5d67f9a33bd0617d605716db
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823984"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Funções de Run-Time do método par do EAPHost

As funções de tempo de execução da API do método peer do EAP são as seguintes.



| Função                                                                   | Descrição                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Inicia uma nova sessão de autenticação no mesmo nível EAPHost.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Encerra uma sessão de autenticação EAP atual entre o EAPHost e o par.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Permite que os desenvolvedores de métodos EAP forneçam as várias propriedades de conexão e propriedades de usuário com suporte pelo método. O EAPHost invoca essa função para criar a propriedade de conexão e a propriedade de usuário do método EAP. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Obtém a identidade para o método EAP que está chamando.                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Obtém um conjunto de ponteiros de função para uma implementação do método de par EAP carregado.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Obtém uma matriz de atributos EAP do método EAP.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Obtém um pacote de resposta do método EAP.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Obtém o resultado de uma sessão de autenticação do método EAP.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Obtém o contexto da interface do usuário do método EAP.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Inicializa o EAPHost para o método par.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Processa um pacote recebido pelo EAPHost de um suplicante.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Fornece credenciais de usuário novas ou atualizadas para o método EAP.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Fornece uma matriz atualizada de atributos EAP para o método EAP.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Fornece um contexto de interface do usuário para o método EAP.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Desliga o método EAP e se prepara para descarregar sua DLL correspondente.                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de configuração do método de emparelhamento EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




