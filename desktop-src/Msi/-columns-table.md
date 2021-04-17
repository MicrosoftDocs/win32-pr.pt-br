---
description: A \_ tabela Columns é uma tabela de sistema somente leitura que contém o catálogo de colunas. Ele lista as colunas de todas as tabelas. Você pode consultar esta tabela para descobrir se existe uma determinada coluna.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Tabela de _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754655"
---
# <a name="_columns-table"></a><span data-ttu-id="07968-105">\_Tabela de colunas</span><span class="sxs-lookup"><span data-stu-id="07968-105">\_Columns Table</span></span>

<span data-ttu-id="07968-106">A \_ tabela Columns é uma tabela de sistema somente leitura que contém o catálogo de colunas.</span><span class="sxs-lookup"><span data-stu-id="07968-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="07968-107">Ele lista as colunas de todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="07968-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="07968-108">Você pode consultar esta tabela para descobrir se existe uma determinada coluna.</span><span class="sxs-lookup"><span data-stu-id="07968-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="07968-109">A \_ tabela Columns tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="07968-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="07968-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="07968-110">Column</span></span> | <span data-ttu-id="07968-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="07968-111">Type</span></span>                   | <span data-ttu-id="07968-112">Chave</span><span class="sxs-lookup"><span data-stu-id="07968-112">Key</span></span> | <span data-ttu-id="07968-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="07968-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="07968-114">Tabela</span><span class="sxs-lookup"><span data-stu-id="07968-114">Table</span></span>  | [<span data-ttu-id="07968-115">Text</span><span class="sxs-lookup"><span data-stu-id="07968-115">Text</span></span>](text.md)       | <span data-ttu-id="07968-116">S</span><span class="sxs-lookup"><span data-stu-id="07968-116">Y</span></span>   | <span data-ttu-id="07968-117">N</span><span class="sxs-lookup"><span data-stu-id="07968-117">N</span></span>        |
| <span data-ttu-id="07968-118">Número</span><span class="sxs-lookup"><span data-stu-id="07968-118">Number</span></span> | [<span data-ttu-id="07968-119">Inteiro</span><span class="sxs-lookup"><span data-stu-id="07968-119">Integer</span></span>](integer.md) | <span data-ttu-id="07968-120">S</span><span class="sxs-lookup"><span data-stu-id="07968-120">Y</span></span>   | <span data-ttu-id="07968-121">N</span><span class="sxs-lookup"><span data-stu-id="07968-121">N</span></span>        |
| <span data-ttu-id="07968-122">Nome</span><span class="sxs-lookup"><span data-stu-id="07968-122">Name</span></span>   | [<span data-ttu-id="07968-123">Text</span><span class="sxs-lookup"><span data-stu-id="07968-123">Text</span></span>](text.md)       | <span data-ttu-id="07968-124">N</span><span class="sxs-lookup"><span data-stu-id="07968-124">N</span></span>   | <span data-ttu-id="07968-125">N</span><span class="sxs-lookup"><span data-stu-id="07968-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="07968-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="07968-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="07968-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="07968-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="07968-128">O nome da tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="07968-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="07968-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Automática</span><span class="sxs-lookup"><span data-stu-id="07968-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="07968-130">A ordem da coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="07968-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="07968-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="07968-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="07968-132">O nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="07968-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07968-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="07968-133">Remarks</span></span>

<span data-ttu-id="07968-134">Como a \_ tabela Columns é uma tabela do sistema que não pode ser modificada por meio de consultas SQL, você não pode obter as chaves primárias com a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou a [**Propriedade primarykeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="07968-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="07968-135">Somente colunas persistentes são armazenadas na \_ tabela colunas.</span><span class="sxs-lookup"><span data-stu-id="07968-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="07968-136">Para determinar se uma coluna temporária existe, é necessário criar uma exibição usando uma instrução SELECT \* em relação à tabela e, em seguida, fazer um loop por todos os campos em um registro retornado pela função [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) com a \_ opção nomes de MSICOLINFO.</span><span class="sxs-lookup"><span data-stu-id="07968-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



