---
description: 'Saiba mais sobre: função JetDefragment2'
title: Função JetDefragment2
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838800"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="fa6f3-103">Função JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="fa6f3-103">JetDefragment2 Function</span></span>


<span data-ttu-id="fa6f3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fa6f3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="fa6f3-105">Função JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="fa6f3-105">JetDefragment2 Function</span></span>

<span data-ttu-id="fa6f3-106">A função **JetDefragment2** inicia e interrompe as tarefas de desfragmentação do banco de dados, o que melhora a organização da data em um banco de dado, com um parâmetro de retorno de chamada disponível para relatar o progresso da desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="fa6f3-107">Isso é feito para limitar o crescimento do banco de dados usando a alocação de disco existente com mais eficiência no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="fa6f3-108">Ele também pode reduzir o conjunto de trabalho, garantindo que os dados sejam mais bem compactados.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="fa6f3-109">Por fim, ele pode melhorar o desempenho do aplicativo acelerando as operações comuns por meio de uma melhor organização de dados.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="fa6f3-110">**Windows XP:** o **JetDefragment2** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="fa6f3-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="fa6f3-111">**JetDefragment2** também contém um parâmetro de função de retorno de chamada que é usado para relatar o progresso do processo de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="fa6f3-112">A desfragmentação de banco de dados é uma operação online e não interrompe a atividade de banco de dados regular, como operações de consulta ou atualizações de data.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="fa6f3-113">O **JetDefragment2** também não faz uma cópia de todos os dados existentes.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="fa6f3-114">Em vez disso, ele desfragmenta um banco de dados em vigor.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="fa6f3-115">Por fim, o **JetDefragment2** recupera o espaço interno do banco de dados para reutilização, mas não libera espaço em excesso para o sistema de arquivos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="fa6f3-116">O formato resultante dos dados pode ser muito mais eficiente, mas geralmente não é o ideal.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="fa6f3-117">A desfragmentação é limitada à liberação de páginas de banco de dados para reutilização que contêm dados que já foram excluídos logicamente.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="fa6f3-118">A desfragmentação também torna as páginas de banco de dados disponíveis para reutilização em alguns casos, combinando dados de duas páginas quando elas podem caber em uma única página.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="fa6f3-119">Essa operação é diferente de [JetCompact](./jetcompact-function.md) , que faz uma cópia de um banco de dados somente leitura em um formato altamente ideal.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="fa6f3-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa6f3-120">Parameters</span></span>

<span data-ttu-id="fa6f3-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-121">*sesid*</span></span>

<span data-ttu-id="fa6f3-122">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-122">The session to use for this call.</span></span>

<span data-ttu-id="fa6f3-123">*DBID*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-123">*dbid*</span></span>

<span data-ttu-id="fa6f3-124">O banco de dados a ser desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-124">The database to defragment.</span></span>

<span data-ttu-id="fa6f3-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-125">*szTableName*</span></span>

<span data-ttu-id="fa6f3-126">Às vezes, *szTableName* é necessário e, às vezes, é proibido:</span><span class="sxs-lookup"><span data-stu-id="fa6f3-126">Sometimes *szTableName* is required, and sometimes it is forbidden:</span></span>

| <span data-ttu-id="fa6f3-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-127">*grbit*</span></span> | <span data-ttu-id="fa6f3-128">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-128">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="fa6f3-129">Deve ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-129">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="fa6f3-130">Especifica o nome da tabela/árvore b a ser desfragmentada.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-130">Specifies the name of the table/BTree to defragment.</span></span> |
| <span data-ttu-id="fa6f3-131">*outros*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-131">*other*</span></span> | <span data-ttu-id="fa6f3-132">Deve ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-132">Must be `NULL`.</span></span> |
 
<span data-ttu-id="fa6f3-133">A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-133">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="fa6f3-134">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-134">*pcPasses*</span></span>

<span data-ttu-id="fa6f3-135">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o número máximo de passagens de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-135">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="fa6f3-136">Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido como o número de passagens executadas.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-136">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="fa6f3-137">Quando esse parâmetro é definido como NULL, o número de passagens de desfragmentação online é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-137">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="fa6f3-138">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-138">*pcSeconds*</span></span>

<span data-ttu-id="fa6f3-139">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o tempo máximo para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-139">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="fa6f3-140">Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido com o período de tempo usado para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-140">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="fa6f3-141">Quando esse parâmetro é definido como nulo ou se *pcSeconds* aponta para um valor negativo, o tempo máximo para desfragmentação é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-141">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="fa6f3-142">*retorno de chamada*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-142">*callback*</span></span>

<span data-ttu-id="fa6f3-143">Função de retorno de chamada que a desfragmentação chama regularmente para relatar o progresso.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-143">Callback function that defragmentation calls regularly to report progress.</span></span>

| <span data-ttu-id="fa6f3-144">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-144">*grbit*</span></span> | <span data-ttu-id="fa6f3-145">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-145">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="fa6f3-146">Deve ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-146">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="fa6f3-147">Deve ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-147">Must be `NULL`.</span></span> |
| <span data-ttu-id="fa6f3-148">*outros*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-148">*other*</span></span> | <span data-ttu-id="fa6f3-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-149">Optional.</span></span>


<span data-ttu-id="fa6f3-150">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fa6f3-150">*grbit*</span></span>

