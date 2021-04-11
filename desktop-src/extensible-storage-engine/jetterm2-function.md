---
description: 'Saiba mais sobre: função JetTerm2'
title: Função JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090655"
---
# <a name="jetterm2-function"></a><span data-ttu-id="733c3-103">Função JetTerm2</span><span class="sxs-lookup"><span data-stu-id="733c3-103">JetTerm2 Function</span></span>


<span data-ttu-id="733c3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="733c3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="733c3-105">Função JetTerm2</span><span class="sxs-lookup"><span data-stu-id="733c3-105">JetTerm2 Function</span></span>

<span data-ttu-id="733c3-106">A função **JetTerm2** inicia o desligamento de uma instância que foi inicializada pelo [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="733c3-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="733c3-107">**JetTerm2** também pode destruir uma instância não inicializada que foi criada pelo [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="733c3-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="733c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="733c3-108">Parameters</span></span>

<span data-ttu-id="733c3-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="733c3-109">*instance*</span></span>

<span data-ttu-id="733c3-110">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="733c3-110">The instance to use for this call.</span></span>

<span data-ttu-id="733c3-111">**Windows 2000:**  Esse parâmetro é ignorado e sempre deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="733c3-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="733c3-112">**Windows XP e versões posteriores:**  Este parâmetro está sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="733c3-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="733c3-113">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="733c3-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="733c3-114">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser um ponteiro para uma instância que foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="733c3-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="733c3-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="733c3-115">*grbit*</span></span>

<span data-ttu-id="733c3-116">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="733c3-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="733c3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="733c3-117">Value</span></span></p></th>
<th><p><span data-ttu-id="733c3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="733c3-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="733c3-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="733c3-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="733c3-120">Solicita que a instância seja desligada corretamente.</span><span class="sxs-lookup"><span data-stu-id="733c3-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="733c3-121">Qualquer trabalho de limpeza opcional que normalmente seria feito em segundo plano em tempo de execução é concluído imediatamente.</span><span class="sxs-lookup"><span data-stu-id="733c3-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="733c3-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="733c3-123">Solicita que a instância seja desligada o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="733c3-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="733c3-124">Qualquer trabalho opcional que normalmente seria feito em segundo plano em tempo de execução é abandonado.</span><span class="sxs-lookup"><span data-stu-id="733c3-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="733c3-125"><strong>Observação</strong>  Essa opção pode causar perda de espaço temporária ou permanente no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="733c3-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="733c3-126">Esse espaço perdido sempre pode ser recuperado por meio de uma desfragmentação offline do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="733c3-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c3-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="733c3-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="733c3-128">Solicita que a instância seja desligada mesmo que atualmente haja um backup em andamento.</span><span class="sxs-lookup"><span data-stu-id="733c3-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="733c3-129">Normalmente, um backup pendente faria com que o <a href="gg269298(v=exchg.10).md">JetTerm</a> falhasse com JET_errBackupInProgress.</span><span class="sxs-lookup"><span data-stu-id="733c3-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="733c3-130">Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitTermAbrupt.</span><span class="sxs-lookup"><span data-stu-id="733c3-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="733c3-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="733c3-132">Solicita que a instância seja desligada com todos os bancos de dados anexados deixados em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="733c3-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="733c3-133">Windows 7: o JET_bitTermDirty é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="733c3-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="733c3-134">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="733c3-134">Return Value</span></span>

<span data-ttu-id="733c3-135">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="733c3-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="733c3-136">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="733c3-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="733c3-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="733c3-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="733c3-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="733c3-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="733c3-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="733c3-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="733c3-140">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="733c3-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="733c3-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="733c3-142">A operação não pode ser concluída porque uma operação de backup está em andamento na instância.</span><span class="sxs-lookup"><span data-stu-id="733c3-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c3-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="733c3-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="733c3-144">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="733c3-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="733c3-145">Esse erro será retornado por <a href="gg269298(v=exchg.10).md">JetTerm</a> quando o mecanismo estiver no modo de várias instâncias e quando <em>pinstance</em> se referir a uma instância inválida.</span><span class="sxs-lookup"><span data-stu-id="733c3-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="733c3-146"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="733c3-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="733c3-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="733c3-148">A operação não pode ser concluída porque a instância ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="733c3-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c3-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="733c3-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="733c3-150">A operação não pode ser concluída porque a instância está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="733c3-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="733c3-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="733c3-152">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância.</span><span class="sxs-lookup"><span data-stu-id="733c3-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c3-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="733c3-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="733c3-154">A instância não pode ser desligada porque existem sessões com transações ativas para a instância especificada.</span><span class="sxs-lookup"><span data-stu-id="733c3-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="733c3-155">Esse erro ocorrerá somente se o JET_bitTermComplete for usado.</span><span class="sxs-lookup"><span data-stu-id="733c3-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="733c3-156">Se essa função for realizada com sucesso, a instância especificada será desligada.</span><span class="sxs-lookup"><span data-stu-id="733c3-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="733c3-157">O identificador de instância também será fechado e ficará indisponível para qualquer API que usa um identificador de instância.</span><span class="sxs-lookup"><span data-stu-id="733c3-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="733c3-158">Todos os outros objetos associados à instância, como sessões, também serão fechados.</span><span class="sxs-lookup"><span data-stu-id="733c3-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="733c3-159">O estado do arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância serão modificados durante o processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="733c3-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="733c3-160">Se essa função falhar como resultado de um erro de uso, a instância permanecerá em um estado inicializado e nada será alterado.</span><span class="sxs-lookup"><span data-stu-id="733c3-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="733c3-161">Caso contrário, a instância ainda será desligada conforme indicado para o caso de êxito.</span><span class="sxs-lookup"><span data-stu-id="733c3-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="733c3-162">A diferença é que a instância precisará passar pela recuperação de pane quando for inicializada na próxima vez.</span><span class="sxs-lookup"><span data-stu-id="733c3-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="733c3-163">O mecanismo tentará liberar o máximo de dados possível para minimizar a quantidade de recuperação necessária.</span><span class="sxs-lookup"><span data-stu-id="733c3-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="733c3-164">Conceitualmente, essa falha de [JetTerm](./jetterm-function.md) não é diferente de uma falha de processo.</span><span class="sxs-lookup"><span data-stu-id="733c3-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="733c3-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="733c3-165">Remarks</span></span>

<span data-ttu-id="733c3-166">Consulte [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="733c3-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="733c3-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733c3-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="733c3-168"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="733c3-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="733c3-169">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="733c3-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-170"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="733c3-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="733c3-171">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="733c3-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c3-172"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="733c3-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="733c3-173">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="733c3-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c3-174"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="733c3-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="733c3-175">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="733c3-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c3-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="733c3-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="733c3-177">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="733c3-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="733c3-178">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="733c3-178">See Also</span></span>

[<span data-ttu-id="733c3-179">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="733c3-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="733c3-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="733c3-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="733c3-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="733c3-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="733c3-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="733c3-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="733c3-183">JetInit</span><span class="sxs-lookup"><span data-stu-id="733c3-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="733c3-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="733c3-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="733c3-185">JetTerm</span><span class="sxs-lookup"><span data-stu-id="733c3-185">JetTerm</span></span>](./jetterm-function.md)
