---
description: 'Saiba mais sobre: função JetCreateInstance2'
title: Função JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af31e7e66d92cf7ebbc238ac54a9b331e6dc5362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780731"
---
# <a name="jetcreateinstance2-function"></a><span data-ttu-id="624b7-103">Função JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="624b7-103">JetCreateInstance2 Function</span></span>


<span data-ttu-id="624b7-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="624b7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance2-function"></a><span data-ttu-id="624b7-105">Função JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="624b7-105">JetCreateInstance2 Function</span></span>

<span data-ttu-id="624b7-106">A função **JetCreateInstance2** é usada para alocar uma nova instância do mecanismo de banco de dados para uso em um único processo, com um nome de exibição especificado.</span><span class="sxs-lookup"><span data-stu-id="624b7-106">The **JetCreateInstance2** function is used to allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="624b7-107">**Windows XP:** o **JetCreateInstance2** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="624b7-107">**Windows XP:**  **JetCreateInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="624b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="624b7-108">Parameters</span></span>

<span data-ttu-id="624b7-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="624b7-109">*pinstance*</span></span>

<span data-ttu-id="624b7-110">O buffer de saída que receberá a instância recém-criada.</span><span class="sxs-lookup"><span data-stu-id="624b7-110">The output buffer that will receive the newly created instance.</span></span>

<span data-ttu-id="624b7-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="624b7-111">*szInstanceName*</span></span>

<span data-ttu-id="624b7-112">Especifica um identificador de cadeia de caracteres exclusivo para a instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="624b7-112">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="624b7-113">Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="624b7-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="624b7-114">**Observação** Um valor nulo é tratado como um identificador de cadeia de caracteres válido para uma instância.</span><span class="sxs-lookup"><span data-stu-id="624b7-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="624b7-115">Somente uma instância pode ter um identificador de cadeia de caracteres nulo.</span><span class="sxs-lookup"><span data-stu-id="624b7-115">Only one instance may have a NULL string identifier.</span></span>

<span data-ttu-id="624b7-116">*szDisplayName*</span><span class="sxs-lookup"><span data-stu-id="624b7-116">*szDisplayName*</span></span>

<span data-ttu-id="624b7-117">Um nome de exibição para a instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="624b7-117">A display name for the instance to be created.</span></span> <span data-ttu-id="624b7-118">Quando esse parâmetro não estiver presente, seu valor será presumido como nulo.</span><span class="sxs-lookup"><span data-stu-id="624b7-118">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="624b7-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="624b7-119">*grbit*</span></span>

<span data-ttu-id="624b7-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="624b7-120">Reserved for future use.</span></span> <span data-ttu-id="624b7-121">Quando esse parâmetro não estiver presente, seu valor será presumido como zero.</span><span class="sxs-lookup"><span data-stu-id="624b7-121">When this parameter is not present, its value is presumed to be zero.</span></span>

### <a name="return-value"></a><span data-ttu-id="624b7-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="624b7-122">Return Value</span></span>

