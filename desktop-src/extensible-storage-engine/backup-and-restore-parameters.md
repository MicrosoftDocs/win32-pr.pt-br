---
description: 'Saiba mais sobre: parâmetros de backup e restauração'
title: Parâmetros de backup e restauração
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506215"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="fe635-103">Parâmetros de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="fe635-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="fe635-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fe635-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="fe635-105">Parâmetros de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="fe635-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="fe635-106">Este tópico contém parâmetros que são usados para backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="fe635-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="fe635-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="fe635-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="fe635-108">113</span><span class="sxs-lookup"><span data-stu-id="fe635-108">113</span></span>  

<span data-ttu-id="fe635-109">O caminho completo para cada banco de dados é mantido nos logs de transação em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fe635-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="fe635-110">Normalmente, esses bancos de dados devem permanecer no local original para que a execução da transação funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="fe635-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="fe635-111">Esse parâmetro pode ser usado para forçar a recuperação de pane ou uma operação de restauração para procurar os bancos de dados referenciados no log de transações na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="fe635-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe635-112">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="fe635-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="fe635-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="fe635-114">Caminho da pasta (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="fe635-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="fe635-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fe635-116">0 a 246 caracteres</span><span class="sxs-lookup"><span data-stu-id="fe635-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-117">Escopo:</span><span class="sxs-lookup"><span data-stu-id="fe635-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fe635-118">Instância</span><span class="sxs-lookup"><span data-stu-id="fe635-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-119">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-120">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-121">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-122">No</span><span class="sxs-lookup"><span data-stu-id="fe635-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-123">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="fe635-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fe635-124">No</span><span class="sxs-lookup"><span data-stu-id="fe635-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-125">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-126">No</span><span class="sxs-lookup"><span data-stu-id="fe635-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-127">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="fe635-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fe635-128">No</span><span class="sxs-lookup"><span data-stu-id="fe635-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-129">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="fe635-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fe635-130">No</span><span class="sxs-lookup"><span data-stu-id="fe635-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-131">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-132">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="fe635-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe635-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="fe635-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="fe635-134">77</span><span class="sxs-lookup"><span data-stu-id="fe635-134">77</span></span>  

<span data-ttu-id="fe635-135">Esse parâmetro controla o resultado de [JetInit](./jetinit-function.md) quando o mecanismo de banco de dados é configurado para começar a usar arquivos de log de transações em um disco que tenha um tamanho diferente do que está configurado.</span><span class="sxs-lookup"><span data-stu-id="fe635-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="fe635-136">Normalmente, o [JetInit](./jetinit-function.md) recuperará com êxito os bancos de dados, mas irá falhar com JET_errLogFileSizeMismatchDatabasesConsistent para indicar que o tamanho do arquivo de log está configurado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="fe635-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="fe635-137">No entanto, quando esse parâmetro for definido como true, o mecanismo de banco de dados excluirá silenciosamente todos os arquivos de log antigos, iniciará um novo conjunto de arquivos de log de transações usando o tamanho do arquivo de log configurado e retornará JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="fe635-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="fe635-138">Esse parâmetro é útil quando o aplicativo deseja alterar de forma transparente o tamanho do arquivo de log de transações e ainda funcionar de forma transparente nos cenários de atualização e restauração.</span><span class="sxs-lookup"><span data-stu-id="fe635-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe635-139">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="fe635-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fe635-140">Falso</span><span class="sxs-lookup"><span data-stu-id="fe635-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-141">Tipo:</span><span class="sxs-lookup"><span data-stu-id="fe635-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="fe635-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe635-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-143">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="fe635-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fe635-144">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="fe635-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-145">Escopo:</span><span class="sxs-lookup"><span data-stu-id="fe635-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fe635-146">Instância</span><span class="sxs-lookup"><span data-stu-id="fe635-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-147">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-148">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-149">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-150">No</span><span class="sxs-lookup"><span data-stu-id="fe635-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-151">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="fe635-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fe635-152">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-153">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-154">No</span><span class="sxs-lookup"><span data-stu-id="fe635-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-155">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="fe635-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fe635-156">No</span><span class="sxs-lookup"><span data-stu-id="fe635-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-157">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="fe635-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fe635-158">No</span><span class="sxs-lookup"><span data-stu-id="fe635-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-159">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-160">Tudo</span><span class="sxs-lookup"><span data-stu-id="fe635-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe635-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="fe635-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="fe635-162">52</span><span class="sxs-lookup"><span data-stu-id="fe635-162">52</span></span>  