<span data-ttu-id="fa6f3-151">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-151">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa6f3-152">Valor</span><span class="sxs-lookup"><span data-stu-id="fa6f3-152">Value</span></span></p></th>
<th><p><span data-ttu-id="fa6f3-153">Significado</span><span class="sxs-lookup"><span data-stu-id="fa6f3-153">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-154">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="fa6f3-154">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-155">Essa opção é usada para desfragmentar a parte de espaço disponível da alocação de espaço do banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-155">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="fa6f3-156">O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-156">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="fa6f3-157">O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-157">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="fa6f3-158">O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-158">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-159">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="fa6f3-159">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-160">Essa opção é usada para iniciar uma nova tarefa de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-160">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-161">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="fa6f3-161">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-162">Essa opção é usada para interromper uma tarefa de desfragmentação iniciada existente.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-162">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-163">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="fa6f3-163">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-164">Essa opção é usada para desfragmentar uma árvore B, especificada por szTableName.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-164">This option is used to defrag a B-Tree, specified by szTableName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-165">JET_bitDefragmentBTreeBatch</span><span class="sxs-lookup"><span data-stu-id="fa6f3-165">JET_bitDefragmentBTreeBatch</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-166">Essa opção é usada para chamar OLD2 em todo o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-166">This option is used to call OLD2 on the entire database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fa6f3-167">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fa6f3-167">Return Value</span></span>

<span data-ttu-id="fa6f3-168">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-168">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fa6f3-169">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fa6f3-169">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa6f3-170">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa6f3-170">Return code</span></span></p></th>
<th><p><span data-ttu-id="fa6f3-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa6f3-171">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-172">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fa6f3-172">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-173">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-173">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-174">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fa6f3-174">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-175">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-175">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-176">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="fa6f3-176">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-177">O banco de dados escolhido para desfragmentação é somente leitura e não pode ser atualizado de nenhuma forma, incluindo a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-177">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="fa6f3-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-179">A sessão fornecida está no estado preparado para confirmar e não pode iniciar novas atualizações até que a transação atual seja confirmada ou revertida.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-179">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-180">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fa6f3-180">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-181">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-181">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fa6f3-182">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-182">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-183">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="fa6f3-183">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-184">A ID de banco de dados fornecida não corresponde a um banco de dados conhecido na instância.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-184">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-185">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fa6f3-185">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-186">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-186">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-187">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fa6f3-187">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-188">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-188">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-189">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fa6f3-189">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-190">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-190">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="fa6f3-191">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-191">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-192">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fa6f3-192">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-193">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-193">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-194">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="fa6f3-194">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-195">A sessão fornecida tem somente privilégios somente leitura e não pode iniciar uma tarefa que possa executar uma atualização, incluindo a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-195">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-196">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="fa6f3-196">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-197">Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-197">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-198">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="fa6f3-198">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-199">A opção JET_bitDefragmentBatchStart foi aprovada, mas uma tarefa de desfragmentação já está executando a desfragmentação no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-199">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-200">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="fa6f3-200">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="fa6f3-201">A opção JET_bitDefragmentBatchStop foi aprovada, mas nenhuma tarefa de desfragmentação está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-201">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa6f3-202">Em caso de sucesso, a ação solicitada de iniciar uma tarefa de desfragmentação para determinados dados com determinadas opções é executada ou a ação de parar uma tarefa de desfragmentação existente é executada.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-202">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="fa6f3-203">Em caso de falha, a ação solicitada de iniciar ou parar um trabalho de desfragmentação online não é feita.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-203">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="fa6f3-204">Nenhum outro efeito colateral ocorre.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-204">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fa6f3-205">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa6f3-205">Remarks</span></span>

<span data-ttu-id="fa6f3-206">A desfragmentação online é controlada por uma configuração de parâmetro, bem como por essa API.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-206">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="fa6f3-207">O valor do parâmetro do sistema padrão é JET_OnlineDefragAll, o que significa que a desfragmentação está habilitada para todas as estruturas de dados com suporte.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-207">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="fa6f3-208">No entanto, usando o [JetSetSystemParameter](./jetsetsystemparameter-function.md), é possível desabilitar a desfragmentação online ou habilitá-la seletivamente somente para árvores de espaço de banco de dados, somente para bancos, somente para arquivos de streaming ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-208">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="fa6f3-209">Se a configuração do sistema para desfragmentação online for para uma configuração obsoleta, **JetDefragment2** tratará a configuração como JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-209">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="fa6f3-210">Pode haver, no máximo, uma tarefa em execução para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-210">There can at most be one task running for each database.</span></span> <span data-ttu-id="fa6f3-211">A tarefa é executada como um thread no processo que hospeda o ESE.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-211">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="fa6f3-212">A sessão usada para iniciar a tarefa de desfragmentação online pode ser usada posteriormente para operações de banco de dados enquanto a tarefa de desfragmentação continuar, pois a tarefa de desfragmentação aloca sua própria sessão.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-212">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="fa6f3-213">A sessão fornecida é usada apenas para verificar as permissões associadas à sessão de início da tarefa e não é realmente usada para as operações de desfragmentação propriamente ditas.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-213">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fa6f3-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa6f3-214">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-215"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fa6f3-215"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fa6f3-216">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-216">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-217"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="fa6f3-217"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fa6f3-218">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-218">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-219"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="fa6f3-219"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fa6f3-220">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-220">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-221"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="fa6f3-221"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fa6f3-222">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-222">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa6f3-223"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fa6f3-223"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fa6f3-224">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fa6f3-224">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa6f3-225"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fa6f3-225"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fa6f3-226">Implementado como <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fa6f3-226">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fa6f3-227">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fa6f3-227">See Also</span></span>

[<span data-ttu-id="fa6f3-228">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fa6f3-228">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fa6f3-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fa6f3-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fa6f3-230">JetCompact</span><span class="sxs-lookup"><span data-stu-id="fa6f3-230">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="fa6f3-231">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="fa6f3-231">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="fa6f3-232">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="fa6f3-232">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="fa6f3-233">JetStopService</span><span class="sxs-lookup"><span data-stu-id="fa6f3-233">JetStopService</span></span>](./jetstopservice-function.md)
