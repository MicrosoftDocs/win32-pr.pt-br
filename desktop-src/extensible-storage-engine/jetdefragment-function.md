---
description: 'Saiba mais sobre: função JetDefragment'
title: Função JetDefragment
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297636"
---
# <a name="jetdefragment-function"></a><span data-ttu-id="6653a-103">Função JetDefragment</span><span class="sxs-lookup"><span data-stu-id="6653a-103">JetDefragment Function</span></span>


<span data-ttu-id="6653a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6653a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment-function"></a><span data-ttu-id="6653a-105">Função JetDefragment</span><span class="sxs-lookup"><span data-stu-id="6653a-105">JetDefragment Function</span></span>

<span data-ttu-id="6653a-106">A função **JetDefragment** é iniciada e interrompe as tarefas de desfragmentação do banco de dados que aprimoram a organização em um banco de dado.</span><span class="sxs-lookup"><span data-stu-id="6653a-106">The **JetDefragment** function starts and stops database defragmentation tasks that improves data organization within a database.</span></span> <span data-ttu-id="6653a-107">Isso é feito para limitar o crescimento do banco de dados usando a alocação de disco existente com mais eficiência no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6653a-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="6653a-108">Ele também pode reduzir o conjunto de trabalho, garantindo que os dados sejam mais bem compactados.</span><span class="sxs-lookup"><span data-stu-id="6653a-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="6653a-109">Por fim, ele pode melhorar o desempenho do aplicativo acelerando as operações comuns por meio de uma melhor organização de dados.</span><span class="sxs-lookup"><span data-stu-id="6653a-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="6653a-110">A desfragmentação de banco de dados é uma operação online e não interrompe a atividade de banco de dados regular, como operações de consulta ou atualizações de data.</span><span class="sxs-lookup"><span data-stu-id="6653a-110">Database defragmentation is an online operation and does not interrupt regular database activity, such as query operations or data updates.</span></span> <span data-ttu-id="6653a-111">O **JetDefragment** também não faz uma cópia de todos os dados existentes.</span><span class="sxs-lookup"><span data-stu-id="6653a-111">**JetDefragment** also does not make a copy of all existing data.</span></span> <span data-ttu-id="6653a-112">Em vez disso, ele desfragmenta um banco de dados em vigor.</span><span class="sxs-lookup"><span data-stu-id="6653a-112">Instead, it defragments a database in place.</span></span> <span data-ttu-id="6653a-113">Por fim, o **JetDefragment** recupera o espaço interno do banco de dados para reutilização, mas não libera espaço em excesso para o sistema de arquivos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6653a-113">Lastly, **JetDefragment** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="6653a-114">O formato resultante dos dados pode ser muito mais eficiente, mas geralmente não é o ideal.</span><span class="sxs-lookup"><span data-stu-id="6653a-114">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="6653a-115">A desfragmentação é limitada à liberação de páginas de banco de dados para reutilização que contêm dados que já foram excluídos logicamente.</span><span class="sxs-lookup"><span data-stu-id="6653a-115">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="6653a-116">A desfragmentação também torna as páginas de banco de dados disponíveis para reutilização em alguns casos, combinando dados de duas páginas quando elas podem caber em uma única página.</span><span class="sxs-lookup"><span data-stu-id="6653a-116">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="6653a-117">Essa operação é diferente de [JetCompact](./jetcompact-function.md) , que faz uma cópia de um banco de dados somente leitura em um formato altamente ideal.</span><span class="sxs-lookup"><span data-stu-id="6653a-117">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6653a-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6653a-118">Parameters</span></span>

<span data-ttu-id="6653a-119">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6653a-119">*sesid*</span></span>

<span data-ttu-id="6653a-120">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="6653a-120">The session to use for this call.</span></span>

<span data-ttu-id="6653a-121">*DBID*</span><span class="sxs-lookup"><span data-stu-id="6653a-121">*dbid*</span></span>

<span data-ttu-id="6653a-122">O banco de dados que será desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="6653a-122">The database that will be defragmented.</span></span>

