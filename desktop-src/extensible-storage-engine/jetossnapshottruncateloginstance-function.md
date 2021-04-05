---
description: 'Saiba mais sobre: função JetOSSnapshotTruncateLogInstance'
title: Função JetOSSnapshotTruncateLogInstance
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646700"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="cd31d-103">Função JetOSSnapshotTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="cd31d-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="cd31d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd31d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="cd31d-105">Função JetOSSnapshotTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="cd31d-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="cd31d-106">A função **JetOSSnapshotTruncateLogInstance** trunca o log para uma instância especificada durante uma sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cd31d-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="cd31d-107">**Windows Vista:** o **JetOSSnapshotTruncateLogInstance** é introduzido no Windows Vista.  </span><span class="sxs-lookup"><span data-stu-id="cd31d-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="cd31d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd31d-108">Parameters</span></span>

<span data-ttu-id="cd31d-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="cd31d-109">*snapId*</span></span>

<span data-ttu-id="cd31d-110">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cd31d-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="cd31d-111">*cópia*</span><span class="sxs-lookup"><span data-stu-id="cd31d-111">*instance*</span></span>

<span data-ttu-id="cd31d-112">A instância que será usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="cd31d-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="cd31d-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cd31d-113">*grbit*</span></span>

<span data-ttu-id="cd31d-114">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="cd31d-114">The options for this call.</span></span> <span data-ttu-id="cd31d-115">Esse parâmetro pode ter uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd31d-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="cd31d-116">*grbit* pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="cd31d-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd31d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cd31d-117">Value</span></span></p></th>
<th><p><span data-ttu-id="cd31d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cd31d-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd31d-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="cd31d-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="cd31d-120">Todos os bancos de dados são anexados para que o mecanismo de armazenamento possa computar e fazer o truncamento de log.</span><span class="sxs-lookup"><span data-stu-id="cd31d-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd31d-121">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="cd31d-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="cd31d-122">Nenhum truncamento ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="cd31d-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cd31d-123">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cd31d-123">Return Value</span></span>

<span data-ttu-id="cd31d-124">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd31d-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cd31d-125">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd31d-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd31d-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cd31d-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="cd31d-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd31d-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd31d-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cd31d-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cd31d-129">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="cd31d-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd31d-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="cd31d-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="cd31d-131">O parâmetro <em>grbit</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="cd31d-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd31d-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="cd31d-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="cd31d-133">A sessão de instantâneo não está no estado em que pode ocorrer um truncamento.</span><span class="sxs-lookup"><span data-stu-id="cd31d-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="cd31d-134">Causas possíveis:</span><span class="sxs-lookup"><span data-stu-id="cd31d-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd31d-135">A chamada é concluída após o tempo limite da sessão de instantâneo expirar.</span><span class="sxs-lookup"><span data-stu-id="cd31d-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="cd31d-136">A sessão foi especificada como um instantâneo de cópia.</span><span class="sxs-lookup"><span data-stu-id="cd31d-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd31d-137">Se essa função for realizada com sucesso, os arquivos de log para uma ou todas as instâncias que fazem parte da sessão de instantâneo serão truncados, se possível.</span><span class="sxs-lookup"><span data-stu-id="cd31d-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cd31d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd31d-138">Remarks</span></span>

<span data-ttu-id="cd31d-139">Essa função deve ser chamada somente se o instantâneo tiver sido criado com a opção JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="cd31d-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="cd31d-140">Caso contrário, a sessão de instantâneo termina após a chamada para [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="cd31d-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="cd31d-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd31d-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd31d-142"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cd31d-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd31d-143">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd31d-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd31d-144"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="cd31d-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd31d-145">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cd31d-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd31d-146"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="cd31d-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd31d-147">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="cd31d-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd31d-148"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="cd31d-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cd31d-149">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cd31d-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd31d-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cd31d-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cd31d-151">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cd31d-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cd31d-152">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cd31d-152">See Also</span></span>

[<span data-ttu-id="cd31d-153">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="cd31d-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="cd31d-154">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="cd31d-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="cd31d-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cd31d-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cd31d-156">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="cd31d-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="cd31d-157">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="cd31d-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="cd31d-158">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="cd31d-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="cd31d-159">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="cd31d-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
