---
description: 'Saiba mais sobre: função JetCreateInstance'
title: Função JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793685"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="14a0a-103">Função JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="14a0a-103">JetCreateInstance Function</span></span>


<span data-ttu-id="14a0a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="14a0a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="14a0a-105">Função JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="14a0a-105">JetCreateInstance Function</span></span>

<span data-ttu-id="14a0a-106">A função **JetCreateInstance** aloca uma nova instância do mecanismo de banco de dados para uso em um único processo.</span><span class="sxs-lookup"><span data-stu-id="14a0a-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="14a0a-107">**Windows XP: o JetCreateInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="14a0a-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="14a0a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14a0a-108">Parameters</span></span>

<span data-ttu-id="14a0a-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="14a0a-109">*pinstance*</span></span>

<span data-ttu-id="14a0a-110">O buffer de saída que recebe a instância recém-criada.</span><span class="sxs-lookup"><span data-stu-id="14a0a-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="14a0a-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="14a0a-111">*szInstanceName*</span></span>

<span data-ttu-id="14a0a-112">Um identificador de cadeia de caracteres exclusivo para a instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="14a0a-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="14a0a-113">Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="14a0a-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="14a0a-114">**Observação** Um valor nulo é tratado como um identificador de cadeia de caracteres válido para uma instância.</span><span class="sxs-lookup"><span data-stu-id="14a0a-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="14a0a-115">Somente uma instância pode ter um identificador de cadeia de caracteres nulo.</span><span class="sxs-lookup"><span data-stu-id="14a0a-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="14a0a-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="14a0a-116">Return Value</span></span>

<span data-ttu-id="14a0a-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="14a0a-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="14a0a-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="14a0a-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14a0a-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="14a0a-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="14a0a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="14a0a-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a0a-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="14a0a-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="14a0a-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="14a0a-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a0a-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="14a0a-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="14a0a-124">O nome de instância especificado já está em uso para este processo.</span><span class="sxs-lookup"><span data-stu-id="14a0a-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a0a-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="14a0a-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="14a0a-126">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="14a0a-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="14a0a-127">Isso pode ocorrer para <strong>JetCreateInstance</strong> quando <em>pinstance</em> é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="14a0a-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a0a-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="14a0a-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="14a0a-129">A operação falhou porque não pode ser usada quando o mecanismo de banco de dados está operando em modo de instância única (modo de compatibilidade do Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="14a0a-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a0a-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="14a0a-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="14a0a-131">Não foi possível criar uma nova instância porque o número máximo de instâncias foi atingido.</span><span class="sxs-lookup"><span data-stu-id="14a0a-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="14a0a-132">O número máximo de instâncias com suporte é configurado usando o <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="14a0a-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14a0a-133">Em caso de êxito, uma nova instância será alocada e o identificador para ela será retornado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="14a0a-134">Neste ponto, todos os parâmetros do sistema para a instância terão os valores dos parâmetros do sistema padrão global.</span><span class="sxs-lookup"><span data-stu-id="14a0a-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="14a0a-135">Depois que uma instância for alocada, ela precisará ser terminada e/ou liberada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="14a0a-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="14a0a-136">Em caso de falha, um erro que representa a causa da falha será retornado e nenhuma instância será alocada.</span><span class="sxs-lookup"><span data-stu-id="14a0a-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="14a0a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="14a0a-137">Remarks</span></span>

<span data-ttu-id="14a0a-138">Uma instância deve ser inicializada com uma chamada para [JetInit](./jetinit-function.md) antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="14a0a-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="14a0a-139">Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="14a0a-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="14a0a-140">O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por [JET_paramMaxInstances](./resource-parameters.md), que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="14a0a-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="14a0a-141">Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="14a0a-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="14a0a-142">Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="14a0a-143">Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="14a0a-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="14a0a-144">Se a função for bem sucedido, o mecanismo de banco de dados será automaticamente alterado para o modo de várias instâncias como um efeito colateral dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="14a0a-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="14a0a-145">Se o aplicativo desejar permitir apenas uma instância no processo, [JetInit](./jetinit-function.md) deverá ser usado para iniciar o mecanismo de banco de dados no modo de compatibilidade do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="14a0a-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="14a0a-146">Se houver, o *szDisplayName* será usado para identificar a instância em locais como o log de eventos ou para outros chamadores, como aplicativos de backup (por meio de funções como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="14a0a-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="14a0a-147">Se o nome de exibição não for fornecido, o *szInstanceName* exclusivo será usado, em vez disso, se estiver presente, caso contrário, uma cadeia de caracteres vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="14a0a-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="14a0a-148">Se o mecanismo não tiver o modo de execução definido, após essa chamada, ele será definido como modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="14a0a-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="14a0a-149">A sequência de inicialização típica para um processo que potencialmente executa várias instâncias do Jet seria:</span><span class="sxs-lookup"><span data-stu-id="14a0a-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="14a0a-150">Uma chamada para [JetCreateInstance2](./jetcreateinstance2-function.md) que irá alocar e nomear a instância.</span><span class="sxs-lookup"><span data-stu-id="14a0a-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="14a0a-151">Várias chamadas para [JetSetSystemParameter](./jetsetsystemparameter-function.md) para essa instância a fim de definir diferentes parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="14a0a-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="14a0a-152">Observe que alguns parâmetros do sistema precisam ser exclusivos por instância (como [JET_paramSystemPath](./transaction-log-parameters.md) ou [JET_paramLogFilePath](./transaction-log-parameters.md)), portanto, provavelmente, será necessário definir cada um deles.</span><span class="sxs-lookup"><span data-stu-id="14a0a-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="14a0a-153">Inicie a instância usando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="14a0a-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="14a0a-154">Para encerrar e/ou liberar uma instância, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) precisa ser usado.</span><span class="sxs-lookup"><span data-stu-id="14a0a-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="14a0a-155">Se esta for a primeira instância a ser iniciada, haverá várias etapas adicionais que serão executadas durante essa chamada para fazer a inicialização e a configuração básica do sistema.</span><span class="sxs-lookup"><span data-stu-id="14a0a-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="14a0a-156">Várias etapas podem resultar em erros específicos, começando com JET_errOutOfMemory, mas outros também (consulte os erros acima).</span><span class="sxs-lookup"><span data-stu-id="14a0a-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="14a0a-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a0a-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a0a-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="14a0a-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="14a0a-159">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="14a0a-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a0a-160"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="14a0a-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="14a0a-161">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="14a0a-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a0a-162"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="14a0a-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="14a0a-163">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="14a0a-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a0a-164"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="14a0a-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="14a0a-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="14a0a-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a0a-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="14a0a-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="14a0a-167">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="14a0a-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a0a-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="14a0a-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="14a0a-169">Implementado como <strong>JetCreateInstanceW</strong> (Unicode) e <strong>JetCreateInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="14a0a-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="14a0a-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="14a0a-170">See Also</span></span>

[<span data-ttu-id="14a0a-171">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="14a0a-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="14a0a-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="14a0a-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="14a0a-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="14a0a-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="14a0a-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="14a0a-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="14a0a-175">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="14a0a-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="14a0a-176">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="14a0a-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="14a0a-177">JetInit</span><span class="sxs-lookup"><span data-stu-id="14a0a-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="14a0a-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="14a0a-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="14a0a-179">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="14a0a-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="14a0a-180">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="14a0a-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="14a0a-181">JetTerm</span><span class="sxs-lookup"><span data-stu-id="14a0a-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="14a0a-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="14a0a-182">JetTerm2</span></span>](./jetterm2-function.md)
