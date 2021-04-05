---
description: Como o instalador usa um banco de dados relacional, há funções para fazer consultas de linguagem SQL (SQL) para o banco de dados. O procedimento a seguir descreve como usar o SQL para consultar um banco de dados.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Trabalhando com consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921957"
---
# <a name="working-with-queries"></a><span data-ttu-id="e889b-104">Trabalhando com consultas</span><span class="sxs-lookup"><span data-stu-id="e889b-104">Working with Queries</span></span>

<span data-ttu-id="e889b-105">Como o instalador usa um banco de dados relacional, há funções para fazer consultas de linguagem SQL (SQL) para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e889b-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="e889b-106">O procedimento a seguir descreve como usar o SQL para consultar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e889b-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="e889b-107">**Para consultar um banco de dados com SQL**</span><span class="sxs-lookup"><span data-stu-id="e889b-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="e889b-108">Abra o objeto [**View**](view-object.md) , com a instrução SQL apropriada, chamando a função [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="e889b-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="e889b-109">Um objeto [**View**](view-object.md) é a tabela lógica criada pela aplicação de uma consulta a um conjunto de tabelas.</span><span class="sxs-lookup"><span data-stu-id="e889b-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="e889b-110">As consultas SQL devem aderir à [sintaxe SQL](sql-syntax.md) fornecida pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="e889b-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="e889b-111">Essa instrução SQL pode conter marcadores de parâmetro que não são especificados até que o objeto de **exibição** seja executado.</span><span class="sxs-lookup"><span data-stu-id="e889b-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="e889b-112">Execute o objeto [**View**](view-object.md) chamando a função [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .</span><span class="sxs-lookup"><span data-stu-id="e889b-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="e889b-113">Recupere o próximo registro de um objeto [**View**](view-object.md) chamando a função [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .</span><span class="sxs-lookup"><span data-stu-id="e889b-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="e889b-114">Modifique o objeto [**View**](view-object.md) chamando a função [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .</span><span class="sxs-lookup"><span data-stu-id="e889b-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="e889b-115">Você também pode validar dados com o [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) passando os sinalizadores apropriados.</span><span class="sxs-lookup"><span data-stu-id="e889b-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="e889b-116">Se **MsiViewModify** retornar \_ dados inválidos \_ de erro de uma solicitação de validação, os dados subjacentes serão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="e889b-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="e889b-117">Obtenha informações detalhadas de erro no objeto [**View**](view-object.md) chamando a função [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .</span><span class="sxs-lookup"><span data-stu-id="e889b-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="e889b-118">Feche o objeto [**View**](view-object.md) chamando a função [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .</span><span class="sxs-lookup"><span data-stu-id="e889b-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="e889b-119">Para obter mais informações, consulte [exemplos de consultas de banco de dados usando SQL e script](examples-of-database-queries-using-sql-and-script.md).</span><span class="sxs-lookup"><span data-stu-id="e889b-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



