---
description: Um aplicativo de servidor fornece serviços aos clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Controle de acesso de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c943d9d1e1f1cc5dcc405f49ab200aa30618f7eefb86c7f26342f005f23249fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782721"
---
# <a name="clientserver-access-control"></a>Controle de acesso de cliente/servidor

Um aplicativo de servidor fornece serviços aos clientes. Por exemplo, um servidor pode executar os seguintes serviços em nome de um cliente:

-   Salvar e recuperar informações de um banco de dados privado
-   Acessar recursos de rede
-   Iniciar [*processos*](/windows/desktop/SecGloss/p-gly) no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do cliente no computador do servidor

Um servidor protegido controla o acesso a seus serviços. Windows fornece suporte de segurança que permite que um servidor faça o seguinte:

-   Representar o contexto de [*segurança*](/windows/desktop/SecGloss/s-gly)de um cliente, o que faz com que o sistema execute a maioria das verificações de [*privilégio*](/windows/desktop/SecGloss/p-gly) e acesso no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do cliente, em vez de no servidor
-   Fazer logon de um cliente no computador do servidor
-   Conexão aos recursos de rede usando o contexto de segurança do cliente
-   Criar [*descritores de segurança*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados
-   Determinar se um descritor de segurança permite acesso a um cliente
-   Determinar se um conjunto de privilégios está habilitado no token de um cliente
-   Gerar mensagens de auditoria no log de eventos de segurança para registrar tentativas de um cliente para acessar objetos ou usar privilégios

 

 
