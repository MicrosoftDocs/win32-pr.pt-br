---
title: Sobre a publicação de serviço
description: Um serviço é um aplicativo que torna os dados ou as operações disponíveis para os clientes de rede. Geralmente, um serviço é implementado como um serviço formal baseado em Win32 da Microsoft, mas isso não é necessário.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915852"
---
# <a name="about-service-publication"></a>Sobre a publicação de serviço

Um serviço é um aplicativo que torna os dados ou as operações disponíveis para os clientes de rede. Geralmente, um serviço é implementado como um serviço formal baseado em Win32 da Microsoft, mas isso não é necessário.

A publicação de serviço é o ato de criar e manter dados sobre uma ou mais instâncias de um determinado serviço para que os clientes de rede possam localizar e usar o serviço. A publicação de um serviço no Active Directory Domain Services permite que clientes e administradores se movam de uma exibição centrada em computador do sistema distribuído para uma exibição centrada em serviços.

**Sistemas operacionais Microsoft Windows NT 3,51 e posteriores:** Um sistema distribuído era um grupo de computadores que executam vários serviços. Para acessar um serviço, um aplicativo exigiu dados sobre quais computadores ofereciam o serviço.

**Windows 2000 Server, windows 2000 Advanced Server e windows 2000 Datacenter Server:** Os serviços publicam sua existência usando Active Directory Domain Services objetos. Os objetos contêm informações de associação que os aplicativos cliente usam para se conectar a instâncias do serviço. Para acessar um serviço, um cliente não precisa saber sobre computadores específicos: os objetos em um servidor de Active Directory incluem essas informações. Um cliente consulta o servidor de Active Directory para um objeto que representa um serviço (chamado de objeto de ponto de conexão) e usa os dados de associação do objeto para se conectar ao serviço.

A tabela a seguir mostra exemplos de associações.



| Serviço      | Associação                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serviço de arquivos | Nome UNC de um compartilhamento. Por exemplo, " \\ \\ meuservidor \\ mysharename".                                                                                                                                                              |
| Serviço Web  | URL. Por exemplo, " https://www.fabrikam.com ".                                                                                                                                                                                 |
| Serviço RPC  | Associação de RPC (chamada de procedimento remoto): informações especiais codificadas usadas para se conectar ao servidor RPC. As associações RPC podem ser convertidas de e para cadeias de caracteres com as APIs RPC. Por exemplo: "ncacn \_ IP \_ TCP:Server. fabrikam. com". |



 

Em um sistema distribuído, os computadores são mecanismos e as entidades interessantes são os serviços que estão disponíveis. Da perspectiva do usuário, a identidade do computador que fornece um serviço específico não é importante. O que é importante é acessar o próprio serviço.

Esse também é o caso com o gerenciamento de serviços. O administrador de uma determinada zona DNS não está interessado nos computadores que executam o serviço DNS; o administrador deseja administrar o DNS. Provavelmente, haverá várias instâncias do serviço DNS, uma das quais é autoritativo. Os computadores que oferecem suporte ao serviço DNS não são importantes para o administrador de DNS. O que é importante é como gerenciar o serviço como um único recurso distribuído — não como processos individuais em execução em computadores diferentes.

 

 




