---
description: 'Saiba mais sobre: função JetOSSnapshotThaw'
title: Função JetOSSnapshotThaw
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837350"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="42587-103">Função JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="42587-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="42587-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="42587-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="42587-105">Função JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="42587-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="42587-106">A função **JetOSSnapshotThaw** notifica o mecanismo de que ele pode retomar as operações de e/s normais após um período de congelamento e um instantâneo bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="42587-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="42587-107">**Windows XP:** o **JetOSSnapshotThaw** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="42587-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="42587-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42587-108">Parameters</span></span>

<span data-ttu-id="42587-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="42587-109">*snapId*</span></span>

<span data-ttu-id="42587-110">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="42587-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="42587-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="42587-111">*grbit*</span></span>

<span data-ttu-id="42587-112">Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0.</span><span class="sxs-lookup"><span data-stu-id="42587-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="42587-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="42587-113">Return Value</span></span>

<span data-ttu-id="42587-114">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="42587-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="42587-115">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="42587-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42587-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="42587-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="42587-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="42587-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42587-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="42587-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="42587-119">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="42587-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42587-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="42587-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="42587-121">A sessão de instantâneo é inválida ou o parâmetro <em>grbit</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="42587-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42587-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="42587-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="42587-123">A sessão de instantâneo tinha um tempo limite interno antes que essa chamada tivesse ocorrido.</span><span class="sxs-lookup"><span data-stu-id="42587-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="42587-124">Consequentemente, as operações de e/s retornadas para normal antes que essa chamada fosse feita.</span><span class="sxs-lookup"><span data-stu-id="42587-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42587-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="42587-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="42587-126">O identificador da sessão de instantâneo não é válido.</span><span class="sxs-lookup"><span data-stu-id="42587-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42587-127">Se essa função for bem sucedido, uma sessão de instantâneo terminará e o comportamento normal do mecanismo será retomado.</span><span class="sxs-lookup"><span data-stu-id="42587-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="42587-128">Uma nova sessão de instantâneo pode ser iniciada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="42587-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="42587-129">Se essa função falhar, a sessão de instantâneo atual terminará, mas o congelamento do IOs durante o período de instantâneo não foi respeitado internamente.</span><span class="sxs-lookup"><span data-stu-id="42587-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="42587-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="42587-130">Remarks</span></span>

<span data-ttu-id="42587-131">As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="42587-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="42587-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42587-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42587-133"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="42587-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="42587-134">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="42587-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42587-135"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="42587-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="42587-136">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="42587-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42587-137"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="42587-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="42587-138">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="42587-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42587-139"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="42587-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="42587-140">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="42587-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42587-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="42587-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="42587-142">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="42587-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="42587-143">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="42587-143">See Also</span></span>

[<span data-ttu-id="42587-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="42587-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="42587-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="42587-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="42587-146">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="42587-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="42587-147">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="42587-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="42587-148">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="42587-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)