<span data-ttu-id="6653a-123">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="6653a-123">*szTableName*</span></span>

<span data-ttu-id="6653a-124">Parâmetro não utilizado.</span><span class="sxs-lookup"><span data-stu-id="6653a-124">Unused parameter.</span></span> <span data-ttu-id="6653a-125">A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.</span><span class="sxs-lookup"><span data-stu-id="6653a-125">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="6653a-126">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="6653a-126">*pcPasses*</span></span>

<span data-ttu-id="6653a-127">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada define o número máximo de passagens de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-127">When starting an online defragmentation task, this input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="6653a-128">Ao parar uma tarefa de desfragmentação online, esse buffer de saída é definido como o número de passagens executadas.</span><span class="sxs-lookup"><span data-stu-id="6653a-128">When stopping an online defragmentation task, this output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="6653a-129">Quando esse parâmetro é definido como NULL, o número de passagens de desfragmentação online é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="6653a-129">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="6653a-130">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="6653a-130">*pcSeconds*</span></span>

<span data-ttu-id="6653a-131">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada define o tempo máximo para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-131">When starting an online defragmentation task, this input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="6653a-132">Ao parar uma tarefa de desfragmentação online, esse buffer de saída é definido com o período de tempo usado para desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-132">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="6653a-133">Quando esse parâmetro é definido como nulo ou se *pcSeconds* aponta para um valor negativo, o tempo máximo para desfragmentação é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="6653a-133">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="6653a-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6653a-134">*grbit*</span></span>

<span data-ttu-id="6653a-135">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6653a-135">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6653a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6653a-136">Value</span></span></p></th>
<th><p><span data-ttu-id="6653a-137">Significado</span><span class="sxs-lookup"><span data-stu-id="6653a-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6653a-138">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="6653a-138">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="6653a-139">Desfragmenta a parte de espaço disponível da alocação de espaço do banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="6653a-139">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="6653a-140">O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="6653a-140">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="6653a-141">O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6653a-141">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="6653a-142">O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</span><span class="sxs-lookup"><span data-stu-id="6653a-142">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-143">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="6653a-143">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="6653a-144">Inicia uma nova tarefa de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-144">Starts a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-145">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="6653a-145">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="6653a-146">Interrompe uma tarefa de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-146">Stops a defragmentation task.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6653a-147">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6653a-147">Return Value</span></span>

<span data-ttu-id="6653a-148">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6653a-148">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6653a-149">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6653a-149">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6653a-150">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6653a-150">Return code</span></span></p></th>
<th><p><span data-ttu-id="6653a-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="6653a-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6653a-152">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6653a-152">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6653a-153">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6653a-153">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-154">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6653a-154">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6653a-155">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="6653a-155">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-156">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="6653a-156">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6653a-157">O banco de dados escolhido para desfragmentação é somente leitura e não pode ser atualizado de nenhuma forma, incluindo a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-157">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="6653a-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="6653a-159">A sessão fornecida está no estado preparado para confirmar e não pode iniciar novas atualizações até que a transação atual seja confirmada ou revertida.</span><span class="sxs-lookup"><span data-stu-id="6653a-159">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6653a-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6653a-161">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="6653a-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6653a-162">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="6653a-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-163">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="6653a-163">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="6653a-164">A ID de banco de dados fornecida não corresponde a um banco de dados conhecido na instância.</span><span class="sxs-lookup"><span data-stu-id="6653a-164">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-165">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6653a-165">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6653a-166">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="6653a-166">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6653a-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6653a-168">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="6653a-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6653a-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6653a-170">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6653a-170">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="6653a-171">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="6653a-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6653a-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6653a-173">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="6653a-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-174">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="6653a-174">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6653a-175">A sessão fornecida tem somente privilégios somente leitura e não pode iniciar uma tarefa que possa executar uma atualização, incluindo a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="6653a-175">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-176">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6653a-176">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6653a-177">Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</span><span class="sxs-lookup"><span data-stu-id="6653a-177">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-178">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="6653a-178">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="6653a-179">A opção JET_bitDefragmentBatchStart foi aprovada, mas uma tarefa de desfragmentação já está executando a desfragmentação no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="6653a-179">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-180">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="6653a-180">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="6653a-181">A opção JET_bitDefragmentBatchStop foi aprovada, mas nenhuma tarefa de desfragmentação está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="6653a-181">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6653a-182">Em caso de sucesso, a ação solicitada de iniciar uma tarefa de desfragmentação para determinados dados com determinadas opções é executada ou a ação de parar uma tarefa de desfragmentação existente é executada.</span><span class="sxs-lookup"><span data-stu-id="6653a-182">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="6653a-183">Em caso de falha, a ação solicitada de iniciar ou parar um trabalho de desfragmentação online não é feita.</span><span class="sxs-lookup"><span data-stu-id="6653a-183">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="6653a-184">Nenhum outro efeito colateral ocorre.</span><span class="sxs-lookup"><span data-stu-id="6653a-184">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6653a-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="6653a-185">Remarks</span></span>

