---
title: Noções básicas de segurança RPC
description: Para concluir qualquer chamada de procedimento remoto, todos os aplicativos distribuídos devem criar uma associação entre o cliente e o servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed8bce6f97ecfc7bd257d20eebbb35d068624fe017c01a662b47fceb463b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926027"
---
# <a name="rpc-security-essentials"></a>Noções básicas de segurança RPC

Para concluir qualquer chamada de procedimento remoto, todos os aplicativos distribuídos devem criar uma associação entre o cliente e o servidor. Para obter mais informações sobre associações, consulte [associação e identificadores](binding-and-handles.md). Para concluir uma chamada de procedimento remoto segura, são necessárias etapas adicionais. Primeiro, o servidor deve escolher um provedor de segurança (serviço de autenticação na terminologia do DCE). Em seguida, ele deve decidir seu mecanismo de autenticação. Depois disso, o cliente obtém uma associação ao servidor e solicita uma chamada de procedimento remoto segura a partir do tempo de execução do RPC e especifica várias opções de segurança, como provedor de segurança, opções de QOS de segurança e assim por diante.

Esta seção explica os conceitos essenciais e as informações necessárias para usar as funções RPC para criar um cliente e um servidor para um aplicativo distribuído autenticado. Ele é organizado nos seguintes tópicos:

-   [Nomes de entidade](principal-names.md)
-   [Níveis de autenticação](authentication-levels.md)
-   [Serviços de autenticação](authentication-services.md)
-   [Credenciais de autenticação de cliente](client-authentication-credentials.md)
-   [Serviços de autorização](authorization-services.md)
-   [Qualidade de Serviço](quality-of-service.md)
-   [Funções de autorização](authorization-functions.md)
-   [Funções de aquisição de chave](key-acquisition-functions.md)
-   [Client Impersonation (em inglês)](client-impersonation.md)

 

 




