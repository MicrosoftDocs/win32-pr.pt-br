---
title: Sobre a publicação de serviço
description: Um serviço é um aplicativo que disponibiliza dados ou operações para clientes de rede. Geralmente, um serviço é implementado como um serviço formal baseado no Microsoft Win32, mas isso não é necessário.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3945107125df04bbdb862d476d0aba78711ba8f89622c732e0d6ae53d65d1eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840901"
---
# <a name="about-service-publication"></a>Sobre a publicação de serviço

Um serviço é um aplicativo que disponibiliza dados ou operações para clientes de rede. Geralmente, um serviço é implementado como um serviço formal baseado no Microsoft Win32, mas isso não é necessário.

A publicação de serviço é o ato de criar e manter dados sobre uma ou mais instâncias de um determinado serviço para que os clientes de rede possam encontrar e usar o serviço. Publicar um serviço no Active Directory Domain Services permite que clientes e administradores se movam de uma exibição centrada no computador do sistema distribuído para uma exibição centrada no serviço.

**Microsoft Windows NT 3.51 e sistemas operacionais posteriores:** Um sistema distribuído era um grupo de computadores que executam vários serviços. Para acessar um serviço, um aplicativo exigia dados sobre quais computadores ofereciam o serviço.

**Windows 2000 Server, Windows 2000 Advanced Server e Windows 2000 Datacenter Server:** Os serviços publicam sua existência usando Active Directory Domain Services objetos. Os objetos contêm informações de associação que os aplicativos cliente usam para se conectar a instâncias do serviço. Para acessar um serviço, um cliente não precisa saber sobre computadores específicos: os objetos em um servidor do Active Directory incluem essas informações. Um cliente consulta o servidor do Active Directory para um objeto que representa um serviço (chamado de objeto de ponto de conexão) e usa os dados de associação do objeto para se conectar ao serviço.

A tabela a seguir mostra exemplos de vinculações.



| Serviço      | Associação                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serviço de arquivos | Nome UNC para um compartilhamento. Por exemplo, \\ \\ "MyServer \\ MyshareName".                                                                                                                                                              |
| Serviço Web  | Url. Por exemplo, " https://www.fabrikam.com ".                                                                                                                                                                                 |
| Serviço RPC  | Associação RPC (chamada de procedimento remoto) : informações codificadas especiais usadas para se conectar ao servidor RPC. As vinculações RPC podem ser convertidas de e para cadeias de caracteres com as APIs RPC. Por exemplo: "ncacn \_ ip \_ tcp:server.fabrikam.com". |



 

Em um sistema distribuído, os computadores são mecanismos e as entidades interessantes são os serviços disponíveis. Da perspectiva do usuário, a identidade do computador que fornece um serviço específico não é importante. O que é importante é acessar o próprio serviço.

Esse também é o caso com o gerenciamento de serviços. O administrador de uma determinada zona DNS não está interessado nos computadores que executam o serviço DNS; o administrador deseja administrar o DNS. Provavelmente haverá várias instâncias do serviço DNS, uma das quais é autoritativa. Os computadores que suportam o serviço DNS não são importantes para o administrador dns. O que é importante é como gerenciar o serviço como um único recurso distribuído, não como processos individuais em execução em computadores diferentes.

 

 




