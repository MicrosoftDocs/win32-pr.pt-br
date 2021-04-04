---
title: Noções básicas de segurança RPC
description: Para concluir qualquer chamada de procedimento remoto, todos os aplicativos distribuídos devem criar uma associação entre o cliente e o servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822943"
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

 

 




