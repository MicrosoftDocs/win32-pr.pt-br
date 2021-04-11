---
title: Como o servidor se prepara para uma conexão
description: Quando um programa de servidor começa a execução, ele deve primeiro registrar a interface ou as interfaces que ele contém com a biblioteca de tempo de execução RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292345"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Como o servidor se prepara para uma conexão

Quando um programa de servidor começa a execução, ele deve primeiro registrar a interface ou as interfaces que ele contém com a biblioteca de tempo de execução RPC. Em seguida, ele cria as informações de associação necessárias. O programa de servidor também deve registrar o ponto de extremidade ou os pontos de extremidades que ele ouve. Em seguida, ele pode começar a escutar chamadas do cliente. Esse processo é ilustrado no diagrama a seguir.

![um aplicativo de servidor RPC se prepara para conexões de cliente](images/srvrcon.png)

Dependendo do design escolhido, um aplicativo de servidor pode escolher um conjunto diferente de etapas; o exemplo anterior e a ilustração fornecem uma abordagem.

Esta seção apresenta informações sobre as etapas que um processo do servidor deve executar para se preparar para uma conexão. A discussão é dividida nas seguintes seções:

-   [Registrando a interface](registering-the-interface.md)
-   [Disponibilizando o servidor na rede](making-the-server-available-on-the-network.md)
-   [Registrando pontos de extremidade](registering-endpoints.md)
-   [Escutando chamadas de cliente](listening-for-client-calls.md)

 

 




