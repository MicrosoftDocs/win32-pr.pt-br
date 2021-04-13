---
description: 'Saiba mais sobre: função JetInit3'
title: Função JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297733"
---
# <a name="jetinit3-function"></a><span data-ttu-id="92166-103">Função JetInit3</span><span class="sxs-lookup"><span data-stu-id="92166-103">JetInit3 Function</span></span>


<span data-ttu-id="92166-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="92166-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="92166-105">Função JetInit3</span><span class="sxs-lookup"><span data-stu-id="92166-105">JetInit3 Function</span></span>

<span data-ttu-id="92166-106">A função **JetInit3** coloca o mecanismo de banco de dados em um estado no qual ele pode dar suporte ao uso do aplicativo de arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="92166-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="92166-107">O mecanismo já deve estar configurado corretamente para inicialização, o que você realiza usando a função [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="92166-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="92166-108">Observe que a recuperação de falhas do banco de dados ocorre automaticamente como parte do processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="92166-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="92166-109">**Windows Vista:** o **JetInit3** é introduzido no Windows Vista.  </span><span class="sxs-lookup"><span data-stu-id="92166-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="92166-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92166-110">Parameters</span></span>

<span data-ttu-id="92166-111">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="92166-111">*pinstance*</span></span>

<span data-ttu-id="92166-112">A instância que você usa para uma chamada específica.</span><span class="sxs-lookup"><span data-stu-id="92166-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="92166-113">O uso desse parâmetro depende do modo de operação do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="92166-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="92166-114">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000), no qual apenas uma instância tem suporte, você poderá definir esse parâmetro como **NULL** ou como um buffer de saída válido contendo **NULL** ou JET_instanceNil, que retorna o identificador de instância global criado como um efeito colateral da inicialização.</span><span class="sxs-lookup"><span data-stu-id="92166-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="92166-115">Esse identificador de instância pode então ser passado para qualquer outra API que usa uma instância.</span><span class="sxs-lookup"><span data-stu-id="92166-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="92166-116">Se o mecanismo estiver operando no modo de várias instâncias, você deverá definir esse parâmetro como um buffer de entrada válido que contenha o identificador de instância retornado pela função [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="92166-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="92166-117">*prstInfo*</span><span class="sxs-lookup"><span data-stu-id="92166-117">*prstInfo*</span></span>

<span data-ttu-id="92166-118">Parâmetros de recuperação adicionais usados para remapear bancos de dados durante a recuperação, para definir a posição em que a recuperação será interrompida ou para determinar o status de recuperação atual.</span><span class="sxs-lookup"><span data-stu-id="92166-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="92166-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="92166-119">*grbit*</span></span>

<span data-ttu-id="92166-120">Um grupo de bits que especifica zero ou mais das opções listadas e definidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="92166-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92166-121">Valor</span><span class="sxs-lookup"><span data-stu-id="92166-121">Value</span></span></p></th>
<th><p><span data-ttu-id="92166-122">Significado</span><span class="sxs-lookup"><span data-stu-id="92166-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92166-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="92166-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="92166-124">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="92166-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92166-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="92166-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="92166-126">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="92166-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92166-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="92166-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="92166-128">Esse valor permite que o usuário execute a recuperação em um conjunto de arquivos de log, mesmo na ausência dos bancos de dados que foram anexados ao arquivo de log definido em algum momento.</span><span class="sxs-lookup"><span data-stu-id="92166-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92166-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="92166-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="92166-130">Esse valor permite que o usuário execute a recuperação, mas apenas até (e não incluindo) a fase de desfazer.</span><span class="sxs-lookup"><span data-stu-id="92166-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="92166-131">Usando esse valor, os logs de transações adicionais podem ser copiados e aplicados.</span><span class="sxs-lookup"><span data-stu-id="92166-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92166-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="92166-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="92166-133">Esse valor faz com que os arquivos de log sejam truncados durante uma recuperação de software bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="92166-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92166-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="92166-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="92166-135">Esse valor faz com que uma entrada de mapa de banco de dados ausente seja padrão para o mesmo local.</span><span class="sxs-lookup"><span data-stu-id="92166-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92166-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="92166-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="92166-137">Esse valor faz com que os logs perdidos do final do fluxo de log sejam ignorados durante uma recuperação.</span><span class="sxs-lookup"><span data-stu-id="92166-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="92166-138"><strong>Windows 7: o JET_bitReplayIgnoreLostLogs</strong> é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92166-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="92166-139">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="92166-139">Return Value</span></span>

<span data-ttu-id="92166-140">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="92166-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="92166-141">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="92166-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="92166-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="92166-142">Remarks</span></span>

<span data-ttu-id="92166-143">Uma instância deve ser inicializada com uma chamada para a função **JetInit3** antes que possa ser usada por algo diferente da função [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="92166-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="92166-144">Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando a função [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="92166-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="92166-145">Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="92166-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="92166-146">Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado.</span><span class="sxs-lookup"><span data-stu-id="92166-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="92166-147">Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="92166-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="92166-148">Observe que [JetTerm](./jetterm-function.md) não deve ser chamado se a função **JetInit3** falhar.</span><span class="sxs-lookup"><span data-stu-id="92166-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="92166-149">No entanto, [JetTerm](./jetterm-function.md) ainda deve ser chamado para todas as instâncias criadas por **JetCreateInstance2** se **JetInit3** nunca foi chamado ou se **JetInit3** tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="92166-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="92166-150">Se a recuperação estiver em execução em um conjunto de logs para os quais nem todos os bancos de dados relacionados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente quiser que a recuperação continue apesar dos bancos de dados ausentes, o erro JET_bitReplayIgnoreMissingDB será usado para continuar a recuperação para os bancos de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="92166-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="92166-151">Como a recuperação de falha geralmente não acontece no mesmo computador (e com a mesma configuração) que no momento da falha, um banco de dados normalmente não altera o local.</span><span class="sxs-lookup"><span data-stu-id="92166-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="92166-152">Em determinados cenários, como a movimentação de arquivos para um computador diferente ou a restauração de backup de instantâneo em locais diferentes, isso não é mais verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="92166-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="92166-153">A função **JetInit3** permite que você especifique um mapeamento (usando as estruturas [JET_RSTINFO](./jet-rstinfo-structure.md) e [JET_RSTMAP](./jet-rstmap-structure.md) ) entre o local do banco de dados antigo e seu novo local.</span><span class="sxs-lookup"><span data-stu-id="92166-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="92166-154">Na verdade, você precisa apenas do novo local, desde que os arquivos de banco de dados estejam presentes nesse local.</span><span class="sxs-lookup"><span data-stu-id="92166-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="92166-155">Assim que você souber os locais dos bancos de dados restaurados, a assinatura do banco de dados será usada para identificar o banco de dados por meio do processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="92166-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="92166-156">Você precisará do local do banco de dados original somente se precisar recriar um banco de dados, caso em que a assinatura é conhecida.</span><span class="sxs-lookup"><span data-stu-id="92166-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="92166-157">Além disso, se você precisar interromper uma recuperação após uma operação de desfazer, poderá especificar uma posição de log específica na qual a recuperação será interrompida.</span><span class="sxs-lookup"><span data-stu-id="92166-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="92166-158">Observe que isso inclui a capacidade de parar no final de uma geração de log específica se a posição especificada fizer parte da geração, mas após o final do log real.</span><span class="sxs-lookup"><span data-stu-id="92166-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="92166-159">Para obter mais informações, consulte a seção "Comentários" no tópico [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="92166-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="92166-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92166-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92166-161">Cliente</span><span class="sxs-lookup"><span data-stu-id="92166-161">Client</span></span></p></td>
<td><p><span data-ttu-id="92166-162">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92166-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92166-163">Servidor</span><span class="sxs-lookup"><span data-stu-id="92166-163">Server</span></span></p></td>
<td><p><span data-ttu-id="92166-164">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="92166-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92166-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92166-165">Header</span></span></p></td>
<td><p><span data-ttu-id="92166-166">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="92166-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92166-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92166-167">Library</span></span></p></td>
<td><p><span data-ttu-id="92166-168">Usa ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="92166-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92166-169">DLL</span><span class="sxs-lookup"><span data-stu-id="92166-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="92166-170">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="92166-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92166-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="92166-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="92166-172">Implementado como <strong>JetInit3W</strong> (Unicode) e <strong>JetInit3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="92166-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="92166-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="92166-173">See Also</span></span>

[<span data-ttu-id="92166-174">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="92166-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="92166-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="92166-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="92166-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="92166-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="92166-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="92166-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="92166-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="92166-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="92166-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="92166-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="92166-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="92166-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="92166-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="92166-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="92166-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="92166-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="92166-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="92166-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="92166-184">Parâmetros do recurso</span><span class="sxs-lookup"><span data-stu-id="92166-184">Resource Parameters</span></span>](./resource-parameters.md)
