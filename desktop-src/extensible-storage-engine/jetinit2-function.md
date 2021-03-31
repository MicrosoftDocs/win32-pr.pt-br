---
description: 'Saiba mais sobre: função JetInit2'
title: Função JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930780"
---
# <a name="jetinit2-function"></a><span data-ttu-id="c3eda-103">Função JetInit2</span><span class="sxs-lookup"><span data-stu-id="c3eda-103">JetInit2 Function</span></span>


<span data-ttu-id="c3eda-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c3eda-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="c3eda-105">Função JetInit2</span><span class="sxs-lookup"><span data-stu-id="c3eda-105">JetInit2 Function</span></span>

<span data-ttu-id="c3eda-106">A função **JetInit2** coloca o mecanismo de banco de dados em um estado em que ele pode dar suporte ao uso do aplicativo de arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c3eda-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="c3eda-107">O mecanismo já deve estar configurado corretamente para inicialização usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="c3eda-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="c3eda-108">A recuperação de falhas no banco de dados é executada automaticamente como parte do processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="c3eda-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="c3eda-109">**Windows XP:** o **JetInit2** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="c3eda-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="c3eda-110">Essa função está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="c3eda-110">This function is obsolete.</span></span> <span data-ttu-id="c3eda-111">Use [JetInit3](./jetinit3-function.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c3eda-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="c3eda-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3eda-112">Parameters</span></span>

<span data-ttu-id="c3eda-113">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="c3eda-113">*pinstance*</span></span>

<span data-ttu-id="c3eda-114">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c3eda-114">The instance to use for this call.</span></span>

<span data-ttu-id="c3eda-115">Para o Windows 2000, esse parâmetro é ignorado e sempre deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c3eda-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="c3eda-116">Para o Windows XP e versões posteriores, o uso desse parâmetro depende do modo de operação do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="c3eda-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="c3eda-117">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser nulo ou poderá ser definido como um buffer de saída válido contendo nulo ou JET_instanceNil que retorna o identificador de instância global criado como um efeito colateral da inicialização.</span><span class="sxs-lookup"><span data-stu-id="c3eda-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="c3eda-118">Esse identificador de instância pode então ser passado para qualquer outra API que usa uma instância.</span><span class="sxs-lookup"><span data-stu-id="c3eda-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="c3eda-119">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser definido como um buffer de entrada válido que contenha o identificador de instância retornado pelo [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="c3eda-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="c3eda-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c3eda-120">*grbit*</span></span>

<span data-ttu-id="c3eda-121">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3eda-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3eda-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c3eda-122">Value</span></span></p></th>
<th><p><span data-ttu-id="c3eda-123">Significado</span><span class="sxs-lookup"><span data-stu-id="c3eda-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="c3eda-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="c3eda-125">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c3eda-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3eda-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="c3eda-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="c3eda-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c3eda-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="c3eda-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="c3eda-129">Essa opção permite que o usuário execute a recuperação em um conjunto de arquivos de log, sem que todos os bancos de dados estejam presentes, que foram anexados em um ponto do conjunto de logs.</span><span class="sxs-lookup"><span data-stu-id="c3eda-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3eda-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="c3eda-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="c3eda-131">Execute a recuperação, mas pare na fase de desfazer.</span><span class="sxs-lookup"><span data-stu-id="c3eda-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="c3eda-132">Isso permite que os logs de transações adicionais sejam copiados e aplicados.</span><span class="sxs-lookup"><span data-stu-id="c3eda-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="c3eda-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="c3eda-134">Na recuperação reversível bem-sucedida, TRUNCATE os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="c3eda-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3eda-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="c3eda-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="c3eda-136">Padrão de entrada de mapa de banco de dados ausente para o mesmo local.</span><span class="sxs-lookup"><span data-stu-id="c3eda-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="c3eda-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="c3eda-138">Ignorar logs perdidos do final do fluxo de log.</span><span class="sxs-lookup"><span data-stu-id="c3eda-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="c3eda-139"><strong>Windows 7: o JET_bitReplayIgnoreLostLogs</strong> é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3eda-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c3eda-140">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c3eda-140">Return Value</span></span>

<span data-ttu-id="c3eda-141">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3eda-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c3eda-142">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c3eda-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="c3eda-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3eda-143">Remarks</span></span>

<span data-ttu-id="c3eda-144">Uma instância deve ser inicializada com uma chamada para **JetInit2** antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="c3eda-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="c3eda-145">Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c3eda-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="c3eda-146">Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c3eda-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="c3eda-147">Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado.</span><span class="sxs-lookup"><span data-stu-id="c3eda-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="c3eda-148">Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="c3eda-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="c3eda-149">Se a recuperação estiver em execução em um conjunto de logs, para os quais nem todos os bancos de dados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente desejar que a recuperação continue apesar dos bancos de dados ausentes, o JET_ bitReplayIgnoreMissingDB será usado para continuar a recuperação para os bancos de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c3eda-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="c3eda-150">Consulte a seção comentários em [JetInit](./jetinit-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c3eda-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c3eda-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3eda-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-152"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c3eda-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c3eda-153">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3eda-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3eda-154"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c3eda-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c3eda-155">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3eda-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-156"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c3eda-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c3eda-157">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c3eda-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3eda-158"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="c3eda-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c3eda-159">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c3eda-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3eda-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c3eda-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c3eda-161">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c3eda-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c3eda-162">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c3eda-162">See Also</span></span>

[<span data-ttu-id="c3eda-163">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="c3eda-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="c3eda-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c3eda-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c3eda-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c3eda-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c3eda-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3eda-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c3eda-167">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c3eda-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c3eda-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="c3eda-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c3eda-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="c3eda-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="c3eda-170">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c3eda-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c3eda-171">Parâmetros do recurso</span><span class="sxs-lookup"><span data-stu-id="c3eda-171">Resource Parameters</span></span>](./resource-parameters.md)
