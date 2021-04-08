---
description: 'Saiba mais sobre: adicionando tabelas ao banco de dados'
title: Adicionando tabelas ao banco de dados
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920646"
---
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="9f665-103">Adicionando tabelas ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="9f665-103">Adding Tables to the Database</span></span>


<span data-ttu-id="9f665-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9f665-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="9f665-105">Adicionando tabelas ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="9f665-105">Adding Tables to the Database</span></span>

<span data-ttu-id="9f665-106">As tabelas são uma coleção heterogênea de registros que agrupam de forma física e lógica os dados no banco de dado.</span><span class="sxs-lookup"><span data-stu-id="9f665-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="9f665-107">As tabelas são identificadas exclusivamente por seu nome.</span><span class="sxs-lookup"><span data-stu-id="9f665-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="9f665-108">A ID da tabela ([JET_TABLEID](./jet-tableid.md)) é um identificador para um cursor que é usado para atualizar e navegar em tabelas.</span><span class="sxs-lookup"><span data-stu-id="9f665-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="9f665-109">Você pode abrir vários [JET_TABLEID](./jet-tableid.md) na mesma tabela.</span><span class="sxs-lookup"><span data-stu-id="9f665-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="9f665-110">Uma tabela existente é aberta na chamada para [JetOpenTable](./jetopentable-function.md), e uma nova tabela é criada sem linhas ou colunas com [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f665-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="9f665-111">Para criar atomicamente uma tabela com um conjunto inicial de colunas e índices, chame [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f665-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="9f665-112">O tamanho inicial da tabela é fornecido no parâmetro *lPages* em [JetCreateTable](./jetcreatetable-function.md) ou no membro **ulPages** da estrutura [JET_TABLECREATE](./jet-tablecreate-structure.md) na chamada para [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f665-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="9f665-113">As tabelas crescem automaticamente quando os dados são adicionados à tabela.</span><span class="sxs-lookup"><span data-stu-id="9f665-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="9f665-114">O crescimento é proporcional ao tamanho inicial da tabela.</span><span class="sxs-lookup"><span data-stu-id="9f665-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="9f665-115">As colunas podem ser adicionadas à tabela a qualquer momento com [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f665-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="9f665-116">Quando o aplicativo não precisar mais acessar a tabela, o cursor poderá ser fechado com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f665-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="9f665-117">A tabela pode ser excluída por meio de uma chamada para [JetDeleteTable](./jetdeletetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f665-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="9f665-118">As operações de tabela devem ser executadas dentro do contexto de uma transação.</span><span class="sxs-lookup"><span data-stu-id="9f665-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f665-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9f665-119">See Also</span></span>

[<span data-ttu-id="9f665-120">Transações</span><span class="sxs-lookup"><span data-stu-id="9f665-120">Transactions</span></span>](./transactions.md)
