---
title: Como o cliente estabelece uma conexão
description: Para estabelecer uma sessão de comunicação de cliente/servidor com um programa de servidor, os aplicativos cliente com identificadores explícitos precisam criar um identificador de associação.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005635"
---
# <a name="how-the-client-establishes-a-connection"></a>Como o cliente estabelece uma conexão

Para estabelecer uma sessão de comunicação de cliente/servidor com um programa de servidor, os aplicativos cliente com identificadores explícitos precisam criar um identificador de associação. Depois disso, a biblioteca de tempo de execução RPC localiza o computador que hospeda o programa do servidor. Em seguida, ele localiza o ponto de extremidade que o programa do servidor está ouvindo e direciona a chamada para ele. O diagrama a seguir ilustra esse processo.

![um cliente RPC estabelece uma conexão com um servidor RPC](images/clntcon.png)

Esta seção apresenta informações sobre como o cliente se conecta ao programa do servidor e executa procedimentos remotos que ele oferece. Há muitas abordagens para concluir essas etapas; dependendo do design escolhido, um aplicativo pode escolher um conjunto de etapas diferente. Este exemplo é simplesmente uma maneira de fazer isso.

A discussão é dividida nas seguintes seções:

-   [Criando um identificador de associação](creating-a-binding-handle.md)
-   [Fazendo uma chamada de procedimento remoto](making-a-remote-procedure-call.md)
-   [Localizando o programa do servidor](finding-the-server-program.md)
-   [Enviando a chamada para o programa do servidor](sending-the-call-to-the-server-program.md)

 

 




