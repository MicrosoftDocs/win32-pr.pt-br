---
description: 'Saiba mais sobre: função JetOpenTempTable'
title: Função JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763857"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="d6697-103">Função JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="d6697-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="d6697-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d6697-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="d6697-105">Função JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="d6697-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="d6697-106">A função **JetOpenTempTable** cria uma tabela temporária com um único índice.</span><span class="sxs-lookup"><span data-stu-id="d6697-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="d6697-107">Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6697-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="d6697-108">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="d6697-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="d6697-109">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="d6697-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="d6697-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6697-110">Parameters</span></span>

<span data-ttu-id="d6697-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d6697-111">*sesid*</span></span>

<span data-ttu-id="d6697-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d6697-112">The session to use.</span></span>

<span data-ttu-id="d6697-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="d6697-113">*prgcolumndef*</span></span>

<span data-ttu-id="d6697-114">Definições de coluna para as colunas criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="d6697-115">Existem limitações **importantes** para as opções de definição de coluna usadas com uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="d6697-116">Consulte a seção Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d6697-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="d6697-117">Além das opções de definição de coluna usual, zero ou mais das opções a seguir também podem ser especificadas, que são relevantes apenas no contexto de uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6697-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d6697-118">Value</span></span></p></th>
<th><p><span data-ttu-id="d6697-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d6697-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6697-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="d6697-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="d6697-121">A ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente.</span><span class="sxs-lookup"><span data-stu-id="d6697-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="d6697-122">Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="d6697-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="d6697-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="d6697-124">A coluna será uma coluna de chave para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="d6697-125">A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="d6697-126">A primeira definição de coluna na matriz que tem esse conjunto de opções será a coluna de chave mais significativa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d6697-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="d6697-127">Se mais colunas de chave forem solicitadas do que o mecanismo de banco de dados pode ter suporte, essa opção será ignorada para as colunas de chave sem suporte.</span><span class="sxs-lookup"><span data-stu-id="d6697-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6697-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="d6697-128">*ccolumn*</span></span>

<span data-ttu-id="d6697-129">Consulte *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="d6697-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="d6697-130">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d6697-130">*grbit*</span></span>

<span data-ttu-id="d6697-131">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6697-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6697-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d6697-132">Value</span></span></p></th>
<th><p><span data-ttu-id="d6697-133">Significado</span><span class="sxs-lookup"><span data-stu-id="d6697-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6697-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="d6697-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="d6697-135">Qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente irá falhar imediatamente com JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="d6697-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="d6697-136">Se essa opção não for solicitada, uma duplicata será detectada imediatamente e falhará ou será removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária, com base na funcionalidade solicitada.</span><span class="sxs-lookup"><span data-stu-id="d6697-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="d6697-137">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="d6697-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="d6697-138">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d6697-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="d6697-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="d6697-140">Força o Gerenciador de tabelas temporária a abandonar a pesquisa para que a melhor estratégia use o gerenciamento da tabela temporária, o que resultará em desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d6697-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="d6697-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="d6697-142">A tabela temporária só será criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários.</span><span class="sxs-lookup"><span data-stu-id="d6697-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="d6697-143">Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="d6697-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="d6697-144">Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="d6697-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="d6697-145">Consulte JET_bitTTUnique para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d6697-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="d6697-146">Essa opção só está disponível no Windows Server 2003 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6697-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="d6697-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="d6697-148">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para pesquisar registros por chave de índice.</span><span class="sxs-lookup"><span data-stu-id="d6697-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="d6697-149">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="d6697-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="d6697-150">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d6697-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="d6697-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="d6697-152">As solicitações que os registros com chaves de índice duplicadas são removidas do conjunto final de registros na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="d6697-153">Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="d6697-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="d6697-154">A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção de JET_bitTTForwardOnly também é especificada.</span><span class="sxs-lookup"><span data-stu-id="d6697-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="d6697-155">Não é possível saber qual duplicata terá sucesso e quais duplicatas serão descartadas, em geral.</span><span class="sxs-lookup"><span data-stu-id="d6697-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="d6697-156">No entanto, quando a opção JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserida na tabela temporária sempre terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="d6697-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="d6697-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="d6697-158">Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="d6697-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="d6697-159">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="d6697-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="d6697-160">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d6697-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="d6697-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="d6697-162">Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="d6697-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="d6697-163">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="d6697-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="d6697-164">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d6697-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="d6697-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="d6697-166">Solicita que os valores da coluna de chave nula sejam mais próximos do final do índice que os valores de coluna de chave não nulos.</span><span class="sxs-lookup"><span data-stu-id="d6697-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="d6697-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="d6697-168">Solicitações para permitir somente valores longos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="d6697-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="d6697-169"><strong>Windows 7</strong>: o <strong>JET_bitTTIntrinsicLVsOnly</strong> é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6697-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6697-170">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="d6697-170">*ptableid*</span></span>

