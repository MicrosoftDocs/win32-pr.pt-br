---
description: 'Saiba mais sobre: sobre o mecanismo de armazenamento extensível'
title: Sobre o mecanismo de armazenamento extensível
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920647"
---
# <a name="about-extensible-storage-engine"></a>Sobre o mecanismo de armazenamento extensível


_**Aplica-se a:** Exchange Server 2013 | Windows | Windows Server_

## <a name="about-extensible-storage-engine"></a>Sobre o mecanismo de armazenamento extensível

O ESE (mecanismo de armazenamento extensível) é um mecanismo de banco de dados que armazena informações em uma sequência lógica. As informações podem ser recuperadas em sequência ou por meio do acesso a índices definidos. As atualizações no banco de dados são implementadas com uma transação para garantir operações seguras. O ESE permite o acesso simultâneo a vários bancos de dados, incluindo bancos de dados de arquivos de log de transações que podem ser usados para recuperação do sistema. O ESE é escalonável para aplicativos grandes ou pequenos. Os recursos a seguir estão disponíveis com a API (interface de programação de aplicativo) do ESE:

  - Backup e restauração: um aplicativo pode fazer cópias consistentes do estado de dados enquanto está online e modificando o estado de dados ativamente.

  - Navegação do cursor: o aplicativo pode navegar com o cursor para acessar os dados em sequência ou usando índices.

  - Banco de dados: uma coleção de tabelas que são submetidas a backup e restauradas como uma única unidade.

  - Log e recuperação de falhas: a API ESE garante que a consistência de dados definida pelo aplicativo seja respeitada mesmo no caso de uma falha do sistema.

  - Tables: a estrutura fundamental do banco de dados ESE que é usada para armazenar o dado.

  - Transação: o mecanismo de banco de dados ESE fornece transações ACID (duráveis consistentemente isoladas) que permitem que os aplicativos recuperem dados somente de Estados de dados confiáveis e mantém a consistência dos dados no caso de um encerramento de processo inesperado ou desligamento do sistema.

  - Escalonável: o aplicativo pode criar bancos de dados tão grandes quanto 100 GB ou tão pequenos quanto 1MB.

