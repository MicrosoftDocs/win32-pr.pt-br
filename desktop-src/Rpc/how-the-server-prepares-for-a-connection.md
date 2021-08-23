---
title: Como o servidor se prepara para uma conexão
description: Quando um programa de servidor inicia a execução, ele deve primeiro registrar a interface ou as interfaces que ele contém com a biblioteca em tempo de execução RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66314c55ad8e78922f7afcc74c6de3b4afad8234293373cf0cd35a560a1942ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929484"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Como o servidor se prepara para uma conexão

Quando um programa de servidor inicia a execução, ele deve primeiro registrar a interface ou as interfaces que ele contém com a biblioteca em tempo de execução RPC. Em seguida, ele cria as informações de associação necessárias. O programa de servidor também deve registrar o ponto de extremidade ou os pontos de extremidade que ele escuta. Em seguida, ele pode começar a escutar chamadas de cliente. Esse processo é ilustrado no diagrama a seguir.

![um aplicativo de servidor rpc se prepara para conexões de cliente](images/srvrcon.png)

Dependendo do design escolhido, um aplicativo de servidor pode escolher um conjunto diferente de etapas; o exemplo anterior e a ilustração fornece uma abordagem.

Esta seção apresenta informações sobre as etapas que um processo de servidor deve seguir para se preparar para uma conexão. A discussão é dividida nas seguintes seções:

-   [Registrando a interface](registering-the-interface.md)
-   [Disponibilizando o servidor na rede](making-the-server-available-on-the-network.md)
-   [Registrando pontos de extremidade](registering-endpoints.md)
-   [Escutando chamadas de cliente](listening-for-client-calls.md)

 

 




