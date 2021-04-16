---
description: A \_ tabela de fluxos lista os fluxos de dados OLE inseridos. Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Tabela de _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757539"
---
# <a name="_streams-table"></a><span data-ttu-id="dd271-104">\_Tabela de fluxos</span><span class="sxs-lookup"><span data-stu-id="dd271-104">\_Streams Table</span></span>

<span data-ttu-id="dd271-105">A \_ tabela de fluxos lista os fluxos de dados OLE inseridos.</span><span class="sxs-lookup"><span data-stu-id="dd271-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="dd271-106">Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="dd271-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="dd271-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="dd271-107">Column</span></span> | <span data-ttu-id="dd271-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd271-108">Type</span></span>                 | <span data-ttu-id="dd271-109">Chave</span><span class="sxs-lookup"><span data-stu-id="dd271-109">Key</span></span> | <span data-ttu-id="dd271-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="dd271-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="dd271-111">Nome</span><span class="sxs-lookup"><span data-stu-id="dd271-111">Name</span></span>   | [<span data-ttu-id="dd271-112">Text</span><span class="sxs-lookup"><span data-stu-id="dd271-112">Text</span></span>](text.md)     | <span data-ttu-id="dd271-113">S</span><span class="sxs-lookup"><span data-stu-id="dd271-113">Y</span></span>   | <span data-ttu-id="dd271-114">N</span><span class="sxs-lookup"><span data-stu-id="dd271-114">N</span></span>        |
| <span data-ttu-id="dd271-115">Dados</span><span class="sxs-lookup"><span data-stu-id="dd271-115">Data</span></span>   | [<span data-ttu-id="dd271-116">Binary</span><span class="sxs-lookup"><span data-stu-id="dd271-116">Binary</span></span>](binary.md) | <span data-ttu-id="dd271-117">N</span><span class="sxs-lookup"><span data-stu-id="dd271-117">N</span></span>   | <span data-ttu-id="dd271-118">S</span><span class="sxs-lookup"><span data-stu-id="dd271-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="dd271-119">Colunas</span><span class="sxs-lookup"><span data-stu-id="dd271-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="dd271-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="dd271-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="dd271-121">Uma chave exclusiva que identifica o fluxo.</span><span class="sxs-lookup"><span data-stu-id="dd271-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="dd271-122">O comprimento máximo do nome é de 62 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dd271-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="dd271-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado</span><span class="sxs-lookup"><span data-stu-id="dd271-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="dd271-124">Os dados binários não formatados.</span><span class="sxs-lookup"><span data-stu-id="dd271-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd271-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd271-125">Remarks</span></span>

<span data-ttu-id="dd271-126">Para copiar um fluxo de dados OLE (por exemplo, um objeto de tipo de dados [Binary](binary.md) ) de um arquivo para um banco de dados, crie um registro na \_ tabela de fluxos e insira o nome do fluxo de dado na coluna nome desse registro e copie os dados do arquivo para a coluna de dados usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span><span class="sxs-lookup"><span data-stu-id="dd271-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="dd271-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o novo registro na tabela.</span><span class="sxs-lookup"><span data-stu-id="dd271-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="dd271-128">Para ler um fluxo de dados binários inserido em um banco de dado, use uma consulta SQL para localizar e buscar o registro que contém os dados binários.</span><span class="sxs-lookup"><span data-stu-id="dd271-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="dd271-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) para ler os dados binários em um buffer.</span><span class="sxs-lookup"><span data-stu-id="dd271-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="dd271-130">Para mover um fluxo de dados binários de um banco para outro, primeiro exporte os dados para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd271-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="dd271-131">Use uma consulta SQL para localizar o fluxo de dados no arquivo e use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar os dados do arquivo para a coluna de dados da \_ tabela de fluxos do segundo banco de dado.</span><span class="sxs-lookup"><span data-stu-id="dd271-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="dd271-132">Isso garante que cada banco de dados tenha sua própria cópia dos dados binários.</span><span class="sxs-lookup"><span data-stu-id="dd271-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="dd271-133">Não é possível mover dados binários de um banco de dado para outro simplesmente buscando um registro com os dados do primeiro banco de dado e inserindo-o no segundo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dd271-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="dd271-134">Para excluir um fluxo de dados, busque o registro e defina a coluna de dados como NULL antes de atualizar o registro.</span><span class="sxs-lookup"><span data-stu-id="dd271-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="dd271-135">Outro método é remover o registro da tabela, excluindo-o usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou uma consulta SQL simples.</span><span class="sxs-lookup"><span data-stu-id="dd271-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="dd271-136">Um fluxo não deve ser buscado em um registro se o fluxo for excluído da tabela.</span><span class="sxs-lookup"><span data-stu-id="dd271-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="dd271-137">Para renomear um fluxo de dados OLE, atualize a coluna ' name ' do registro.</span><span class="sxs-lookup"><span data-stu-id="dd271-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="dd271-138">Se uma espera for colocada nessa tabela usando SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="dd271-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="dd271-139">HOLD) ou uma coluna é adicionada com HOLD, a tabela deve ser liberada usando FREE.</span><span class="sxs-lookup"><span data-stu-id="dd271-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="dd271-140">Os fluxos não são gravados até que a tabela seja liberada ou confirmada.</span><span class="sxs-lookup"><span data-stu-id="dd271-140">Streams are not written until the table has been released or committed.</span></span>

 

 



