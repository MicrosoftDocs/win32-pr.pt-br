---
description: 'Saiba mais sobre: função JetInit'
title: Função JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298892"
---
# <a name="jetinit-function"></a><span data-ttu-id="98e61-103">Função JetInit</span><span class="sxs-lookup"><span data-stu-id="98e61-103">JetInit Function</span></span>


<span data-ttu-id="98e61-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98e61-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="98e61-105">Função JetInit</span><span class="sxs-lookup"><span data-stu-id="98e61-105">JetInit Function</span></span>

<span data-ttu-id="98e61-106">A função **JetInit** coloca o mecanismo de banco de dados em um estado em que ele pode dar suporte ao uso do aplicativo de arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="98e61-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="98e61-107">O mecanismo já deve estar configurado corretamente para inicialização usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="98e61-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="98e61-108">A recuperação de falhas no banco de dados é executada automaticamente como parte do processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="98e61-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="98e61-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98e61-109">Parameters</span></span>

<span data-ttu-id="98e61-110">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="98e61-110">*pinstance*</span></span>

<span data-ttu-id="98e61-111">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="98e61-111">The instance to use for this call.</span></span>

<span data-ttu-id="98e61-112">Para o Windows 2000, esse parâmetro é ignorado e sempre deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="98e61-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="98e61-113">Para o Windows XP e versões posteriores, o uso desse parâmetro depende do modo de operação do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="98e61-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="98e61-114">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser nulo ou poderá ser definido como um buffer de saída válido que retornará o identificador de instância global criado como um efeito colateral da inicialização.</span><span class="sxs-lookup"><span data-stu-id="98e61-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="98e61-115">Esse buffer de saída deve ser definido como nulo ou JET_instanceNil.</span><span class="sxs-lookup"><span data-stu-id="98e61-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="98e61-116">Esse identificador de instância pode então ser passado para qualquer outra função que use uma instância do.</span><span class="sxs-lookup"><span data-stu-id="98e61-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="98e61-117">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser definido como um buffer de entrada válido que contenha o identificador de instância retornado pela instância de função [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="98e61-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="98e61-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="98e61-118">Remarks</span></span>

