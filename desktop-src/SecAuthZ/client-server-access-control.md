---
description: Um aplicativo de servidor fornece serviços aos clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Controle de acesso de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750098"
---
# <a name="clientserver-access-control"></a>Controle de acesso de cliente/servidor

Um aplicativo de servidor fornece serviços aos clientes. Por exemplo, um servidor pode executar os seguintes serviços em nome de um cliente:

-   Salvar e recuperar informações de um banco de dados privado
-   Acessar recursos de rede
-   Iniciar [*processos*](/windows/desktop/SecGloss/p-gly) no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do cliente no computador do servidor

Um servidor protegido controla o acesso a seus serviços. O Windows fornece suporte de segurança que permite que um servidor faça o seguinte:

-   Representar o contexto de [*segurança*](/windows/desktop/SecGloss/s-gly)de um cliente, o que faz com que o sistema execute a maioria das verificações de [*privilégio*](/windows/desktop/SecGloss/p-gly) e acesso no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do cliente, em vez de no servidor
-   Fazer logon de um cliente no computador do servidor
-   Conectar-se a recursos de rede usando o contexto de segurança do cliente
-   Criar [*descritores de segurança*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados
-   Determinar se um descritor de segurança permite acesso a um cliente
-   Determinar se um conjunto de privilégios está habilitado no token de um cliente
-   Gerar mensagens de auditoria no log de eventos de segurança para registrar tentativas de um cliente para acessar objetos ou usar privilégios

 

 
