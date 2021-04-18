---
description: 'Saiba mais sobre: função JetOSSnapshotTruncateLog'
title: Função JetOSSnapshotTruncateLog
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750113"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="f34e3-103">Função JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="f34e3-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="f34e3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f34e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="f34e3-105">Função JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="f34e3-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="f34e3-106">A função **JetOSSnapshotTruncateLog** habilita o truncamento de log para todas as instâncias que fazem parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="f34e3-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="f34e3-107">**Windows Vista:** o **JetOSSnapshotTruncateLog** é introduzido no Windows Vista.  </span><span class="sxs-lookup"><span data-stu-id="f34e3-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f34e3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f34e3-108">Parameters</span></span>

<span data-ttu-id="f34e3-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="f34e3-109">*snapId*</span></span>

<span data-ttu-id="f34e3-110">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="f34e3-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="f34e3-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f34e3-111">*grbit*</span></span>

<span data-ttu-id="f34e3-112">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="f34e3-112">The options for this call.</span></span> <span data-ttu-id="f34e3-113">Esse parâmetro pode ter uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f34e3-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f34e3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f34e3-114">Value</span></span></p></th>
<th><p><span data-ttu-id="f34e3-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f34e3-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f34e3-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f34e3-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="f34e3-117">Todos os bancos de dados são anexados para que o mecanismo de armazenamento possa computar e fazer o truncamento de log.</span><span class="sxs-lookup"><span data-stu-id="f34e3-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f34e3-118">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="f34e3-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="f34e3-119">Nenhum truncamento ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="f34e3-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f34e3-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f34e3-120">Return Value</span></span>

<span data-ttu-id="f34e3-121">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="f34e3-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f34e3-122">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f34e3-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f34e3-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f34e3-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="f34e3-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="f34e3-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f34e3-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f34e3-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f34e3-126">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="f34e3-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f34e3-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="f34e3-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="f34e3-128">O parâmetro <em>grbit</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="f34e3-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f34e3-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="f34e3-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="f34e3-130">A sessão de instantâneo não está no estado em que pode ocorrer um truncamento.</span><span class="sxs-lookup"><span data-stu-id="f34e3-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="f34e3-131">Causas possíveis:</span><span class="sxs-lookup"><span data-stu-id="f34e3-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f34e3-132">a chamada é feita depois que o tempo limite da sessão de instantâneo for atingido</span><span class="sxs-lookup"><span data-stu-id="f34e3-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="f34e3-133">a sessão foi especificada como um instantâneo de cópia</span><span class="sxs-lookup"><span data-stu-id="f34e3-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f34e3-134">Em caso de êxito, os arquivos de log de uma ou todas as instâncias que fazem parte da sessão de instantâneo serão truncados, se possível.</span><span class="sxs-lookup"><span data-stu-id="f34e3-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f34e3-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="f34e3-135">Remarks</span></span>

<span data-ttu-id="f34e3-136">Essa função deve ser chamada somente se o instantâneo tiver sido criado com a opção JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="f34e3-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="f34e3-137">Caso contrário, a sessão de instantâneo teria terminado após a chamada [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f34e3-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f34e3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f34e3-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f34e3-139"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f34e3-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f34e3-140">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f34e3-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f34e3-141"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f34e3-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f34e3-142">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f34e3-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f34e3-143"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="f34e3-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f34e3-144">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f34e3-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f34e3-145"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="f34e3-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f34e3-146">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f34e3-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f34e3-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f34e3-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f34e3-148">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f34e3-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f34e3-149">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f34e3-149">See Also</span></span>

[<span data-ttu-id="f34e3-150">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="f34e3-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="f34e3-151">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="f34e3-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="f34e3-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f34e3-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f34e3-153">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="f34e3-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="f34e3-154">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="f34e3-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="f34e3-155">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="f34e3-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="f34e3-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="f34e3-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