<span data-ttu-id="624b7-123">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="624b7-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="624b7-124">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="624b7-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="624b7-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="624b7-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="624b7-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="624b7-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="624b7-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="624b7-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="624b7-128">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="624b7-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="624b7-129">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="624b7-129">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="624b7-130">O nome de instância especificado já está em uso para este processo.</span><span class="sxs-lookup"><span data-stu-id="624b7-130">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="624b7-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="624b7-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="624b7-132">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="624b7-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="624b7-133">Isso pode ocorrer para <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> quando <em>pinstance</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="624b7-133">This can happen for <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> when <em>pinstance</em> is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="624b7-134">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="624b7-134">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="624b7-135">A operação falhou porque não pode ser usada quando o mecanismo de banco de dados está operando em modo de instância única (modo de compatibilidade do Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="624b7-135">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="624b7-136">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="624b7-136">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="624b7-137">Não foi possível criar uma nova instância porque o número máximo de instâncias foi atingido.</span><span class="sxs-lookup"><span data-stu-id="624b7-137">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="624b7-138">O número máximo de instâncias com suporte é configurado usando o <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="624b7-138">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="624b7-139">Em caso de êxito, uma nova instância será alocada e o identificador para ela será retornado.</span><span class="sxs-lookup"><span data-stu-id="624b7-139">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="624b7-140">Neste ponto, todos os parâmetros do sistema para a instância terão os valores dos parâmetros do sistema padrão global.</span><span class="sxs-lookup"><span data-stu-id="624b7-140">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="624b7-141">Depois que uma instância for alocada, ela precisará ser terminada e/ou liberada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="624b7-141">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="624b7-142">Em caso de falha, um erro que representa a causa da falha será retornado e nenhuma instância será alocada.</span><span class="sxs-lookup"><span data-stu-id="624b7-142">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="624b7-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="624b7-143">Remarks</span></span>

<span data-ttu-id="624b7-144">Uma instância deve ser inicializada com uma chamada para [JetInit](./jetinit-function.md) antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="624b7-144">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="624b7-145">Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="624b7-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="624b7-146">O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por *JET_paramMaxInstances*, que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="624b7-146">The maximum number of instances that may be created at any one time is controlled by *JET_paramMaxInstances*, which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="624b7-147">Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="624b7-147">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="624b7-148">Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado.</span><span class="sxs-lookup"><span data-stu-id="624b7-148">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="624b7-149">Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="624b7-149">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="624b7-150">Se a função for bem sucedido, o mecanismo de banco de dados será automaticamente alterado para o modo de várias instâncias como um efeito colateral dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="624b7-150">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="624b7-151">Se o aplicativo desejar permitir apenas uma instância no processo, [JetInit](./jetinit-function.md) deverá ser usado para iniciar o mecanismo de banco de dados no modo de compatibilidade do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="624b7-151">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="624b7-152">Se estiver presente, o parâmetro *szDisplayName* será usado para identificar a instância em locais como log de eventos ou em relação a outros chamadores, como aplicativos de backup (por meio de funções como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="624b7-152">If present, the *szDisplayName* parameter will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="624b7-153">Se o nome de exibição não for fornecido, o parâmetro *szInstanceName* exclusivo será usado, se presente, caso contrário, uma cadeia de caracteres vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="624b7-153">If the display name is not provided, the unique *szInstanceName* parameter will be used instead, if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="624b7-154">Se o mecanismo não tiver o modo de execução definido, após essa chamada, ele será definido como modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="624b7-154">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="624b7-155">A sequência de inicialização típica para um processo que potencialmente executa várias instâncias do Jet seria:</span><span class="sxs-lookup"><span data-stu-id="624b7-155">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="624b7-156">Uma chamada para **JetCreateInstance2** que irá alocar e nomear a instância.</span><span class="sxs-lookup"><span data-stu-id="624b7-156">A call to **JetCreateInstance2** which will allocate and name the instance.</span></span>

  - <span data-ttu-id="624b7-157">Várias chamadas para [JetSetSystemParameter](./jetsetsystemparameter-function.md) para essa instância a fim de definir diferentes parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="624b7-157">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="624b7-158">Observe que alguns parâmetros do sistema precisam ser exclusivos para cada instância (como *JET_paramSystemPath* ou *JET_paramLogFilePath*), portanto, é mais provável que cada um deles precise ser definido.</span><span class="sxs-lookup"><span data-stu-id="624b7-158">Note that some system parameters need to be unique for each instance (like *JET_paramSystemPath* or *JET_paramLogFilePath*) so most likely, each of these will need to be set.</span></span>

  - <span data-ttu-id="624b7-159">Inicie a instância usando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="624b7-159">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="624b7-160">Para encerrar e/ou liberar uma instância, use [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="624b7-160">In order to terminate and/or free an instance, use [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="624b7-161">Se esta for a primeira instância a ser iniciada, haverá várias etapas adicionais que serão executadas durante essa chamada para fazer a inicialização e a configuração básica do sistema.</span><span class="sxs-lookup"><span data-stu-id="624b7-161">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="624b7-162">Várias etapas podem resultar em erros específicos, começando com JET_errOutOfMemory, mas outros também (consulte valores de retorno para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="624b7-162">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see Return Values for more information).</span></span>

#### <a name="requirements"></a><span data-ttu-id="624b7-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="624b7-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="624b7-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="624b7-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="624b7-165">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="624b7-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="624b7-166"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="624b7-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="624b7-167">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="624b7-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="624b7-168"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="624b7-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="624b7-169">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="624b7-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="624b7-170"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="624b7-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="624b7-171">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="624b7-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="624b7-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="624b7-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="624b7-173">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="624b7-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="624b7-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="624b7-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="624b7-175">Implementado como <strong>JetCreateInstance2W</strong> (Unicode) e <strong>JetCreateInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="624b7-175">Implemented as <strong>JetCreateInstance2W</strong> (Unicode) and <strong>JetCreateInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="624b7-176">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="624b7-176">See Also</span></span>

[<span data-ttu-id="624b7-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="624b7-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="624b7-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="624b7-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="624b7-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="624b7-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="624b7-180">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="624b7-180">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="624b7-181">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="624b7-181">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="624b7-182">JetInit</span><span class="sxs-lookup"><span data-stu-id="624b7-182">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="624b7-183">JetInit2</span><span class="sxs-lookup"><span data-stu-id="624b7-183">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="624b7-184">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="624b7-184">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="624b7-185">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="624b7-185">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="624b7-186">JetTerm</span><span class="sxs-lookup"><span data-stu-id="624b7-186">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="624b7-187">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="624b7-187">JetTerm2</span></span>](./jetterm2-function.md)