<span data-ttu-id="fe635-163">Quando esse parâmetro for true, todos os arquivos de log de transações encontrados no disco que não fazem parte da sequência atual de arquivos de log serão excluídos pelo [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="fe635-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="fe635-164">Isso pode ser usado para limpar automaticamente arquivos de log incorretos após uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="fe635-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="fe635-165">**Windows XP:**  Introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe635-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe635-166">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="fe635-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fe635-167">Falso</span><span class="sxs-lookup"><span data-stu-id="fe635-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-168">Tipo:</span><span class="sxs-lookup"><span data-stu-id="fe635-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="fe635-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe635-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-170">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="fe635-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fe635-171">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="fe635-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-172">Escopo:</span><span class="sxs-lookup"><span data-stu-id="fe635-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fe635-173">Instância</span><span class="sxs-lookup"><span data-stu-id="fe635-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-174">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-175">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-176">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-177">No</span><span class="sxs-lookup"><span data-stu-id="fe635-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-178">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="fe635-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fe635-179">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-180">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-181">No</span><span class="sxs-lookup"><span data-stu-id="fe635-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-182">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="fe635-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fe635-183">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-184">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="fe635-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fe635-185">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-186">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-187">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="fe635-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe635-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="fe635-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="fe635-189">82</span><span class="sxs-lookup"><span data-stu-id="fe635-189">82</span></span>  

<span data-ttu-id="fe635-190">Esse parâmetro configura a quantidade de tempo permitida entre uma chamada para [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) antes de ocorrer um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="fe635-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="fe635-191">Consulte [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="fe635-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="fe635-192">O tempo limite é em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="fe635-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe635-193">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="fe635-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fe635-194">20000 (Windows XP e Windows Server 2003);</span><span class="sxs-lookup"><span data-stu-id="fe635-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="fe635-195">70000 (Windows Server 2003 SP1)</span><span class="sxs-lookup"><span data-stu-id="fe635-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-196">Tipo:</span><span class="sxs-lookup"><span data-stu-id="fe635-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="fe635-197">Integer</span><span class="sxs-lookup"><span data-stu-id="fe635-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-198">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="fe635-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fe635-199">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="fe635-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-200">Escopo:</span><span class="sxs-lookup"><span data-stu-id="fe635-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fe635-201">Global</span><span class="sxs-lookup"><span data-stu-id="fe635-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-202">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-203">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-204">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-205">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-206">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="fe635-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fe635-207">No</span><span class="sxs-lookup"><span data-stu-id="fe635-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-208">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-209">No</span><span class="sxs-lookup"><span data-stu-id="fe635-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-210">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="fe635-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fe635-211">No</span><span class="sxs-lookup"><span data-stu-id="fe635-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-212">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="fe635-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fe635-213">No</span><span class="sxs-lookup"><span data-stu-id="fe635-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-214">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-215">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="fe635-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe635-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="fe635-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="fe635-217">71</span><span class="sxs-lookup"><span data-stu-id="fe635-217">71</span></span>  

<span data-ttu-id="fe635-218">Quando esse parâmetro for true, cada página em um banco de dados que está passando por um backup de streaming será depurada dos dados excluídos.</span><span class="sxs-lookup"><span data-stu-id="fe635-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="fe635-219">É importante observar que as páginas de banco de dados que estão sendo depuradas estão no disco.</span><span class="sxs-lookup"><span data-stu-id="fe635-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="fe635-220">O backup do conjunto de dados completo é feito antes do processo de depuração.</span><span class="sxs-lookup"><span data-stu-id="fe635-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe635-221">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="fe635-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fe635-222">Falso</span><span class="sxs-lookup"><span data-stu-id="fe635-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-223">Tipo:</span><span class="sxs-lookup"><span data-stu-id="fe635-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="fe635-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe635-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-225">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="fe635-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fe635-226">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="fe635-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-227">Escopo:</span><span class="sxs-lookup"><span data-stu-id="fe635-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fe635-228">Instância</span><span class="sxs-lookup"><span data-stu-id="fe635-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-229">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-230">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-231">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fe635-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fe635-232">No</span><span class="sxs-lookup"><span data-stu-id="fe635-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-233">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="fe635-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fe635-234">No</span><span class="sxs-lookup"><span data-stu-id="fe635-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-235">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-236">No</span><span class="sxs-lookup"><span data-stu-id="fe635-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-237">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="fe635-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fe635-238">Yes</span><span class="sxs-lookup"><span data-stu-id="fe635-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-239">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="fe635-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fe635-240">No</span><span class="sxs-lookup"><span data-stu-id="fe635-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-241">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="fe635-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fe635-242">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="fe635-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="fe635-243">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe635-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe635-244"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fe635-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fe635-245">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fe635-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe635-246"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="fe635-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fe635-247">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fe635-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe635-248"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="fe635-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fe635-249">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fe635-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fe635-250">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fe635-250">See Also</span></span>

[<span data-ttu-id="fe635-251">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="fe635-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="fe635-252">JetInit</span><span class="sxs-lookup"><span data-stu-id="fe635-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="fe635-253">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="fe635-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="fe635-254">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="fe635-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
