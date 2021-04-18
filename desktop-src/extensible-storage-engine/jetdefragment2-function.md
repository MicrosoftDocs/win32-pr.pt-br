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
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105816038"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="9a609-103">Função JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="9a609-103">JetDefragment2 Function</span></span>


<span data-ttu-id="9a609-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9a609-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="9a609-105">Função JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="9a609-105">JetDefragment2 Function</span></span>

<span data-ttu-id="9a609-106">A função **JetDefragment2** inicia e interrompe as tarefas de desfragmentação do banco de dados, o que melhora a organização da data em um banco de dado, com um parâmetro de retorno de chamada disponível para relatar o progresso da desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="9a609-107">Isso é feito para limitar o crescimento do banco de dados usando a alocação de disco existente com mais eficiência no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9a609-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="9a609-108">Ele também pode reduzir o conjunto de trabalho, garantindo que os dados sejam mais bem compactados.</span><span class="sxs-lookup"><span data-stu-id="9a609-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="9a609-109">Por fim, ele pode melhorar o desempenho do aplicativo acelerando as operações comuns por meio de uma melhor organização de dados.</span><span class="sxs-lookup"><span data-stu-id="9a609-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="9a609-110">**Windows XP:** o **JetDefragment2** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="9a609-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="9a609-111">**JetDefragment2** também contém um parâmetro de função de retorno de chamada que é usado para relatar o progresso do processo de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="9a609-112">A desfragmentação de banco de dados é uma operação online e não interrompe a atividade de banco de dados regular, como operações de consulta ou atualizações de data.</span><span class="sxs-lookup"><span data-stu-id="9a609-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="9a609-113">O **JetDefragment2** também não faz uma cópia de todos os dados existentes.</span><span class="sxs-lookup"><span data-stu-id="9a609-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="9a609-114">Em vez disso, ele desfragmenta um banco de dados em vigor.</span><span class="sxs-lookup"><span data-stu-id="9a609-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="9a609-115">Por fim, o **JetDefragment2** recupera o espaço interno do banco de dados para reutilização, mas não libera espaço em excesso para o sistema de arquivos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9a609-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="9a609-116">O formato resultante dos dados pode ser muito mais eficiente, mas geralmente não é o ideal.</span><span class="sxs-lookup"><span data-stu-id="9a609-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="9a609-117">A desfragmentação é limitada à liberação de páginas de banco de dados para reutilização que contêm dados que já foram excluídos logicamente.</span><span class="sxs-lookup"><span data-stu-id="9a609-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="9a609-118">A desfragmentação também torna as páginas de banco de dados disponíveis para reutilização em alguns casos, combinando dados de duas páginas quando elas podem caber em uma única página.</span><span class="sxs-lookup"><span data-stu-id="9a609-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="9a609-119">Essa operação é diferente de [JetCompact](./jetcompact-function.md) , que faz uma cópia de um banco de dados somente leitura em um formato altamente ideal.</span><span class="sxs-lookup"><span data-stu-id="9a609-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

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

### <a name="parameters"></a><span data-ttu-id="9a609-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a609-120">Parameters</span></span>

<span data-ttu-id="9a609-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9a609-121">*sesid*</span></span>

<span data-ttu-id="9a609-122">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="9a609-122">The session to use for this call.</span></span>

<span data-ttu-id="9a609-123">*DBID*</span><span class="sxs-lookup"><span data-stu-id="9a609-123">*dbid*</span></span>

<span data-ttu-id="9a609-124">O banco de dados a ser desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="9a609-124">The database to defragment.</span></span>

<span data-ttu-id="9a609-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="9a609-125">*szTableName*</span></span>

<span data-ttu-id="9a609-126">Parâmetro não utilizado.</span><span class="sxs-lookup"><span data-stu-id="9a609-126">Unused parameter.</span></span> <span data-ttu-id="9a609-127">A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.</span><span class="sxs-lookup"><span data-stu-id="9a609-127">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="9a609-128">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="9a609-128">*pcPasses*</span></span>

