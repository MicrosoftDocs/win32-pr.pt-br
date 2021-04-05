---
description: A \_ tabela tabelas é uma tabela de sistema somente leitura que lista todas as tabelas no banco de dados. Consulte esta tabela para descobrir se existe uma tabela.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Tabela de _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828102"
---
# <a name="_tables-table"></a><span data-ttu-id="d1821-104">\_Tabela de tabelas</span><span class="sxs-lookup"><span data-stu-id="d1821-104">\_Tables Table</span></span>

<span data-ttu-id="d1821-105">A \_ tabela tabelas é uma tabela de sistema somente leitura que lista todas as tabelas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d1821-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="d1821-106">Consulte esta tabela para descobrir se existe uma tabela.</span><span class="sxs-lookup"><span data-stu-id="d1821-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="d1821-107">A \_ tabela tabelas tem a seguinte coluna.</span><span class="sxs-lookup"><span data-stu-id="d1821-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="d1821-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="d1821-108">Column</span></span> | <span data-ttu-id="d1821-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1821-109">Type</span></span>             | <span data-ttu-id="d1821-110">Chave</span><span class="sxs-lookup"><span data-stu-id="d1821-110">Key</span></span> | <span data-ttu-id="d1821-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="d1821-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="d1821-112">Nome</span><span class="sxs-lookup"><span data-stu-id="d1821-112">Name</span></span>   | [<span data-ttu-id="d1821-113">Text</span><span class="sxs-lookup"><span data-stu-id="d1821-113">Text</span></span>](text.md) | <span data-ttu-id="d1821-114">S</span><span class="sxs-lookup"><span data-stu-id="d1821-114">Y</span></span>   | <span data-ttu-id="d1821-115">N</span><span class="sxs-lookup"><span data-stu-id="d1821-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="d1821-116">Coluna</span><span class="sxs-lookup"><span data-stu-id="d1821-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="d1821-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="d1821-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d1821-118">Nome de uma das tabelas.</span><span class="sxs-lookup"><span data-stu-id="d1821-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1821-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1821-119">Remarks</span></span>

<span data-ttu-id="d1821-120">Como a \_ tabela tabelas é uma tabela do sistema que não pode ser modificada por meio de consultas SQL, você não pode obter as chaves primárias com a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou a [**Propriedade primarykeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="d1821-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



