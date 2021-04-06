---
description: A \_ tabela de armazenamentos lista armazenamentos de dados OLE inseridos. Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Tabela de _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828104"
---
# <a name="_storages-table"></a><span data-ttu-id="93669-104">\_Tabela de armazenamentos</span><span class="sxs-lookup"><span data-stu-id="93669-104">\_Storages Table</span></span>

<span data-ttu-id="93669-105">A \_ tabela de armazenamentos lista armazenamentos de dados OLE inseridos.</span><span class="sxs-lookup"><span data-stu-id="93669-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="93669-106">Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="93669-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="93669-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="93669-107">Column</span></span> | <span data-ttu-id="93669-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="93669-108">Type</span></span>                 | <span data-ttu-id="93669-109">Chave</span><span class="sxs-lookup"><span data-stu-id="93669-109">Key</span></span> | <span data-ttu-id="93669-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="93669-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="93669-111">Nome</span><span class="sxs-lookup"><span data-stu-id="93669-111">Name</span></span>   | [<span data-ttu-id="93669-112">Text</span><span class="sxs-lookup"><span data-stu-id="93669-112">Text</span></span>](text.md)     | <span data-ttu-id="93669-113">S</span><span class="sxs-lookup"><span data-stu-id="93669-113">Y</span></span>   | <span data-ttu-id="93669-114">N</span><span class="sxs-lookup"><span data-stu-id="93669-114">N</span></span>        |
| <span data-ttu-id="93669-115">Dados</span><span class="sxs-lookup"><span data-stu-id="93669-115">Data</span></span>   | [<span data-ttu-id="93669-116">Binary</span><span class="sxs-lookup"><span data-stu-id="93669-116">Binary</span></span>](binary.md) | <span data-ttu-id="93669-117">N</span><span class="sxs-lookup"><span data-stu-id="93669-117">N</span></span>   | <span data-ttu-id="93669-118">S</span><span class="sxs-lookup"><span data-stu-id="93669-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="93669-119">Colunas</span><span class="sxs-lookup"><span data-stu-id="93669-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="93669-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="93669-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="93669-121">Uma chave exclusiva que identifica o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="93669-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="93669-122">O comprimento máximo do nome é 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="93669-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="93669-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado</span><span class="sxs-lookup"><span data-stu-id="93669-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="93669-124">Os dados binários não formatados.</span><span class="sxs-lookup"><span data-stu-id="93669-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93669-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="93669-125">Remarks</span></span>

<span data-ttu-id="93669-126">Para adicionar um armazenamento OLE a um banco de dados, crie um novo registro na \_ tabela armazenamentos e insira o nome do armazenamento na coluna nome.</span><span class="sxs-lookup"><span data-stu-id="93669-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="93669-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar dados para a coluna de dados deste registro.</span><span class="sxs-lookup"><span data-stu-id="93669-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="93669-128">Por fim, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na \_ tabela armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="93669-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="93669-129">Os dados não podem ser lidos da \_ tabela de armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="93669-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="93669-130">No entanto, a \_ tabela de armazenamentos pode ser consultada para verificar a existência de um armazenamento específico.</span><span class="sxs-lookup"><span data-stu-id="93669-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="93669-131">Isso significa que não é possível mover um armazenamento OLE de um banco de dados para outro.</span><span class="sxs-lookup"><span data-stu-id="93669-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="93669-132">Em vez disso, você deve importar o arquivo de armazenamento original para o novo banco de dados. Para excluir um armazenamento OLE, busque o registro que contém os dados binários, defina a coluna de dados na \_ tabela armazenamentos como NULL e, em seguida, atualize o registro.</span><span class="sxs-lookup"><span data-stu-id="93669-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="93669-133">Um método alternativo é simplesmente excluir o registro usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou uma consulta SQL simples.</span><span class="sxs-lookup"><span data-stu-id="93669-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="93669-134">Para renomear um armazenamento OLE, atualize a coluna nome do registro.</span><span class="sxs-lookup"><span data-stu-id="93669-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="93669-135">Se uma espera for colocada nessa tabela usando SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="93669-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="93669-136">HOLD) ou uma coluna é adicionada com HOLD, a tabela deve ser liberada usando FREE.</span><span class="sxs-lookup"><span data-stu-id="93669-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="93669-137">Os armazenamentos não são gravados até que a tabela seja liberada ou confirmada.</span><span class="sxs-lookup"><span data-stu-id="93669-137">Storages are not written until the table has been released or committed.</span></span>

 

 