<span data-ttu-id="9a609-129">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o número máximo de passagens de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-129">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="9a609-130">Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido como o número de passagens executadas.</span><span class="sxs-lookup"><span data-stu-id="9a609-130">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="9a609-131">Quando esse parâmetro é definido como NULL, o número de passagens de desfragmentação online é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9a609-131">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="9a609-132">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="9a609-132">*pcSeconds*</span></span>

<span data-ttu-id="9a609-133">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o tempo máximo para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-133">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="9a609-134">Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido com o período de tempo usado para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-134">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="9a609-135">Quando esse parâmetro é definido como nulo ou se *pcSeconds* aponta para um valor negativo, o tempo máximo para desfragmentação é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9a609-135">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="9a609-136">*retorno de chamada*</span><span class="sxs-lookup"><span data-stu-id="9a609-136">*callback*</span></span>

<span data-ttu-id="9a609-137">Função de retorno de chamada que a desfragmentação chama regularmente para relatar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9a609-137">Callback function that defragmentation calls regularly to report progress.</span></span>

<span data-ttu-id="9a609-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9a609-138">*grbit*</span></span>

<span data-ttu-id="9a609-139">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a609-139">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a609-140">Valor</span><span class="sxs-lookup"><span data-stu-id="9a609-140">Value</span></span></p></th>
<th><p><span data-ttu-id="9a609-141">Significado</span><span class="sxs-lookup"><span data-stu-id="9a609-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a609-142">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="9a609-142">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="9a609-143">Essa opção é usada para desfragmentar a parte de espaço disponível da alocação de espaço do banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="9a609-143">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="9a609-144">O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="9a609-144">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="9a609-145">O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9a609-145">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="9a609-146">O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</span><span class="sxs-lookup"><span data-stu-id="9a609-146">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-147">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="9a609-147">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="9a609-148">Essa opção é usada para iniciar uma nova tarefa de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-148">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-149">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="9a609-149">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="9a609-150">Essa opção é usada para interromper uma tarefa de desfragmentação iniciada existente.</span><span class="sxs-lookup"><span data-stu-id="9a609-150">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-151">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="9a609-151">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="9a609-152">Essa opção é usada para desfragmentar uma árvore B.</span><span class="sxs-lookup"><span data-stu-id="9a609-152">This option is used to defrag a B-Tree.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9a609-153">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9a609-153">Return Value</span></span>

<span data-ttu-id="9a609-154">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a609-154">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9a609-155">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9a609-155">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a609-156">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9a609-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="9a609-157">Description</span><span class="sxs-lookup"><span data-stu-id="9a609-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a609-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9a609-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9a609-159">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9a609-159">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-160">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9a609-160">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9a609-161">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9a609-161">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-162">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="9a609-162">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9a609-163">O banco de dados escolhido para desfragmentação é somente leitura e não pode ser atualizado de nenhuma forma, incluindo a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-163">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="9a609-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="9a609-165">A sessão fornecida está no estado preparado para confirmar e não pode iniciar novas atualizações até que a transação atual seja confirmada ou revertida.</span><span class="sxs-lookup"><span data-stu-id="9a609-165">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-166">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9a609-166">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9a609-167">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="9a609-167">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9a609-168">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9a609-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-169">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="9a609-169">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="9a609-170">A ID de banco de dados fornecida não corresponde a um banco de dados conhecido na instância.</span><span class="sxs-lookup"><span data-stu-id="9a609-170">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-171">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9a609-171">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9a609-172">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="9a609-172">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9a609-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9a609-174">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="9a609-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-175">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9a609-175">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9a609-176">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9a609-176">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="9a609-177">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9a609-177">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-178">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9a609-178">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9a609-179">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="9a609-179">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-180">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="9a609-180">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9a609-181">A sessão fornecida tem somente privilégios somente leitura e não pode iniciar uma tarefa que possa executar uma atualização, incluindo a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="9a609-181">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-182">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9a609-182">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9a609-183">Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</span><span class="sxs-lookup"><span data-stu-id="9a609-183">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-184">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="9a609-184">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="9a609-185">A opção JET_bitDefragmentBatchStart foi aprovada, mas uma tarefa de desfragmentação já está executando a desfragmentação no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="9a609-185">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-186">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="9a609-186">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="9a609-187">A opção JET_bitDefragmentBatchStop foi aprovada, mas nenhuma tarefa de desfragmentação está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="9a609-187">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a609-188">Em caso de sucesso, a ação solicitada de iniciar uma tarefa de desfragmentação para determinados dados com determinadas opções é executada ou a ação de parar uma tarefa de desfragmentação existente é executada.</span><span class="sxs-lookup"><span data-stu-id="9a609-188">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="9a609-189">Em caso de falha, a ação solicitada de iniciar ou parar um trabalho de desfragmentação online não é feita.</span><span class="sxs-lookup"><span data-stu-id="9a609-189">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="9a609-190">Nenhum outro efeito colateral ocorre.</span><span class="sxs-lookup"><span data-stu-id="9a609-190">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9a609-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a609-191">Remarks</span></span>