<span data-ttu-id="d6697-171">O buffer de saída que recebe o novo cursor aberto na tabela temporária recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d6697-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="d6697-172">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="d6697-172">*prgcolumnid*</span></span>

<span data-ttu-id="d6697-173">O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="d6697-174">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="d6697-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="d6697-175">Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="d6697-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="d6697-176">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d6697-176">Return Value</span></span>

<span data-ttu-id="d6697-177">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6697-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d6697-178">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6697-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6697-179">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d6697-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="d6697-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6697-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6697-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d6697-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d6697-182">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d6697-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="d6697-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="d6697-184"><strong>JetOpenTempTable</strong> falhou porque JET_bitTTForwardOnly foi especificado e a tabela temporária como especificada não pôde ser criada usando a otimização somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="d6697-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="d6697-185">Esse erro só será retornado pelo Windows Server 2003 e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6697-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d6697-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d6697-187">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d6697-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="d6697-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="d6697-189">Não foi possível criar o índice porque uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="d6697-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="d6697-190"><strong>JetOpenTempTable</strong> retornará este erro quando:</span><span class="sxs-lookup"><span data-stu-id="d6697-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="d6697-191">A localidade neutra do idioma é especificada.</span><span class="sxs-lookup"><span data-stu-id="d6697-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="d6697-192">Um conjunto inválido de sinalizadores de normalização foi especificado.</span><span class="sxs-lookup"><span data-stu-id="d6697-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="d6697-193">Esse erro só será retornado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d6697-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d6697-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d6697-195">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="d6697-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="d6697-196">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6697-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="d6697-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="d6697-198">O campo CP do <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="d6697-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="d6697-199">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="d6697-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="d6697-200">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="d6697-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="d6697-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="d6697-202">O campo <em>coltyp</em> da <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="d6697-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="d6697-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="d6697-204">Não foi possível criar o índice porque foi feita uma tentativa de usar uma identificação de localidade inválida.</span><span class="sxs-lookup"><span data-stu-id="d6697-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="d6697-205">A ID de localidade pode ser completamente inválida ou o pacote de idiomas associado pode não estar instalado.</span><span class="sxs-lookup"><span data-stu-id="d6697-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="d6697-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="d6697-207">Não foi possível criar o índice porque foi feita uma tentativa de usar um conjunto inválido de sinalizadores de normalização.</span><span class="sxs-lookup"><span data-stu-id="d6697-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="d6697-208">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6697-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="d6697-209">No Windows 2000, sinalizadores de normalização inválidos resultarão em JET_errIndexInvalidDef em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d6697-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="d6697-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="d6697-211">O identificador de sessão é inválido ou se refere a uma sessão fechada.</span><span class="sxs-lookup"><span data-stu-id="d6697-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="d6697-212"><strong>Observação</strong>  Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="d6697-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="d6697-213">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="d6697-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d6697-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d6697-215">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="d6697-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="d6697-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="d6697-217">A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor.</span><span class="sxs-lookup"><span data-stu-id="d6697-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="d6697-218">Os recursos de cursor são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="d6697-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="d6697-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="d6697-220">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="d6697-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="d6697-221"><strong>JetOpenTempTable</strong> pode retornar JET_errOutOfMemory se o espaço de endereço do processo do host se tornar muito fragmentado.</span><span class="sxs-lookup"><span data-stu-id="d6697-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="d6697-222">O Gerenciador de tabela temporária sempre alocará um bloco de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="d6697-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d6697-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d6697-224">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="d6697-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d6697-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d6697-226">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d6697-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d6697-227">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6697-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d6697-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d6697-229">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="d6697-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="d6697-231">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="d6697-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="d6697-232">Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="d6697-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="d6697-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="d6697-234">A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache os índices da tabela.</span><span class="sxs-lookup"><span data-stu-id="d6697-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="d6697-235">O número de índices cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="d6697-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="d6697-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="d6697-237">A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache o esquema da tabela.</span><span class="sxs-lookup"><span data-stu-id="d6697-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="d6697-238">O número de tabelas cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="d6697-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="d6697-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="d6697-240">A operação falhou porque o mecanismo não pode alocar os recursos necessários para criar uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="d6697-241">Os recursos de tabela temporária são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="d6697-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6697-242">Em caso de sucesso, será retornado um cursor aberto na tabela temporária recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d6697-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="d6697-243">O estado do banco de dados temporário será preparado para conter a nova tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="d6697-244">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="d6697-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="d6697-245">Em caso de falha, a tabela temporária não será criada e um cursor não será retornado.</span><span class="sxs-lookup"><span data-stu-id="d6697-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="d6697-246">O estado do banco de dados temporário pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="d6697-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="d6697-247">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="d6697-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d6697-248">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6697-248">Remarks</span></span>

