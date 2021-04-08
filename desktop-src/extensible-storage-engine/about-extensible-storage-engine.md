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
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="8b35d-103">Sobre o mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="8b35d-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="8b35d-104">_**Aplica-se a:** Exchange Server 2013 | Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8b35d-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="8b35d-105">Sobre o mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="8b35d-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="8b35d-106">O ESE (mecanismo de armazenamento extensível) é um mecanismo de banco de dados que armazena informações em uma sequência lógica.</span><span class="sxs-lookup"><span data-stu-id="8b35d-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="8b35d-107">As informações podem ser recuperadas em sequência ou por meio do acesso a índices definidos.</span><span class="sxs-lookup"><span data-stu-id="8b35d-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="8b35d-108">As atualizações no banco de dados são implementadas com uma transação para garantir operações seguras.</span><span class="sxs-lookup"><span data-stu-id="8b35d-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="8b35d-109">O ESE permite o acesso simultâneo a vários bancos de dados, incluindo bancos de dados de arquivos de log de transações que podem ser usados para recuperação do sistema.</span><span class="sxs-lookup"><span data-stu-id="8b35d-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="8b35d-110">O ESE é escalonável para aplicativos grandes ou pequenos.</span><span class="sxs-lookup"><span data-stu-id="8b35d-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="8b35d-111">Os recursos a seguir estão disponíveis com a API (interface de programação de aplicativo) do ESE:</span><span class="sxs-lookup"><span data-stu-id="8b35d-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="8b35d-112">Backup e restauração: um aplicativo pode fazer cópias consistentes do estado de dados enquanto está online e modificando o estado de dados ativamente.</span><span class="sxs-lookup"><span data-stu-id="8b35d-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="8b35d-113">Navegação do cursor: o aplicativo pode navegar com o cursor para acessar os dados em sequência ou usando índices.</span><span class="sxs-lookup"><span data-stu-id="8b35d-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="8b35d-114">Banco de dados: uma coleção de tabelas que são submetidas a backup e restauradas como uma única unidade.</span><span class="sxs-lookup"><span data-stu-id="8b35d-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="8b35d-115">Log e recuperação de falhas: a API ESE garante que a consistência de dados definida pelo aplicativo seja respeitada mesmo no caso de uma falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="8b35d-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="8b35d-116">Tables: a estrutura fundamental do banco de dados ESE que é usada para armazenar o dado.</span><span class="sxs-lookup"><span data-stu-id="8b35d-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="8b35d-117">Transação: o mecanismo de banco de dados ESE fornece transações ACID (duráveis consistentemente isoladas) que permitem que os aplicativos recuperem dados somente de Estados de dados confiáveis e mantém a consistência dos dados no caso de um encerramento de processo inesperado ou desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="8b35d-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="8b35d-118">Escalonável: o aplicativo pode criar bancos de dados tão grandes quanto 100 GB ou tão pequenos quanto 1MB.</span><span class="sxs-lookup"><span data-stu-id="8b35d-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

