---
description: 'Saiba mais sobre: função JetStopBackupInstance'
title: Função JetStopBackupInstance
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090112"
---
# <a name="jetstopbackupinstance-function"></a><span data-ttu-id="2bf63-103">Função JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="2bf63-103">JetStopBackupInstance Function</span></span>


<span data-ttu-id="2bf63-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2bf63-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackupinstance-function"></a><span data-ttu-id="2bf63-105">Função JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="2bf63-105">JetStopBackupInstance Function</span></span>

<span data-ttu-id="2bf63-106">A função **JetStopBackupInstance** impede que o streaming da atividade relacionada ao backup continue em uma instância em execução específica, encerrando assim o backup de streaming de forma previsível.</span><span class="sxs-lookup"><span data-stu-id="2bf63-106">The **JetStopBackupInstance** function prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="2bf63-107">**Windows XP:** o **JetStopBackupInstance** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="2bf63-107">**Windows XP:**  **JetStopBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="2bf63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bf63-108">Parameters</span></span>

<span data-ttu-id="2bf63-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="2bf63-109">*instance*</span></span>

<span data-ttu-id="2bf63-110">Identifica a instância em execução a ser usada para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="2bf63-110">Identifies the running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="2bf63-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2bf63-111">Return Value</span></span>

<span data-ttu-id="2bf63-112">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="2bf63-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2bf63-113">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2bf63-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bf63-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2bf63-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="2bf63-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bf63-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bf63-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2bf63-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2bf63-117">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2bf63-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bf63-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2bf63-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2bf63-119">O parâmetro de instância especificado tem um valor inválido (não uma instância que está sendo executada no momento).</span><span class="sxs-lookup"><span data-stu-id="2bf63-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="2bf63-120"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2bf63-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2bf63-121">Se essa função for realizada com êxito, a instância especificada começará a falhar quaisquer novas APIs de backup de streaming.</span><span class="sxs-lookup"><span data-stu-id="2bf63-121">If this function succeeds, the instance that was specified will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="2bf63-122">Se essa função falhar, nenhuma etapa a ser preparada para o término do backup na instância será executada e nenhuma alteração no estado da instância ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="2bf63-122">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2bf63-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bf63-123">Remarks</span></span>

<span data-ttu-id="2bf63-124">O backup é geralmente disparado por um evento fora do mecanismo de processo e usando essa API, o aplicativo ESENT em si fará outras chamadas para que as APIs de backup de streaming falhem.</span><span class="sxs-lookup"><span data-stu-id="2bf63-124">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="2bf63-125">A maioria das APIs de backup de streaming começará a falhar com JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="2bf63-125">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="2bf63-126">Assim, qualquer progresso de backup de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2bf63-126">As such, any streaming backup progress (such as [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="2bf63-127">Operações de backup que fazem parte do encerramento de backup (como [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ainda serão permitidas.</span><span class="sxs-lookup"><span data-stu-id="2bf63-127">Backup operations which are part of the backup termination (like [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2bf63-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf63-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bf63-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2bf63-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2bf63-130">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2bf63-130">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bf63-131"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="2bf63-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2bf63-132">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2bf63-132">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bf63-133"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="2bf63-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2bf63-134">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2bf63-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bf63-135"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="2bf63-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2bf63-136">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2bf63-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bf63-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2bf63-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2bf63-138">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2bf63-138">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2bf63-139">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2bf63-139">See Also</span></span>

[<span data-ttu-id="2bf63-140">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2bf63-140">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2bf63-141">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2bf63-141">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2bf63-142">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="2bf63-142">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="2bf63-143">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="2bf63-143">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="2bf63-144">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2bf63-144">JetStopService</span></span>](./jetstopservice-function.md)