<span data-ttu-id="6653a-186">A desfragmentação online é controlada por uma configuração de parâmetro, bem como por essa API.</span><span class="sxs-lookup"><span data-stu-id="6653a-186">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="6653a-187">O valor do parâmetro do sistema padrão é JET_OnlineDefragAll, o que significa que a desfragmentação está habilitada para todas as estruturas de dados com suporte.</span><span class="sxs-lookup"><span data-stu-id="6653a-187">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="6653a-188">No entanto, usando o [JetSetSystemParameter](./jetsetsystemparameter-function.md), é possível desabilitar a desfragmentação online ou habilitá-la seletivamente somente para árvores de espaço de banco de dados, somente para bancos, somente para arquivos de streaming ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="6653a-188">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="6653a-189">Se a configuração do sistema para desfragmentação online estiver definida como uma configuração obsoleta, **JetDefragment** tratará a configuração como JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="6653a-189">If the system setting for online defragmentation is set to an obsolete setting, **JetDefragment** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="6653a-190">Pode haver, no máximo, uma tarefa em execução para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6653a-190">There can at most be one task running for each database.</span></span> <span data-ttu-id="6653a-191">A tarefa é executada como um thread no processo que hospeda o ESE.</span><span class="sxs-lookup"><span data-stu-id="6653a-191">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="6653a-192">A sessão usada para iniciar a tarefa de desfragmentação online pode ser usada posteriormente para operações de banco de dados enquanto a tarefa de desfragmentação continuar, pois a tarefa de desfragmentação aloca sua própria sessão.</span><span class="sxs-lookup"><span data-stu-id="6653a-192">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="6653a-193">A sessão fornecida é usada apenas para verificar as permissões associadas à sessão de início da tarefa e não é realmente usada para as operações de desfragmentação propriamente ditas.</span><span class="sxs-lookup"><span data-stu-id="6653a-193">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6653a-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6653a-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6653a-195"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6653a-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6653a-196">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6653a-196">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-197"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6653a-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6653a-198">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6653a-198">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-199"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6653a-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6653a-200">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6653a-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-201"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6653a-201"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6653a-202">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6653a-202">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6653a-203"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6653a-203"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6653a-204">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6653a-204">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6653a-205"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6653a-205"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6653a-206">Implementado como <strong>JetDefragmentW</strong> (Unicode) e <strong>JetDefragmentA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6653a-206">Implemented as <strong>JetDefragmentW</strong> (Unicode) and <strong>JetDefragmentA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6653a-207">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6653a-207">See Also</span></span>

[<span data-ttu-id="6653a-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6653a-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6653a-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6653a-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6653a-210">JetCompact</span><span class="sxs-lookup"><span data-stu-id="6653a-210">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="6653a-211">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="6653a-211">JetDefragment2</span></span>](./jetdefragment2-function.md)  
[<span data-ttu-id="6653a-212">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6653a-212">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6653a-213">JetStopService</span><span class="sxs-lookup"><span data-stu-id="6653a-213">JetStopService</span></span>](./jetstopservice-function.md)
