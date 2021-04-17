---
description: 'Saiba mais sobre: função JetBeginExternalBackupInstance'
title: Função JetBeginExternalBackupInstance
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457255"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="7ee45-103">Função JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="7ee45-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="7ee45-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7ee45-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="7ee45-105">Função JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="7ee45-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="7ee45-106">A função **JetBeginExternalBackupInstance** inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.</span><span class="sxs-lookup"><span data-stu-id="7ee45-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="7ee45-107">**Windows XP: o JetBeginExternalBackupInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ee45-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7ee45-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ee45-108">Parameters</span></span>

<span data-ttu-id="7ee45-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="7ee45-109">*instance*</span></span>

<span data-ttu-id="7ee45-110">A instância do banco de dados a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="7ee45-110">The database instance to use for this call.</span></span>

<span data-ttu-id="7ee45-111">Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="7ee45-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="7ee45-112">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="7ee45-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="7ee45-113">Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="7ee45-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="7ee45-114">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="7ee45-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="7ee45-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7ee45-115">*grbit*</span></span>

<span data-ttu-id="7ee45-116">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ee45-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ee45-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7ee45-117">Value</span></span></p></th>
<th><p><span data-ttu-id="7ee45-118">Significado</span><span class="sxs-lookup"><span data-stu-id="7ee45-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ee45-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="7ee45-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="7ee45-120">Esse sinalizador foi preterido.</span><span class="sxs-lookup"><span data-stu-id="7ee45-120">This flag is deprecated.</span></span> <span data-ttu-id="7ee45-121">O uso desse bit resultará na JET_errInvalidgrbit retornando.</span><span class="sxs-lookup"><span data-stu-id="7ee45-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee45-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="7ee45-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="7ee45-123">Cria um backup incremental em oposição a um backup completo.</span><span class="sxs-lookup"><span data-stu-id="7ee45-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="7ee45-124">Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="7ee45-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee45-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="7ee45-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="7ee45-126">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7ee45-126">Reserved for future use.</span></span> <span data-ttu-id="7ee45-127">Definido para o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ee45-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7ee45-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7ee45-128">Return Value</span></span>

<span data-ttu-id="7ee45-129">O sistema pode gerar códigos de êxito ou de falha como resultado de uma chamada para essa função.</span><span class="sxs-lookup"><span data-stu-id="7ee45-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="7ee45-130">Para obter uma lista completa de erros para essa API, consulte [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7ee45-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="7ee45-131">Consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee45-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="7ee45-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ee45-132">Remarks</span></span>

<span data-ttu-id="7ee45-133">**JetBeginExternalBackupInstance** é a primeira função em uma série de funções que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="7ee45-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="7ee45-134">Consulte também [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) e [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee45-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="7ee45-135">Um backup externo pode ser usado para implementar backups completos, incrementais ou diferenciais.</span><span class="sxs-lookup"><span data-stu-id="7ee45-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="7ee45-136">O backup será difuso, pois o backup será consistente para um único ponto no histórico de transações, mas controlar o ponto exato no tempo não é possível no momento.</span><span class="sxs-lookup"><span data-stu-id="7ee45-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7ee45-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ee45-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ee45-138"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7ee45-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee45-139">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7ee45-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee45-140"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="7ee45-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee45-141">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7ee45-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee45-142"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="7ee45-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee45-143">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7ee45-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee45-144"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="7ee45-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee45-145">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7ee45-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee45-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7ee45-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee45-147">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7ee45-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7ee45-148">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7ee45-148">See Also</span></span>

[<span data-ttu-id="7ee45-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7ee45-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7ee45-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7ee45-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7ee45-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7ee45-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7ee45-152">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="7ee45-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="7ee45-153">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="7ee45-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="7ee45-154">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="7ee45-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="7ee45-155">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="7ee45-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="7ee45-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="7ee45-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="7ee45-157">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="7ee45-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="7ee45-158">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="7ee45-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="7ee45-159">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="7ee45-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="7ee45-160">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="7ee45-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="7ee45-161">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="7ee45-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="7ee45-162">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="7ee45-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)
