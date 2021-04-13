---
description: 'Saiba mais sobre: função JetOSSnapshotFreeze'
title: Função JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170723"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="7a8e6-103">Função JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="7a8e6-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="7a8e6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7a8e6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="7a8e6-105">Função JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="7a8e6-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="7a8e6-106">A função **JetOSSnapshotFreeze** inicia um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="7a8e6-107">Enquanto o instantâneo está em andamento, nenhuma atividade de gravação em disco pelo mecanismo pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="7a8e6-108">**Windows XP:** o **JetOSSnapshotFreeze** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="7a8e6-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7a8e6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a8e6-109">Parameters</span></span>

<span data-ttu-id="7a8e6-110">*snapid*</span><span class="sxs-lookup"><span data-stu-id="7a8e6-110">*snapId*</span></span>

<span data-ttu-id="7a8e6-111">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="7a8e6-112">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="7a8e6-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="7a8e6-113">O número de instâncias em execução no momento no mecanismo que fazem parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="7a8e6-114">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="7a8e6-114">*paInstanceInfo*</span></span>

<span data-ttu-id="7a8e6-115">Uma matriz de estruturas, uma para cada instância em execução que faz parte da sessão de instantâneo, descrevendo a instância e os bancos de dados que fazem parte dela.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="7a8e6-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7a8e6-116">*grbit*</span></span>

<span data-ttu-id="7a8e6-117">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-117">The options for this call.</span></span> <span data-ttu-id="7a8e6-118">Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="7a8e6-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7a8e6-119">Return Value</span></span>

<span data-ttu-id="7a8e6-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7a8e6-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7a8e6-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a8e6-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7a8e6-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="7a8e6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a8e6-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7a8e6-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a8e6-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7a8e6-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-127">Os ponteiros fornecidos para os parâmetros de saída são nulos, a sessão de instantâneo é inválida ou o parâmetro <em>grbit</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="7a8e6-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-129">A sessão de instantâneo não está no estado apropriado para iniciar um congelamento (por exemplo, um congelamento anterior falhou nesta sessão antes).</span><span class="sxs-lookup"><span data-stu-id="7a8e6-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a8e6-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="7a8e6-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-131">O mecanismo não está em um estado no qual um instantâneo pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="7a8e6-132">Um ou mais backups de streaming já estão em andamento ou uma ou mais instâncias estão passando por etapas de recuperação ou terminando.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="7a8e6-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-134">O identificador da sessão de instantâneo não é válido.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a8e6-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="7a8e6-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-136">A função falhou devido a uma condição de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="7a8e6-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="7a8e6-138">A função falhou porque um novo thread que está fazendo a congelamento falhou ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a8e6-139">Se essa função for realizada com sucesso, não haverá nenhum IOs de gravação emitido para os arquivos de banco de dados ou para os arquivos de log que fazem parte das instâncias que estão congeladas.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="7a8e6-140">Além disso, as informações da instância serão preenchidas corretamente e deverão ser liberadas posteriormente chamando [JetFreeBuffer](./jetfreebuffer-function.md) com o ponteiro para a matriz de informações da instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="7a8e6-141">Se essa função falhar, o mecanismo continuará funcionando normalmente com o IOs ocorrendo como de costume.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="7a8e6-142">Não é necessário chamar [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) se a congelamento falhar.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="7a8e6-143">Além disso, as informações da instância não serão preenchidas, portanto, não é necessário liberar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7a8e6-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a8e6-144">Remarks</span></span>

<span data-ttu-id="7a8e6-145">Durante o período de congelamento, não haverá nenhum IOs de gravação emitido para os bancos de dados anexados ou os logs de transações, embora possa haver um IOs de gravação emitido para os bancos de dados temporários ou arquivos de streaming.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="7a8e6-146">O estado no qual os bancos de dados e os arquivos de log estarão durante o congelamento (o estado em que os arquivos estaria em uma imagem de instantâneo de volume) será de forma que uma recuperação normal seja possível se esses arquivos forem restaurados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="7a8e6-147">Como não há nenhuma operação de gravação durante o período de congelamento, as chamadas de API normais no mecanismo podem ser interrompidas para esse intervalo.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="7a8e6-148">O aplicativo cliente deve ser capaz de lidar com chamadas de API que podem demorar mais tempo normal se um congelamento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="7a8e6-149">Devido aos possíveis efeitos descritos acima, há um tempo limite interno após o qual a sessão de instantâneo interromperá a fase congelar, mesmo que as APIs que fazem a descongelação ou anulação não tenham sido chamadas.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="7a8e6-150">O valor do tempo limite pode ser alterado usando o parâmetro do sistema [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8e6-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="7a8e6-151">Observe que o intervalo de congelamento típico está no intervalo de 10 segundos com o tempo limite padrão em cerca de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7a8e6-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a8e6-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7a8e6-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7a8e6-154">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a8e6-155"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="7a8e6-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7a8e6-156">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-157"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="7a8e6-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7a8e6-158">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a8e6-159"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="7a8e6-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7a8e6-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a8e6-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7a8e6-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7a8e6-162">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7a8e6-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a8e6-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7a8e6-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7a8e6-164">Implementado como <strong>JetOSSnapshotFreezeW</strong> (Unicode) e <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7a8e6-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7a8e6-165">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7a8e6-165">See Also</span></span>

[<span data-ttu-id="7a8e6-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7a8e6-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7a8e6-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="7a8e6-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="7a8e6-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="7a8e6-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="7a8e6-169">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="7a8e6-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="7a8e6-170">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="7a8e6-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="7a8e6-171">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="7a8e6-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="7a8e6-172">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="7a8e6-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
