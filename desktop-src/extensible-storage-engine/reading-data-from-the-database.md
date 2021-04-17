---
description: 'Saiba mais sobre: lendo dados do banco'
title: Lendo dados do banco de dados
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780147"
---
# <a name="reading-data-from-the-database"></a><span data-ttu-id="d53bf-103">Lendo dados do banco de dados</span><span class="sxs-lookup"><span data-stu-id="d53bf-103">Reading Data from the Database</span></span>


<span data-ttu-id="d53bf-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d53bf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="d53bf-105">Lendo dados do banco de dados</span><span class="sxs-lookup"><span data-stu-id="d53bf-105">Reading Data from the Database</span></span>

<span data-ttu-id="d53bf-106">A leitura de dados do Database deve ser executada em uma transação.</span><span class="sxs-lookup"><span data-stu-id="d53bf-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="d53bf-107">O procedimento a seguir mostra como executar uma operação de leitura simples no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d53bf-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="d53bf-108">Para ler dados de um banco de dado</span><span class="sxs-lookup"><span data-stu-id="d53bf-108">To read data from a database</span></span>

1.  <span data-ttu-id="d53bf-109">Chame [JetBeginTransaction](./jetbegintransaction-function.md) ou [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) com a ID de sessão para iniciar a transação.</span><span class="sxs-lookup"><span data-stu-id="d53bf-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="d53bf-110">Mova o cursor para o registro desejado chamando [JetMove](./jetmove-function.md) com JET_MoveFirst no parâmetro de *galinha* .</span><span class="sxs-lookup"><span data-stu-id="d53bf-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="d53bf-111">Para obter mais informações sobre como mover o cursor, consulte o tópico [indexação na tabela](./indexing-in-the-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d53bf-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="d53bf-112">Chame [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) no registro atual com JET_ColInfo especificado no parâmetro *InfoLevel* para recuperar a ID de coluna para a coluna.</span><span class="sxs-lookup"><span data-stu-id="d53bf-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="d53bf-113">A ID da coluna é retornada na estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d53bf-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="d53bf-114">Leia os dados da coluna chamando [JetRetrieveColumn](./jetretrievecolumn-function.md) com a ID de coluna recuperada na etapa 3 no parâmetro columnid.</span><span class="sxs-lookup"><span data-stu-id="d53bf-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="d53bf-115">O parâmetro *pvData* contém o tipo de dados especificado na estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) recuperada na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="d53bf-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="d53bf-116">Chame [JetCommitTransaction](./jetcommittransaction-function.md) para confirmar a transação para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d53bf-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