<span data-ttu-id="9a609-192">A desfragmentação online é controlada por uma configuração de parâmetro, bem como por essa API.</span><span class="sxs-lookup"><span data-stu-id="9a609-192">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="9a609-193">O valor do parâmetro do sistema padrão é JET_OnlineDefragAll, o que significa que a desfragmentação está habilitada para todas as estruturas de dados com suporte.</span><span class="sxs-lookup"><span data-stu-id="9a609-193">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="9a609-194">No entanto, usando o [JetSetSystemParameter](./jetsetsystemparameter-function.md), é possível desabilitar a desfragmentação online ou habilitá-la seletivamente somente para árvores de espaço de banco de dados, somente para bancos, somente para arquivos de streaming ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="9a609-194">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="9a609-195">Se a configuração do sistema para desfragmentação online for para uma configuração obsoleta, **JetDefragment2** tratará a configuração como JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="9a609-195">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="9a609-196">Pode haver, no máximo, uma tarefa em execução para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9a609-196">There can at most be one task running for each database.</span></span> <span data-ttu-id="9a609-197">A tarefa é executada como um thread no processo que hospeda o ESE.</span><span class="sxs-lookup"><span data-stu-id="9a609-197">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="9a609-198">A sessão usada para iniciar a tarefa de desfragmentação online pode ser usada posteriormente para operações de banco de dados enquanto a tarefa de desfragmentação continuar, pois a tarefa de desfragmentação aloca sua própria sessão.</span><span class="sxs-lookup"><span data-stu-id="9a609-198">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="9a609-199">A sessão fornecida é usada apenas para verificar as permissões associadas à sessão de início da tarefa e não é realmente usada para as operações de desfragmentação propriamente ditas.</span><span class="sxs-lookup"><span data-stu-id="9a609-199">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9a609-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a609-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a609-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9a609-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9a609-202">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a609-202">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-203"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9a609-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9a609-204">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9a609-204">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-205"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9a609-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9a609-206">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9a609-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-207"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="9a609-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9a609-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9a609-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a609-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9a609-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9a609-210">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9a609-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a609-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9a609-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9a609-212">Implementado como <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9a609-212">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9a609-213">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9a609-213">See Also</span></span>

[<span data-ttu-id="9a609-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9a609-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9a609-215">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9a609-215">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9a609-216">JetCompact</span><span class="sxs-lookup"><span data-stu-id="9a609-216">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="9a609-217">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="9a609-217">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="9a609-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9a609-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9a609-219">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9a609-219">JetStopService</span></span>](./jetstopservice-function.md)
