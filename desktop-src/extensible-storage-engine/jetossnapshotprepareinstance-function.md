---
description: 'Saiba mais sobre: função JetOSSnapshotPrepareInstance'
title: Função JetOSSnapshotPrepareInstance
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104371032"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="a7ffb-103">Função JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="a7ffb-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="a7ffb-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a7ffb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="a7ffb-105">Função JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="a7ffb-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="a7ffb-106">A função **JetOSSnapshotPrepareInstance** seleciona uma instância específica para fazer parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="a7ffb-107">**Windows Vista:** o **JetOSSnapshotPrepareInstance** foi introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="a7ffb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7ffb-108">Parameters</span></span>

<span data-ttu-id="a7ffb-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="a7ffb-109">*snapId*</span></span>

<span data-ttu-id="a7ffb-110">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="a7ffb-111">*cópia*</span><span class="sxs-lookup"><span data-stu-id="a7ffb-111">*instance*</span></span>

<span data-ttu-id="a7ffb-112">A instância que será usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="a7ffb-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a7ffb-113">*grbit*</span></span>

<span data-ttu-id="a7ffb-114">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-114">The options for this call.</span></span> <span data-ttu-id="a7ffb-115">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="a7ffb-116">O único valor válido é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a7ffb-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="a7ffb-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a7ffb-117">Return Value</span></span>

<span data-ttu-id="a7ffb-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a7ffb-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a7ffb-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7ffb-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a7ffb-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="a7ffb-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ffb-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7ffb-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a7ffb-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a7ffb-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ffb-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a7ffb-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a7ffb-125">O ponteiro da ID do instantâneo é <strong>nulo</strong> ou o parâmetro <em>grbit</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ffb-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="a7ffb-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="a7ffb-127">Uma sessão de instantâneo já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ffb-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="a7ffb-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="a7ffb-129">O identificador da sessão de instantâneo não é válido.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7ffb-130">Se essa função for realizada com sucesso, a instância especificada fará parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="a7ffb-131">Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a7ffb-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7ffb-132">Remarks</span></span>

<span data-ttu-id="a7ffb-133">A chamada de sequência de API normal é: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), opcionalmente seguido por uma ou mais chamadas para **JetOSSnapshotPrepareInstance**, seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7ffb-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="a7ffb-134">Quando o congelamento é iniciado, ele pode ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7ffb-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="a7ffb-135">A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada abruptamente com [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7ffb-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="a7ffb-136">As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="a7ffb-137">Se **JetOSSnapshotPrepareInstance** não for chamado entre o início da sessão ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e o tempo de congelamento ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), todas as instâncias em execução no mecanismo serão congeladas e se tornarão parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="a7ffb-138">Isso ocorre por dois motivos:</span><span class="sxs-lookup"><span data-stu-id="a7ffb-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="a7ffb-139">Ele simplifica o código para os usuários que desejam todas as instâncias.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="a7ffb-140">Ele permite compatibilidade com versões anteriores para os chamadores das APIs de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a7ffb-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ffb-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7ffb-142"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a7ffb-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ffb-143">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ffb-144"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a7ffb-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ffb-145">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ffb-146"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a7ffb-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ffb-147">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ffb-148"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a7ffb-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ffb-149">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ffb-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a7ffb-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a7ffb-151">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a7ffb-152">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a7ffb-152">See Also</span></span>

[<span data-ttu-id="a7ffb-153">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="a7ffb-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="a7ffb-154">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="a7ffb-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="a7ffb-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a7ffb-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a7ffb-156">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="a7ffb-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="a7ffb-157">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="a7ffb-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="a7ffb-158">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="a7ffb-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="a7ffb-159">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="a7ffb-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="a7ffb-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="a7ffb-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