<span data-ttu-id="d6697-249">As tabelas temporárias não dão suporte ao complemento completo de opções de definição de coluna que normalmente são compatíveis com o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d6697-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="d6697-250">Na verdade, somente JET_bitColumnFixed e JET_bitColumnTagged têm suporte.</span><span class="sxs-lookup"><span data-stu-id="d6697-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="d6697-251">Isso significa que não é possível criar um incremento automático, uma versão ou uma coluna de valores múltiplos em uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="d6697-252">Finalmente, não há suporte para colunas de atualização de caução porque elas não são úteis em uma tabela temporária, pois elas só podem ser usadas por uma sessão por vez.</span><span class="sxs-lookup"><span data-stu-id="d6697-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="d6697-253">Se qualquer uma dessas opções for solicitada, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="d6697-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="d6697-254">As tabelas temporárias não dão suporte a valores padrão.</span><span class="sxs-lookup"><span data-stu-id="d6697-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="d6697-255">Se for fornecida uma definição de coluna que contenha uma especificação de valor padrão, essa especificação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="d6697-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="d6697-256">As tabelas temporárias são retornadas ao chamador como resultado de muitas funções diferentes do ESE.</span><span class="sxs-lookup"><span data-stu-id="d6697-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="d6697-257">Por exemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) com a opção JET_IdxInfo definida no parâmetro *InfoLevel* retornará uma tabela temporária contendo uma lista de todas as colunas de chave em um determinado índice.</span><span class="sxs-lookup"><span data-stu-id="d6697-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="d6697-258">As tabelas temporárias seguem as mesmas regras de ciclo de vida que as tabelas temporárias comuns, conforme descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="d6697-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="d6697-259">As tabelas temporárias também são usadas internamente pelo mecanismo de banco de dados para muitas tarefas.</span><span class="sxs-lookup"><span data-stu-id="d6697-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="d6697-260">A mais importante dessas tarefas é a criação de um índice em uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="d6697-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="d6697-261">Uma tabela temporária será usada para classificar as chaves de índice usadas para construir esse índice.</span><span class="sxs-lookup"><span data-stu-id="d6697-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="d6697-262">Todas as tabelas temporárias são armazenadas no banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="d6697-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="d6697-263">O banco de dados temporário é um arquivo de banco de dados especial que é mantido durante o tempo de vida de uma instância do ESE e é excluído quando essa instância é desligada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="d6697-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="d6697-264">O local do banco de dados temporário pode ser configurado usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6697-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="d6697-265">O posicionamento do banco de dados temporário em disco em relação aos arquivos de log de transações e arquivos de banco de dados poderá ser importante se seu aplicativo fizer uso intensivo de tabelas temporárias ou criar índices com frequência.</span><span class="sxs-lookup"><span data-stu-id="d6697-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="d6697-266">O ciclo de vida de uma tabela temporária é vinculado aos cursores que fazem referência a ela.</span><span class="sxs-lookup"><span data-stu-id="d6697-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="d6697-267">Se todos os cursores que fazem referência a uma tabela temporária forem fechados, implicitamente ou explicitamente, a tabela temporária será excluída.</span><span class="sxs-lookup"><span data-stu-id="d6697-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="d6697-268">Se uma tabela temporária for criada dentro de uma transação e essa transação for revertida posteriormente, a tabela temporária será excluída porque todos os cursores que fazem referência a ela neste momento serão fechados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="d6697-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="d6697-269">Novos cursores podem fazer referência a uma tabela temporária somente por meio do uso de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6697-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="d6697-270">Nesse caso, os novos cursores serão posicionados na primeira entrada de índice da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="d6697-271">[JetDupCursor](./jetdupcursor-function.md) só funcionará durante determinadas fases de uso para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="d6697-272">Consulte os comentários sobre os recursos de cursor de tabela temporária para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d6697-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="d6697-273">Não é possível fazer referência a uma tabela temporária de mais de uma sessão por vez.</span><span class="sxs-lookup"><span data-stu-id="d6697-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="d6697-274">Há um problema importante no [JetDupCursor](./jetdupcursor-function.md) que afeta as tabelas temporárias.</span><span class="sxs-lookup"><span data-stu-id="d6697-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="d6697-275">Se for feita uma tentativa de duplicar uma tabela temporária que está no modo somente de encaminhamento, o cursor resultante não será criado corretamente e não terá funcionamento adequado.</span><span class="sxs-lookup"><span data-stu-id="d6697-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="d6697-276">Ainda é seguro duplicar um cursor em uma tabela temporária materializada.</span><span class="sxs-lookup"><span data-stu-id="d6697-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="d6697-277">O Gerenciador de tabelas temporárias pode optar por implementar uma tabela temporária de três maneiras.</span><span class="sxs-lookup"><span data-stu-id="d6697-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="d6697-278">O primeiro método é manter uma tabela na memória.</span><span class="sxs-lookup"><span data-stu-id="d6697-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="d6697-279">Essa estratégia é a mais rápida, mas só pode ser usada para tabelas temporárias pequenas e simples.</span><span class="sxs-lookup"><span data-stu-id="d6697-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="d6697-280">O segundo método é criar uma classificação baseada em disco que possa ser controlada usando um iterador somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="d6697-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="d6697-281">Essa estratégia só pode ser usada em determinadas circunstâncias e é a maneira mais rápida de classificar e remover duplicatas de um conjunto de dados muito grande.</span><span class="sxs-lookup"><span data-stu-id="d6697-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="d6697-282">O terceiro método é criar uma árvore B + no banco de dados temporário para manter a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="d6697-283">Essa estratégia é a mais lenta, mas a mais versátil e é conhecida como uma tabela temporária materializada.</span><span class="sxs-lookup"><span data-stu-id="d6697-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="d6697-284">Essas estratégias podem ser usadas em combinação para atingir por fim a funcionalidade solicitada da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d6697-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="d6697-285">Quando a tabela temporária não está materializada, ela é usada em principalmente duas fases principais.</span><span class="sxs-lookup"><span data-stu-id="d6697-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="d6697-286">A primeira fase é a fase de inserção em que a tabela é populada com seu conjunto de dados inicial.</span><span class="sxs-lookup"><span data-stu-id="d6697-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="d6697-287">Durante essa fase, apenas a inserção de dados é permitida.</span><span class="sxs-lookup"><span data-stu-id="d6697-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="d6697-288">Essa fase termina quando é feita uma tentativa de mover o cursor usando [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6697-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="d6697-289">A segunda fase é a fase de extração de dados.</span><span class="sxs-lookup"><span data-stu-id="d6697-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="d6697-290">Durante essa fase, os dados armazenados na tabela temporária podem ser extraídos de acordo com os recursos solicitados quando a tabela temporária foi criada.</span><span class="sxs-lookup"><span data-stu-id="d6697-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="d6697-291">**Recursos de cursor de tabela temporária**</span><span class="sxs-lookup"><span data-stu-id="d6697-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="d6697-292">Quando a tabela temporária é materializada, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções solicitadas:</span><span class="sxs-lookup"><span data-stu-id="d6697-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="d6697-293">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d6697-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="d6697-294">JetDelete</span><span class="sxs-lookup"><span data-stu-id="d6697-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="d6697-295">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="d6697-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="d6697-296">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="d6697-297">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d6697-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="d6697-298">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="d6697-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="d6697-299">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="d6697-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="d6697-300">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="d6697-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="d6697-301">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="d6697-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="d6697-302">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="d6697-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="d6697-303">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="d6697-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="d6697-304">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="d6697-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="d6697-305">JetMove</span><span class="sxs-lookup"><span data-stu-id="d6697-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="d6697-306">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="d6697-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="d6697-307">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d6697-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="d6697-308">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="d6697-309">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="d6697-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="d6697-310">JetSeek</span><span class="sxs-lookup"><span data-stu-id="d6697-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="d6697-311">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="d6697-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="d6697-312">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="d6697-313">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d6697-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="d6697-314">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="d6697-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="d6697-315">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="d6697-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="d6697-316">Quando a tabela temporária não está materializada e está na fase de inserção, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções solicitadas:</span><span class="sxs-lookup"><span data-stu-id="d6697-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="d6697-317">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d6697-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="d6697-318">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d6697-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="d6697-319">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="d6697-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="d6697-320">JetMove</span><span class="sxs-lookup"><span data-stu-id="d6697-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="d6697-321">**Observação**  Faz a transição para a fase de extração.</span><span class="sxs-lookup"><span data-stu-id="d6697-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="d6697-322">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="d6697-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="d6697-323">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="d6697-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="d6697-324">JetSeek</span><span class="sxs-lookup"><span data-stu-id="d6697-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="d6697-325">**Observação**  Faz a transição para a fase de extração.</span><span class="sxs-lookup"><span data-stu-id="d6697-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="d6697-326">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="d6697-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="d6697-327">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="d6697-328">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="d6697-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="d6697-329">Quando a tabela temporária não está materializada e está na fase de extração, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções solicitadas:</span><span class="sxs-lookup"><span data-stu-id="d6697-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="d6697-330">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d6697-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="d6697-331">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="d6697-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="d6697-332">**Observação**  Se for feita uma tentativa de duplicar uma tabela temporária que está no modo somente de encaminhamento, o cursor resultante não será criado corretamente e não terá funcionamento adequado.</span><span class="sxs-lookup"><span data-stu-id="d6697-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="d6697-333">Ainda é seguro duplicar um cursor em uma tabela temporária materializada.</span><span class="sxs-lookup"><span data-stu-id="d6697-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="d6697-334">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="d6697-335">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="d6697-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="d6697-336">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="d6697-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="d6697-337">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="d6697-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="d6697-338">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="d6697-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="d6697-339">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="d6697-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="d6697-340">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="d6697-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="d6697-341">JetMove</span><span class="sxs-lookup"><span data-stu-id="d6697-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="d6697-342">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d6697-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="d6697-343">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="d6697-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="d6697-344">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="d6697-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="d6697-345">JetSeek</span><span class="sxs-lookup"><span data-stu-id="d6697-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="d6697-346">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d6697-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="d6697-347">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="d6697-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="d6697-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6697-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6697-349"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d6697-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d6697-350">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d6697-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-351"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d6697-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d6697-352">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d6697-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-353"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d6697-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d6697-354">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d6697-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6697-355"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d6697-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d6697-356">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d6697-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6697-357"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d6697-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d6697-358">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d6697-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d6697-359">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d6697-359">See Also</span></span>

[<span data-ttu-id="d6697-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="d6697-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="d6697-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d6697-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d6697-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d6697-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d6697-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d6697-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d6697-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d6697-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d6697-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d6697-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d6697-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="d6697-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="d6697-367">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d6697-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="d6697-368">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="d6697-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="d6697-369">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="d6697-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="d6697-370">JetMove</span><span class="sxs-lookup"><span data-stu-id="d6697-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="d6697-371">JetRollback</span><span class="sxs-lookup"><span data-stu-id="d6697-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="d6697-372">JetSeek</span><span class="sxs-lookup"><span data-stu-id="d6697-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="d6697-373">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="d6697-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="d6697-374">Parâmetros de banco de dados temporários</span><span class="sxs-lookup"><span data-stu-id="d6697-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
