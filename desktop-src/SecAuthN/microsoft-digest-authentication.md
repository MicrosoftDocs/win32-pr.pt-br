---
description: Microsoft Digest executa uma autenticação inicial quando o servidor recebe a primeira resposta de desafio de um cliente.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticação do Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747648"
---
# <a name="microsoft-digest-authentication"></a>Autenticação do Microsoft Digest

Microsoft Digest executa uma autenticação inicial quando o servidor recebe a primeira resposta de desafio de um cliente. O servidor verifica se o cliente não foi autenticado e, em seguida, executa a autenticação inicial acessando os serviços de um controlador de domínio. Para obter uma descrição detalhada desse procedimento, consulte [autenticação inicial usando Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Quando a autenticação inicial for bem-sucedida, o servidor receberá uma [*chave de sessão*](../secgloss/s-gly.md)de resumo. O servidor armazena em cache essa chave e a usa para autenticar solicitações subsequentes de recursos do cliente. Essa autenticação é local, ou seja, não requer acesso a um controlador de domínio. Para obter uma descrição detalhada desse procedimento, consulte [Autenticando solicitações subsequentes usando Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Ao usar HTTP, não há nenhuma conexão mantida entre o cliente e o servidor. Para reduzir o tráfego do controlador de domínio e melhorar o desempenho, o Microsoft Digest armazena em cache as informações recebidas após a autenticação bem-sucedida. Para obter informações sobre esse processo, consulte [mantendo o contexto de segurança entre conexões](maintaining-the-security-context-between-connections.md).

 

 
