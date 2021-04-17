---
description: 'Saiba mais sobre: função JetOSSnapshotAbort'
title: Função JetOSSnapshotAbort
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780316"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="c6521-103">Função JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="c6521-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="c6521-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c6521-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="c6521-105">Função JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="c6521-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="c6521-106">A função **JetOSSnapshotAbort** notifica o mecanismo de que ele pode retomar as operações de e/s normais após um período de congelamento finalizado com um instantâneo com falha.</span><span class="sxs-lookup"><span data-stu-id="c6521-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="c6521-107">**Windows server 2003:** o **JetOSSnapshotAbort** é introduzido no Windows Server 2003.  </span><span class="sxs-lookup"><span data-stu-id="c6521-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c6521-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6521-108">Parameters</span></span>

<span data-ttu-id="c6521-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="c6521-109">*snapId*</span></span>

<span data-ttu-id="c6521-110">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c6521-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="c6521-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c6521-111">*grbit*</span></span>

<span data-ttu-id="c6521-112">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c6521-112">The options for this call.</span></span> <span data-ttu-id="c6521-113">Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c6521-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="c6521-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c6521-114">Return Value</span></span>

<span data-ttu-id="c6521-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6521-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c6521-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c6521-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6521-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c6521-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="c6521-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6521-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6521-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c6521-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c6521-120">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c6521-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6521-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c6521-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c6521-122">A sessão de instantâneo é inválida ou o parâmetro grbit é inválido.</span><span class="sxs-lookup"><span data-stu-id="c6521-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6521-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="c6521-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="c6521-124">O identificador da sessão de instantâneo não é válido.</span><span class="sxs-lookup"><span data-stu-id="c6521-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6521-125">Se essa função for bem sucedido, a sessão de instantâneo será encerrada e o comportamento normal do mecanismo será retomado.</span><span class="sxs-lookup"><span data-stu-id="c6521-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="c6521-126">Uma nova sessão de instantâneo pode ser iniciada em um ponto posterior.</span><span class="sxs-lookup"><span data-stu-id="c6521-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="c6521-127">Se essa função falhar, a sessão de instantâneo não será anulada.</span><span class="sxs-lookup"><span data-stu-id="c6521-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c6521-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6521-128">Remarks</span></span>

<span data-ttu-id="c6521-129">Essa função deve ser chamada em vez de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para informar ao mecanismo que o instantâneo foi anulado por motivos que não se relacionam com o mecanismo.</span><span class="sxs-lookup"><span data-stu-id="c6521-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="c6521-130">Essas informações podem ser usadas posteriormente para ajudar a emitir mensagens de log de eventos sobre a sessão de instantâneo ou para ajudar a determinar outras ações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c6521-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c6521-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6521-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6521-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c6521-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c6521-133">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6521-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6521-134"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c6521-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c6521-135">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6521-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6521-136"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c6521-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c6521-137">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c6521-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6521-138"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="c6521-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c6521-139">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c6521-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6521-140"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c6521-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c6521-141">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c6521-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c6521-142">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c6521-142">See Also</span></span>

[<span data-ttu-id="c6521-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c6521-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c6521-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="c6521-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="c6521-145">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="c6521-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="c6521-146">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="c6521-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="c6521-147">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="c6521-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
