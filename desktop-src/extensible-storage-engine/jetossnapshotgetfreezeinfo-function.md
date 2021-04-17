---
description: 'Saiba mais sobre: função JetOSSnapshotGetFreezeInfo'
title: Função JetOSSnapshotGetFreezeInfo
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812221"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="35d72-103">Função JetOSSnapshotGetFreezeInfo</span><span class="sxs-lookup"><span data-stu-id="35d72-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="35d72-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="35d72-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="35d72-105">Função JetOSSnapshotGetFreezeInfo</span><span class="sxs-lookup"><span data-stu-id="35d72-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="35d72-106">A função **JetOSSnapshotGetFreezeInfo** recupera a lista de instâncias e bancos de dados que fazem parte da sessão de instantâneo em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="35d72-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="35d72-107">**Windows Vista:** o **JetOSSnapshotGetFreezeInfo** é introduzido no Windows Vista.  </span><span class="sxs-lookup"><span data-stu-id="35d72-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="35d72-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35d72-108">Parameters</span></span>

<span data-ttu-id="35d72-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="35d72-109">*snapId*</span></span>

<span data-ttu-id="35d72-110">O identificador da sessão de instantâneo a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="35d72-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="35d72-111">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="35d72-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="35d72-112">O número de instâncias em execução no momento que fazem parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="35d72-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="35d72-113">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="35d72-113">*paInstanceInfo*</span></span>

<span data-ttu-id="35d72-114">Uma matriz de estruturas, uma para cada instância em execução, descrevendo a instância e os bancos de dados que fazem parte dela.</span><span class="sxs-lookup"><span data-stu-id="35d72-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="35d72-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="35d72-115">*grbit*</span></span>

<span data-ttu-id="35d72-116">As opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="35d72-116">The options for this call.</span></span> <span data-ttu-id="35d72-117">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="35d72-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="35d72-118">O único valor válido é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="35d72-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="35d72-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="35d72-119">Return Value</span></span>

<span data-ttu-id="35d72-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="35d72-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="35d72-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35d72-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35d72-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="35d72-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="35d72-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="35d72-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d72-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="35d72-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="35d72-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="35d72-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d72-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="35d72-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="35d72-127">A função falhou devido a uma condição de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="35d72-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d72-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="35d72-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="35d72-129"><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="35d72-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d72-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="35d72-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="35d72-131">O identificador da sessão de instantâneo não é válido.</span><span class="sxs-lookup"><span data-stu-id="35d72-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d72-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="35d72-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="35d72-133">Uma sessão de instantâneo não está em andamento.</span><span class="sxs-lookup"><span data-stu-id="35d72-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35d72-134">Se essa função for bem sucedido, as informações da instância serão preenchidas corretamente e deverão ser liberadas mais tarde chamando [JetFreeBuffer](./jetfreebuffer-function.md) com o ponteiro para a matriz de informações da instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="35d72-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="35d72-135">Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="35d72-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="35d72-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d72-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d72-137"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="35d72-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35d72-138">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35d72-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d72-139"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="35d72-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35d72-140">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="35d72-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d72-141"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="35d72-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35d72-142">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="35d72-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d72-143"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="35d72-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="35d72-144">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="35d72-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d72-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="35d72-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="35d72-146">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="35d72-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d72-147"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="35d72-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="35d72-148">Implementado como <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) e <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="35d72-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="35d72-149">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="35d72-149">See Also</span></span>

[<span data-ttu-id="35d72-150">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="35d72-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="35d72-151">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="35d72-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="35d72-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35d72-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="35d72-153">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="35d72-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="35d72-154">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="35d72-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="35d72-155">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="35d72-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="35d72-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="35d72-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