<span data-ttu-id="98e61-119">Uma instância deve ser inicializada com uma chamada para **JetInit** antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="98e61-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="98e61-120">Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="98e61-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="98e61-121">Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="98e61-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="98e61-122">Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado.</span><span class="sxs-lookup"><span data-stu-id="98e61-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="98e61-123">Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="98e61-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="98e61-124">O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por [JET_paramMaxInstances](./resource-parameters.md), que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="98e61-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="98e61-125">Quando o mecanismo de banco de dados é inicializado pela primeira vez, o **JetInit** criará um conjunto inicial de arquivos para dar suporte a essa instância.</span><span class="sxs-lookup"><span data-stu-id="98e61-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="98e61-126">Esses arquivos incluem um arquivo de ponto de verificação (chamado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), um conjunto de arquivos de log de transações reservadas (chamado RES1. LOG e RES2. LOG), um arquivo de log de transações inicial (chamado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) e um arquivo de banco de dados temporário (nomeado de acordo com [JET_paramTempPath](./temporary-database-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="98e61-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="98e61-127">Se [JET_paramRecovery](./transaction-log-parameters.md) for definido como "off", o arquivo de ponto de verificação e os arquivos de log não serão criados.</span><span class="sxs-lookup"><span data-stu-id="98e61-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="98e61-128">Se [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) for definido como zero, o arquivo de banco de dados temporário não será criado.</span><span class="sxs-lookup"><span data-stu-id="98e61-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="98e61-129">Esses arquivos representam a superfície do disco de uma instância e devem ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="98e61-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="98e61-130">Se esses arquivos forem corrompidos individualmente ou em relação um ao outro, os dados armazenados nos bancos de dados associados à instância poderão ser perdidos.</span><span class="sxs-lookup"><span data-stu-id="98e61-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="98e61-131">Quando o mecanismo de banco de dados é inicializado com um conjunto existente de arquivos de log de transações, esses arquivos serão inspecionados para ver se a versão anterior da instância sofreu uma falha.</span><span class="sxs-lookup"><span data-stu-id="98e61-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="98e61-132">Se uma falha for detectada, a recuperação de falha será executada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="98e61-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="98e61-133">Esse processo reconstruirá os bancos de dados anexados à instância durante a versão anterior do mecanismo e salvará as alterações de volta nos arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="98e61-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="98e61-134">O resultado será os bancos de dados que são consistentes com a transação.</span><span class="sxs-lookup"><span data-stu-id="98e61-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="98e61-135">É possível que esse processo demore um pouco de tempo se o número de arquivos de log de transações a serem reproduzidos em relação aos bancos de dados for grande.</span><span class="sxs-lookup"><span data-stu-id="98e61-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="98e61-136">Devido ao fato de que o **JetInit** executa a recuperação de pane, é possível que quase todos os erros do mecanismo de banco de dados sejam retornados em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="98e61-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="98e61-137">Na prática, a maioria dos erros vistos na implantação se enquadra em duas categorias: corrupção de dados e ingestão de arquivos.</span><span class="sxs-lookup"><span data-stu-id="98e61-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="98e61-138">Os dados corrompidos serão manifestados com mais frequência nos seguintes erros ou semelhantes:</span><span class="sxs-lookup"><span data-stu-id="98e61-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="98e61-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="98e61-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="98e61-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="98e61-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="98e61-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="98e61-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="98e61-142">Esses erros são quase sempre causados por problemas de hardware e, portanto, não podem ser evitados.</span><span class="sxs-lookup"><span data-stu-id="98e61-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="98e61-143">O ingerenciamento de arquivos será manifestado com mais frequência nos seguintes erros ou semelhantes:</span><span class="sxs-lookup"><span data-stu-id="98e61-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="98e61-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="98e61-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="98e61-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="98e61-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="98e61-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="98e61-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="98e61-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="98e61-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="98e61-148">Se a recuperação estiver em execução em um conjunto de logs, para os quais nem todos os bancos de dados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente desejar que a recuperação continue apesar dos bancos de dados ausentes, o JET_ bitReplayIgnoreMissingDB poderá ser usado para continuar a recuperação para os bancos de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98e61-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="98e61-149">Esses erros são impedidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="98e61-149">These errors are preventable by the application.</span></span> <span data-ttu-id="98e61-150">O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra a manipulação por forças externas, como o usuário ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="98e61-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="98e61-151">Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="98e61-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="98e61-152">Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância.</span><span class="sxs-lookup"><span data-stu-id="98e61-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="98e61-153">A função **JetInit** se comporta de forma diferente, com relação aos arquivos de banco de dados anexados à instância, entre o Windows 2000 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="98e61-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="98e61-154">**Windows 2000:**  No Windows 2000, qualquer banco de dados anexado à instância durante uma encarnação anterior dessa instância permanece anexado à instância depois que o **JetInit** é concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="98e61-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="98e61-155">Não é necessário chamar [JetAttachDatabase](./jetattachdatabase-function.md) após **JetInit** para garantir o acesso ao banco de dados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="98e61-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="98e61-156">Se a função [JetAttachDatabase](./jetattachdatabase-function.md) for chamada após a função **JetInit** , o aviso de JET_wrnDatabaseAttached será retornado.</span><span class="sxs-lookup"><span data-stu-id="98e61-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="98e61-157">Esse aviso indica que o anexo do banco de dados foi preservado e pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="98e61-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="98e61-158">**Windows XP:**  No Windows XP e versões posteriores, todos os bancos de dados são automaticamente desanexados da instância pelo **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="98e61-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="98e61-159">Isso significa que [JetAttachDatabase](./jetattachdatabase-function.md) sempre deve ser chamado depois de **JetInit** nesse caso.</span><span class="sxs-lookup"><span data-stu-id="98e61-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="98e61-160">Qualquer aplicativo escrito para ser executado no Windows 2000 e em versões posteriores deve sempre chamar [JetAttachDatabase](./jetattachdatabase-function.md) após **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="98e61-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="98e61-161">Se o aplicativo for executado no Windows 2000, ele deverá esperar ver JET_wrnDatabaseAttached em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="98e61-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="98e61-162">Consulte [JetAttachDatabase](./jetattachdatabase-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="98e61-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="98e61-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98e61-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98e61-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="98e61-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98e61-165">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="98e61-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98e61-166"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="98e61-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98e61-167">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98e61-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98e61-168"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="98e61-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98e61-169">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="98e61-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98e61-170"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="98e61-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98e61-171">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98e61-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98e61-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98e61-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98e61-173">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98e61-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98e61-174">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="98e61-174">See Also</span></span>

[<span data-ttu-id="98e61-175">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="98e61-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="98e61-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="98e61-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="98e61-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="98e61-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="98e61-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="98e61-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="98e61-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="98e61-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="98e61-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="98e61-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="98e61-181">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="98e61-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="98e61-182">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="98e61-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="98e61-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="98e61-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="98e61-184">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="98e61-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
