---
description: 'Saiba mais sobre: função JetOSSnapshotPrepare'
title: Função JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752754"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="56f57-103">Função JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="56f57-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="56f57-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56f57-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="56f57-105">Função JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="56f57-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="56f57-106">A função **JetOSSnapshotPrepare** começa a preparação para uma sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="56f57-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="56f57-107">Uma sessão de instantâneo é um intervalo de tempo curto no qual o mecanismo não emite nenhum IOs de gravação para o disco, para que o mecanismo possa participar de uma sessão de instantâneo de volume (quando controlada por um gravador de instantâneo).</span><span class="sxs-lookup"><span data-stu-id="56f57-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="56f57-108">**Windows XP:** o **JetOSSnapshotPrepare** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="56f57-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="56f57-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56f57-109">Parameters</span></span>

<span data-ttu-id="56f57-110">*psnapId*</span><span class="sxs-lookup"><span data-stu-id="56f57-110">*psnapId*</span></span>

<span data-ttu-id="56f57-111">O identificador da sessão de instantâneo a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="56f57-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="56f57-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="56f57-112">*grbit*</span></span>

<span data-ttu-id="56f57-113">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="56f57-113">The options for this call.</span></span> <span data-ttu-id="56f57-114">Esse parâmetro pode ter uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="56f57-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56f57-115">Valor</span><span class="sxs-lookup"><span data-stu-id="56f57-115">Value</span></span></p></th>
<th><p><span data-ttu-id="56f57-116">Significado</span><span class="sxs-lookup"><span data-stu-id="56f57-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56f57-117">0</span><span class="sxs-lookup"><span data-stu-id="56f57-117">0</span></span></p></td>
<td><p><span data-ttu-id="56f57-118">Instantâneo normal.</span><span class="sxs-lookup"><span data-stu-id="56f57-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f57-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="56f57-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="56f57-120">Somente os arquivos de log serão criados.</span><span class="sxs-lookup"><span data-stu-id="56f57-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56f57-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="56f57-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="56f57-122">Um instantâneo de cópia (normal ou incremental) sem truncamento de log.</span><span class="sxs-lookup"><span data-stu-id="56f57-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f57-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="56f57-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="56f57-124">A sessão de instantâneo ocorre após <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> e exigirá uma chamada de função <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</span><span class="sxs-lookup"><span data-stu-id="56f57-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56f57-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="56f57-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="56f57-126">Nenhuma instância será preparada por padrão.</span><span class="sxs-lookup"><span data-stu-id="56f57-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="56f57-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="56f57-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="56f57-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="56f57-128">Return Value</span></span>

<span data-ttu-id="56f57-129">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="56f57-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56f57-130">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56f57-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56f57-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="56f57-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="56f57-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="56f57-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56f57-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56f57-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56f57-134">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="56f57-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f57-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="56f57-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="56f57-136">O ponteiro da ID do instantâneo é nulo ou o parâmetro <em>grbit</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="56f57-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56f57-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="56f57-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="56f57-138">Uma sessão de instantâneo já está em andamento e a operação não tem permissão para ter mais de uma sessão de instantâneo em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="56f57-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56f57-139">Se essa função for realizada com sucesso, uma sessão de instantâneo será capaz de iniciar a qualquer momento com a fase de congelamento de e/s.</span><span class="sxs-lookup"><span data-stu-id="56f57-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="56f57-140">O identificador da sessão será retornado e deverá ser usado nas chamadas subsequentes para a sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="56f57-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="56f57-141">As instâncias em execução do mecanismo agora serão consideradas parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="56f57-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="56f57-142">**Windows Vista:**  Para especificar um subconjunto diferente de instâncias, o [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="56f57-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="56f57-143">A chamada de sequência de API normal é: **JetOSSnapshotPrepare**, opcionalmente seguido por uma ou mais chamadas para [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="56f57-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="56f57-144">Quando o congelamento é iniciado, ele pode ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="56f57-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="56f57-145">A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada abruptamente com [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="56f57-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="56f57-146">Se JET_bitContinueAfterThaw for especificado após [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), a sessão de instantâneo permanecerá (embora a e/s seja retomada).</span><span class="sxs-lookup"><span data-stu-id="56f57-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="56f57-147">Isso permitirá uma verificação do instantâneo e, se necessário, habilitará o truncamento de log usando [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) e exigirá uma chamada para [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span><span class="sxs-lookup"><span data-stu-id="56f57-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="56f57-148">Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="56f57-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="56f57-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="56f57-149">Remarks</span></span>

<span data-ttu-id="56f57-150">As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="56f57-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="56f57-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f57-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56f57-152"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="56f57-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56f57-153">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56f57-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f57-154"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="56f57-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56f57-155">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56f57-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56f57-156"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="56f57-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56f57-157">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="56f57-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f57-158"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="56f57-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56f57-159">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="56f57-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56f57-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="56f57-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56f57-161">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="56f57-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56f57-162">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="56f57-162">See Also</span></span>

[<span data-ttu-id="56f57-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56f57-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56f57-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="56f57-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="56f57-165">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="56f57-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="56f57-166">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="56f57-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="56f57-167">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="56f57-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="56f57-168">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="56f57-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="56f57-169">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="56f57-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="56f57-170">JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="56f57-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)
