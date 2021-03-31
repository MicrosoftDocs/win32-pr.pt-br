---
description: 'Saiba mais sobre: função JetOSSnapshotEnd'
title: Função JetOSSnapshotEnd
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089881"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="ee2b7-103">Função JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="ee2b7-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="ee2b7-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee2b7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="ee2b7-105">Função JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="ee2b7-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="ee2b7-106">A função **JetOSSnapshotEnd** notifica o mecanismo de que a sessão de instantâneo foi concluída.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="ee2b7-107">**Windows Vista:** o **JetOSSnapshotEnd** é introduzido no Windows Vista:.  </span><span class="sxs-lookup"><span data-stu-id="ee2b7-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ee2b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee2b7-108">Parameters</span></span>

<span data-ttu-id="ee2b7-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="ee2b7-109">*snapId*</span></span>

<span data-ttu-id="ee2b7-110">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="ee2b7-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ee2b7-111">*grbit*</span></span>

<span data-ttu-id="ee2b7-112">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-112">The options for this call.</span></span> <span data-ttu-id="ee2b7-113">Esse parâmetro pode ter uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee2b7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ee2b7-114">Value</span></span></p></th>
<th><p><span data-ttu-id="ee2b7-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ee2b7-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-116">0</span><span class="sxs-lookup"><span data-stu-id="ee2b7-116">0</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-117">A extremidade bem-sucedida da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2b7-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="ee2b7-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-119">A sessão de instantâneo foi anulada.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ee2b7-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ee2b7-120">Return Value</span></span>

<span data-ttu-id="ee2b7-121">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ee2b7-122">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ee2b7-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee2b7-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ee2b7-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="ee2b7-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee2b7-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ee2b7-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-126">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2b7-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="ee2b7-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-128">Uma das opções solicitadas é inválida, usada incorretamente ou não implementada.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="ee2b7-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-130">Uma sessão de instantâneo já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="ee2b7-131">Isso não é permitido.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2b7-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="ee2b7-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-133">O identificador da sessão de instantâneo não é válido.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="ee2b7-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="ee2b7-135">A sessão de instantâneo tinha um tempo limite interno antes que essa chamada tivesse ocorrido.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="ee2b7-136">Como resultado, as operações de e/s retornadas para normal antes que essa chamada fosse feita.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee2b7-137">Se essa função for bem sucedido, uma sessão de instantâneo será concluída e o comportamento normal do mecanismo será retomado.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="ee2b7-138">Uma nova sessão de instantâneo pode ser iniciada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="ee2b7-139">Se essa função falhar, o JET_errOSSnapshotTimeOut retorno de código retornado e a sessão de instantâneo atual terminará, mas o congelamento do IOs durante o período de instantâneo não foi respeitado internamente.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="ee2b7-140">Para todos os outros erros, o estado da sessão de instantâneo não será alterado.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ee2b7-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee2b7-141">Remarks</span></span>

<span data-ttu-id="ee2b7-142">Essa função será chamada somente se [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) tiver sido chamado com JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="ee2b7-143">A sessão de instantâneo deve ser concluída para que a verificação de instantâneo e o truncamento de log ocorram.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="ee2b7-144">As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ee2b7-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2b7-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ee2b7-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2b7-147">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2b7-148"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ee2b7-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2b7-149">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-150"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ee2b7-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2b7-151">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2b7-152"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="ee2b7-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2b7-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2b7-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ee2b7-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2b7-155">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ee2b7-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ee2b7-156">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ee2b7-156">See Also</span></span>

[<span data-ttu-id="ee2b7-157">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="ee2b7-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="ee2b7-158">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="ee2b7-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="ee2b7-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ee2b7-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ee2b7-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="ee2b7-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
