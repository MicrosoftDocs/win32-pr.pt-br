---
description: 'Saiba mais sobre: parâmetros do log de transações'
title: Parâmetros de Log de Transação
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781518"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="101cd-103">Parâmetros de Log de Transação</span><span class="sxs-lookup"><span data-stu-id="101cd-103">Transaction Log Parameters</span></span>


<span data-ttu-id="101cd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="101cd-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="101cd-105">**Neste artigo**</span><span class="sxs-lookup"><span data-stu-id="101cd-105">**In this article**</span></span>  
<span data-ttu-id="101cd-106">Parâmetros de Log de Transação</span><span class="sxs-lookup"><span data-stu-id="101cd-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="101cd-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="101cd-107">Requirements</span></span>  
<span data-ttu-id="101cd-108">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="101cd-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="101cd-109">Parâmetros de Log de Transação</span><span class="sxs-lookup"><span data-stu-id="101cd-109">Transaction Log Parameters</span></span>

<span data-ttu-id="101cd-110">Este tópico contém parâmetros que são usados para logs de transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="101cd-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="101cd-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="101cd-112">3</span><span class="sxs-lookup"><span data-stu-id="101cd-112">3</span></span>  

<span data-ttu-id="101cd-113">Esse parâmetro define o prefixo de três letras usado para muitos dos arquivos usados pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="101cd-114">Por exemplo, o arquivo de ponto de verificação é chamado de EDB. CHK por padrão, porque o EDB é o nome de base padrão.</span><span class="sxs-lookup"><span data-stu-id="101cd-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="101cd-115">O nome base pode ser usado para distinguir facilmente entre conjuntos de arquivos que pertencem a diferentes instâncias ou a aplicativos diferentes.</span><span class="sxs-lookup"><span data-stu-id="101cd-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-116">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-117">&quot;EDB&quot;</span><span class="sxs-lookup"><span data-stu-id="101cd-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-118">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-119">String</span><span class="sxs-lookup"><span data-stu-id="101cd-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-120">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-121">3 caracteres</span><span class="sxs-lookup"><span data-stu-id="101cd-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-122">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-123">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-124">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-125">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-126">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-127">No</span><span class="sxs-lookup"><span data-stu-id="101cd-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-128">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-129">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-130">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-131">No</span><span class="sxs-lookup"><span data-stu-id="101cd-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-132">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-133">No</span><span class="sxs-lookup"><span data-stu-id="101cd-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-134">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-135">No</span><span class="sxs-lookup"><span data-stu-id="101cd-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-136">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-137">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="101cd-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="101cd-139">17</span><span class="sxs-lookup"><span data-stu-id="101cd-139">17</span></span>  

<span data-ttu-id="101cd-140">Esse parâmetro configura como os arquivos de log de transações são gerenciados pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="101cd-141">Quando o log circular está desativado, todos os arquivos de log de transações gerados são mantidos no disco até que não sejam mais necessários porque um backup completo do banco de dados foi executado.</span><span class="sxs-lookup"><span data-stu-id="101cd-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="101cd-142">Nesse modo, é possível restaurar de um backup mais antigo e reproduzir todos os arquivos de log de transações retidos, de modo que nenhum dado seja perdido como resultado do desastre que forçou a restauração.</span><span class="sxs-lookup"><span data-stu-id="101cd-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="101cd-143">Backups completos regulares são necessários para impedir que o disco fique cheio de arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="101cd-144">Quando o log circular está ativado, somente os arquivos de log de transações mais jovens do que o ponto de verificação atual são mantidos no disco.</span><span class="sxs-lookup"><span data-stu-id="101cd-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="101cd-145">O benefício desse modo é que os backups não são necessários para desativar arquivos de log de transação antigos.</span><span class="sxs-lookup"><span data-stu-id="101cd-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="101cd-146">A desvantagem é que uma restauração sem perda de dados não é mais possível.</span><span class="sxs-lookup"><span data-stu-id="101cd-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-147">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-148">Falso</span><span class="sxs-lookup"><span data-stu-id="101cd-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-149">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="101cd-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-151">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-152">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="101cd-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-153">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-154">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-155">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-156">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-157">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-158">No</span><span class="sxs-lookup"><span data-stu-id="101cd-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-159">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-160">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-161">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-162">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-163">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-164">No</span><span class="sxs-lookup"><span data-stu-id="101cd-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-165">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-166">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-167">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-168">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="101cd-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="101cd-170">16</span><span class="sxs-lookup"><span data-stu-id="101cd-170">16</span></span>  

<span data-ttu-id="101cd-171">Esse parâmetro controla a ação padrão tomada quando a transação mais externa é confirmada em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="101cd-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="101cd-172">Qualquer opção válida que possa ser passada para [JetCommitTransaction](./jetcommittransaction-function.md) também pode ser feita como o padrão para todas as sessões em uma instância e/ou para uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="101cd-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="101cd-173">Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obter mais detalhes sobre essas opções.</span><span class="sxs-lookup"><span data-stu-id="101cd-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="101cd-174">Esse parâmetro tem um impacto na confiabilidade e no desempenho das transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="101cd-175">Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="101cd-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-176">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-177">0</span><span class="sxs-lookup"><span data-stu-id="101cd-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-178">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-179">JET_GRBIT (inteiro)</span><span class="sxs-lookup"><span data-stu-id="101cd-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-180">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-181">Uma opção válida para JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="101cd-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-182">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-183">Instância ou sessão</span><span class="sxs-lookup"><span data-stu-id="101cd-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-184">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-185">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-186">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-187">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-188">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-189">No</span><span class="sxs-lookup"><span data-stu-id="101cd-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-190">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-191">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-192">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-193">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-194">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-195">No</span><span class="sxs-lookup"><span data-stu-id="101cd-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-196">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-197">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="101cd-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="101cd-199">48</span><span class="sxs-lookup"><span data-stu-id="101cd-199">48</span></span>  

<span data-ttu-id="101cd-200">Quando esse parâmetro for true e os arquivos de log de transações apontados pelo caminho do arquivo de log (**JET_paramLogFilePath**) forem de uma versão obsoleta, esses arquivos de log de transações serão excluídos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="101cd-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="101cd-201">**Windows 2000:**  Deve-se ter cuidado com o uso desse parâmetro ao atualizar um banco de dados do Windows NT para o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="101cd-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="101cd-202">Se o banco de dados não estiver em um estado consistente e os arquivos de log antigos forem excluídos, o conteúdo do banco de dados será perdido.</span><span class="sxs-lookup"><span data-stu-id="101cd-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-203">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-204"><strong>Windows 2000:</strong>  For</span><span class="sxs-lookup"><span data-stu-id="101cd-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="101cd-205"><strong>Windows XP:</strong>  True</span><span class="sxs-lookup"><span data-stu-id="101cd-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-206">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="101cd-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-208">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-209">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="101cd-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-210">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-211">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-212">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-213">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-214">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-215">No</span><span class="sxs-lookup"><span data-stu-id="101cd-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-216">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-217">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-218">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-219">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-220">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-221">No</span><span class="sxs-lookup"><span data-stu-id="101cd-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-222">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-223">No</span><span class="sxs-lookup"><span data-stu-id="101cd-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-224">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-225">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="101cd-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="101cd-227">47</span><span class="sxs-lookup"><span data-stu-id="101cd-227">47</span></span>  

<span data-ttu-id="101cd-228">Se esse parâmetro for true, o mecanismo de banco de dados não validará o número de versão do arquivo de log de transações durante [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="101cd-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="101cd-229">**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-230">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-231">Falso</span><span class="sxs-lookup"><span data-stu-id="101cd-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-232">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="101cd-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-234">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-235">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="101cd-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-236">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-237">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-238">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-239">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-240">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-241">No</span><span class="sxs-lookup"><span data-stu-id="101cd-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-242">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-243">No</span><span class="sxs-lookup"><span data-stu-id="101cd-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-244">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-245">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-246">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-247">No</span><span class="sxs-lookup"><span data-stu-id="101cd-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-248">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-249">No</span><span class="sxs-lookup"><span data-stu-id="101cd-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-250">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-251">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="101cd-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="101cd-253">136</span><span class="sxs-lookup"><span data-stu-id="101cd-253">136</span></span>  

<span data-ttu-id="101cd-254">Esse parâmetro fornece compatibilidade com versões anteriores do mecanismo de banco de dados para as convenções de nomenclatura do arquivo.</span><span class="sxs-lookup"><span data-stu-id="101cd-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="101cd-255">Atualmente, há suporte para as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="101cd-255">The following options are currently supported:</span></span>

<span data-ttu-id="101cd-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="101cd-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="101cd-257">Quando essa opção estiver presente, o mecanismo de banco de dados usará as seguintes convenções de nomenclatura para seus arquivos:</span><span class="sxs-lookup"><span data-stu-id="101cd-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="101cd-258">Os arquivos de log de transações usarão. LOG para sua extensão de arquivo</span><span class="sxs-lookup"><span data-stu-id="101cd-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="101cd-259">Os arquivos de ponto de verificação usarão. CHK para sua extensão de arquivo</span><span class="sxs-lookup"><span data-stu-id="101cd-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-260">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="101cd-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-262">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-263">JET_GRBIT (inteiro)</span><span class="sxs-lookup"><span data-stu-id="101cd-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-264">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-265">0, JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="101cd-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-266">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-267">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-268">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-269">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-270">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-271">No</span><span class="sxs-lookup"><span data-stu-id="101cd-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-272">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-273">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-274">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-275">No</span><span class="sxs-lookup"><span data-stu-id="101cd-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-276">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-277">No</span><span class="sxs-lookup"><span data-stu-id="101cd-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-278">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-279">No</span><span class="sxs-lookup"><span data-stu-id="101cd-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-280">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-281">Windows Vista e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="101cd-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="101cd-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="101cd-283">12</span><span class="sxs-lookup"><span data-stu-id="101cd-283">12</span></span>  

<span data-ttu-id="101cd-284">Esse parâmetro irá configurar a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="101cd-285">A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="101cd-286">O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade.</span><span class="sxs-lookup"><span data-stu-id="101cd-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="101cd-287">Esse parâmetro tem um impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="101cd-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="101cd-288">Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez.</span><span class="sxs-lookup"><span data-stu-id="101cd-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="101cd-289">Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga.</span><span class="sxs-lookup"><span data-stu-id="101cd-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="101cd-290">O padrão é conhecido como muito pequeno para esse caso.</span><span class="sxs-lookup"><span data-stu-id="101cd-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="101cd-291">**Windows XP e windows 2000:**  No Windows XP e versões anteriores, não é recomendável definir esse parâmetro como um número de buffers maior (em bytes) que metade do tamanho de um arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-292">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-293"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80</span><span class="sxs-lookup"><span data-stu-id="101cd-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="101cd-294"><strong>Windows Vista:</strong>  126</span><span class="sxs-lookup"><span data-stu-id="101cd-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-295">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-296">Integer</span><span class="sxs-lookup"><span data-stu-id="101cd-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-297">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-298"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="101cd-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="101cd-299"><strong>Windows Vista:</strong>  1 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="101cd-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-300">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-301">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-302">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-303">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-304">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-305">No</span><span class="sxs-lookup"><span data-stu-id="101cd-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-306">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-307">No</span><span class="sxs-lookup"><span data-stu-id="101cd-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-308">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-309">No</span><span class="sxs-lookup"><span data-stu-id="101cd-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-310">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-311">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-312">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-313">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-314">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-315">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="101cd-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="101cd-317">14</span><span class="sxs-lookup"><span data-stu-id="101cd-317">14</span></span>  

<span data-ttu-id="101cd-318">Esse parâmetro configura o mecanismo de banco de dados para pegar um ponto de verificação quando o número especificado de setores do arquivo de log tiver sido gerado.</span><span class="sxs-lookup"><span data-stu-id="101cd-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="101cd-319">**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-320">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-321">1024</span><span class="sxs-lookup"><span data-stu-id="101cd-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-322">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-323">Integer</span><span class="sxs-lookup"><span data-stu-id="101cd-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-324">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-325">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="101cd-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-326">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-327">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-328">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-329">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-330">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-331">No</span><span class="sxs-lookup"><span data-stu-id="101cd-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-332">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-333">No</span><span class="sxs-lookup"><span data-stu-id="101cd-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-334">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-335">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-336">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-337">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-338">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-339">No</span><span class="sxs-lookup"><span data-stu-id="101cd-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-340">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-341">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="101cd-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="101cd-343">69</span><span class="sxs-lookup"><span data-stu-id="101cd-343">69</span></span>  

<span data-ttu-id="101cd-344">Quando esse parâmetro for definido como true, o mecanismo de banco de dados criará o próximo arquivo de log de transações, pois o arquivo de log de transações atual será consumido.</span><span class="sxs-lookup"><span data-stu-id="101cd-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="101cd-345">A intenção é minimizar o tempo gasto alternando de um arquivo de log de transações para o próximo em uma carga de atualização pesada.</span><span class="sxs-lookup"><span data-stu-id="101cd-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-346">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-347">True</span><span class="sxs-lookup"><span data-stu-id="101cd-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-348">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-349">Boolean</span><span class="sxs-lookup"><span data-stu-id="101cd-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-350">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-351">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="101cd-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-352">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-353">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-354">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-355">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-356">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-357">No</span><span class="sxs-lookup"><span data-stu-id="101cd-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-358">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-359">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-360">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-361">No</span><span class="sxs-lookup"><span data-stu-id="101cd-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-362">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-363">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-364">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-365">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-366">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-367">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="101cd-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="101cd-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="101cd-369">2</span><span class="sxs-lookup"><span data-stu-id="101cd-369">2</span></span> 

<span data-ttu-id="101cd-370">Esse parâmetro indica o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá os logs de transação para a instância.</span><span class="sxs-lookup"><span data-stu-id="101cd-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="101cd-371">O caminho deve ser terminado com um caractere de barra invertida, que indica que o caminho de destino é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="101cd-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="101cd-372">Os arquivos de log de transações contêm as informações necessárias para colocar os arquivos de banco de dados em um estado consistente após uma falha.</span><span class="sxs-lookup"><span data-stu-id="101cd-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="101cd-373">Normalmente, eles são chamados de EDB \* . Façam.</span><span class="sxs-lookup"><span data-stu-id="101cd-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="101cd-374">O conteúdo dos arquivos de log de transações é tão importante (se não mais) do que os próprios arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="101cd-375">Todo esforço deve ser feito para protegê-los.</span><span class="sxs-lookup"><span data-stu-id="101cd-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="101cd-376">Também haverá arquivos de log de reserva adicionais chamados RES1. LOG e RES2. LOG armazenado junto com os arquivos de log comuns.</span><span class="sxs-lookup"><span data-stu-id="101cd-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="101cd-377">O conteúdo desses arquivos não é importante, pois sua única finalidade é reservar espaço em disco para permitir que o mecanismo seja desligado normalmente em um cenário de disco baixo.</span><span class="sxs-lookup"><span data-stu-id="101cd-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="101cd-378">Eles também serão um arquivo de log temporário normalmente chamado de EDBTMP. Faça logon nessa mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="101cd-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="101cd-379">O conteúdo desse arquivo também não é importante.</span><span class="sxs-lookup"><span data-stu-id="101cd-379">The contents of this file are not important either.</span></span> <span data-ttu-id="101cd-380">Este arquivo é um novo arquivo de log que está sendo preparado para uso.</span><span class="sxs-lookup"><span data-stu-id="101cd-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="101cd-381">As propriedades do volume do host dos arquivos de log de transações e seu posicionamento em relação aos outros arquivos usados pelo mecanismo de banco de dados podem afetar drasticamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="101cd-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="101cd-382">**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-383">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-384">&quot;.\& vincular</span><span class="sxs-lookup"><span data-stu-id="101cd-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-385">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-386">Caminho da pasta (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="101cd-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-387">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-388">0 a 246 caracteres</span><span class="sxs-lookup"><span data-stu-id="101cd-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-389">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-390">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-391">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-392">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-393">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-394">No</span><span class="sxs-lookup"><span data-stu-id="101cd-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-395">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-396">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-397">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-398">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-399">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-400">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-401">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-402">No</span><span class="sxs-lookup"><span data-stu-id="101cd-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-403">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-404">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="101cd-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="101cd-406">11</span><span class="sxs-lookup"><span data-stu-id="101cd-406">11</span></span>  

<span data-ttu-id="101cd-407">Esse parâmetro irá configurar o tamanho dos arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="101cd-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="101cd-408">Cada arquivo de log de transações é um tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="101cd-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="101cd-409">O tamanho é igual à configuração desse parâmetro de sistema em unidades de 1024 bytes.</span><span class="sxs-lookup"><span data-stu-id="101cd-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="101cd-410">Esse parâmetro tem um impacto na confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="101cd-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="101cd-411">Se a configuração for muito pequena, o número máximo de arquivos de log (1048575) será alcançado muito mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="101cd-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="101cd-412">Quando isso acontece, a instância deve ser desligada corretamente, os arquivos de log existentes devem ser excluídos e a instância deve ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="101cd-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="101cd-413">Essa ação não apenas reduzirá a disponibilidade do aplicativo, mas também invalidará quaisquer backups anteriores do banco de dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="101cd-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="101cd-414">Esse parâmetro tem um impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="101cd-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="101cd-415">Se a configuração for muito grande, o [JetInit](./jetinit-function.md) será lento, pois o mecanismo de banco de dados deve ler o arquivo de log mais recente (no mínimo) quando ele for inicializado.</span><span class="sxs-lookup"><span data-stu-id="101cd-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="101cd-416">Se a configuração for muito grande, ela também levará mais tempo para alternar entre os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="101cd-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="101cd-417">Se a configuração for muito pequena, mais arquivos de log precisarão ser criados para um determinado número de atualizações que adicionarão mais sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="101cd-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-418">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-419">5120</span><span class="sxs-lookup"><span data-stu-id="101cd-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-420">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-421">Integer</span><span class="sxs-lookup"><span data-stu-id="101cd-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-422">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-423"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  128 – 32768</span><span class="sxs-lookup"><span data-stu-id="101cd-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="101cd-424"><strong>Windows Vista:</strong>  64 – 32768</span><span class="sxs-lookup"><span data-stu-id="101cd-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-425">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-426">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-427">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-428">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-429">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-430">No</span><span class="sxs-lookup"><span data-stu-id="101cd-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-431">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-432">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-433">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-434">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-435">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-436">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-437">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-438">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-439">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-440">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="101cd-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="101cd-442">15</span><span class="sxs-lookup"><span data-stu-id="101cd-442">15</span></span>  

<span data-ttu-id="101cd-443">Esse parâmetro tenta otimizar a liberação do buffer de log causado por uma confirmação durável aguardando que um número especificado de sessões aguarde uma confirmação durável antes de forçar uma liberação a ocorrer na esperança de que outra transação compartilhará a liberação.</span><span class="sxs-lookup"><span data-stu-id="101cd-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="101cd-444">**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-445">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-446">3</span><span class="sxs-lookup"><span data-stu-id="101cd-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-447">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-448">Integer</span><span class="sxs-lookup"><span data-stu-id="101cd-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-449">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-450">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="101cd-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-451">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-452">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-453">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-454">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-455">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-456">No</span><span class="sxs-lookup"><span data-stu-id="101cd-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-457">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-458">No</span><span class="sxs-lookup"><span data-stu-id="101cd-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-459">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-460">No</span><span class="sxs-lookup"><span data-stu-id="101cd-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-461">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-462">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-463">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-464">No</span><span class="sxs-lookup"><span data-stu-id="101cd-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-465">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-466">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="101cd-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="101cd-468">34</span><span class="sxs-lookup"><span data-stu-id="101cd-468">34</span></span>  

<span data-ttu-id="101cd-469">Esse parâmetro é a opção mestra que controla a recuperação de falha de uma instância.</span><span class="sxs-lookup"><span data-stu-id="101cd-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="101cd-470">Se esse parâmetro for definido como "on", a recuperação de estilo ARIES será usada para colocar todos os bancos de dados na instância em um estado consistente no caso de uma falha de processo ou máquina.</span><span class="sxs-lookup"><span data-stu-id="101cd-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="101cd-471">Se esse parâmetro for definido como "off", todos os bancos de dados na instância serão gerenciados sem o benefício da recuperação de falhas.</span><span class="sxs-lookup"><span data-stu-id="101cd-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="101cd-472">Isso significa que, se a instância não for desligada corretamente usando [JetTerm](./jetterm-function.md) antes da saída do processo ou do desligamento do computador, o conteúdo de todos os bancos de dados nessa instância será corrompido.</span><span class="sxs-lookup"><span data-stu-id="101cd-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="101cd-473">A desabilitação da recuperação é útil em circunstâncias especiais, em que é conhecido que o conteúdo de um banco de dados não seja útil no caso de uma falha.</span><span class="sxs-lookup"><span data-stu-id="101cd-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="101cd-474">A recuperação deve ser habilitada para todos os outros casos.</span><span class="sxs-lookup"><span data-stu-id="101cd-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-475">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-476">&quot;Em&quot;</span><span class="sxs-lookup"><span data-stu-id="101cd-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-477">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-478">String</span><span class="sxs-lookup"><span data-stu-id="101cd-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-479">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-480">0 a 259 caracteres</span><span class="sxs-lookup"><span data-stu-id="101cd-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-481">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-482">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-483">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-484">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-485">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-486">No</span><span class="sxs-lookup"><span data-stu-id="101cd-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-487">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-488">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-489">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-490">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-491">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-492">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-493">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-494">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-495">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-496">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="101cd-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="101cd-498">0</span><span class="sxs-lookup"><span data-stu-id="101cd-498">0</span></span>  

<span data-ttu-id="101cd-499">Esse parâmetro indica o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá o arquivo de ponto de verificação para a instância.</span><span class="sxs-lookup"><span data-stu-id="101cd-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="101cd-500">O caminho deve ser terminado com um caractere de barra invertida, que indica que o caminho de destino é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="101cd-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="101cd-501">O arquivo de ponto de verificação é um arquivo simples mantido por instância que lembra o arquivo de log de transações mais antigo que deve ser reproduzido para colocar todos os bancos de dados nessa instância em um estado consistente após uma falha.</span><span class="sxs-lookup"><span data-stu-id="101cd-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="101cd-502">O arquivo de ponto de verificação normalmente é chamado de EDB. CHK.</span><span class="sxs-lookup"><span data-stu-id="101cd-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="101cd-503">**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-504">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-505">&quot;.\& vincular</span><span class="sxs-lookup"><span data-stu-id="101cd-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-506">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-507">Caminho da pasta (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="101cd-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-508">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-509">0 a 246 caracteres</span><span class="sxs-lookup"><span data-stu-id="101cd-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-510">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-511">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-512">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-513">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-514">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-515">No</span><span class="sxs-lookup"><span data-stu-id="101cd-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-516">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-517">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-518">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-519">No</span><span class="sxs-lookup"><span data-stu-id="101cd-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-520">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-521">No</span><span class="sxs-lookup"><span data-stu-id="101cd-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-522">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-523">No</span><span class="sxs-lookup"><span data-stu-id="101cd-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-524">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-525">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="101cd-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="101cd-527">13</span><span class="sxs-lookup"><span data-stu-id="101cd-527">13</span></span> 

<span data-ttu-id="101cd-528">Esse parâmetro tenta otimizar a liberação do buffer de log causado por uma confirmação durável aguardando um período de tempo especificado antes de forçar uma liberação a ocorrer na esperança de que outra transação compartilhará a liberação.</span><span class="sxs-lookup"><span data-stu-id="101cd-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="101cd-529">**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="101cd-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-530">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-531">0</span><span class="sxs-lookup"><span data-stu-id="101cd-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-532">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-533">Integer</span><span class="sxs-lookup"><span data-stu-id="101cd-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-534">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-535">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="101cd-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-536">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-537">Instância ou sessão</span><span class="sxs-lookup"><span data-stu-id="101cd-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-538">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-539">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-540">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-541">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-542">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-543">No</span><span class="sxs-lookup"><span data-stu-id="101cd-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-544">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-545">No</span><span class="sxs-lookup"><span data-stu-id="101cd-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-546">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-547">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-548">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-549">No</span><span class="sxs-lookup"><span data-stu-id="101cd-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-550">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-551">Tudo</span><span class="sxs-lookup"><span data-stu-id="101cd-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="101cd-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="101cd-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="101cd-553">136</span><span class="sxs-lookup"><span data-stu-id="101cd-553">136</span></span>  

<span data-ttu-id="101cd-554">Esse parâmetro é usado para especificar os recursos de compatibilidade de nomenclatura de arquivo a serem mantidos com o esquema de nomenclatura do arquivo do Windows Server 2003 e anterior.</span><span class="sxs-lookup"><span data-stu-id="101cd-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="101cd-555">Para obter mais informações sobre os diferentes arquivos e sua nomenclatura, consulte [arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md).</span><span class="sxs-lookup"><span data-stu-id="101cd-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="101cd-556">O JET_bitESE98FileNames garante que a extensão de arquivo usada nos arquivos de log de transações e o arquivo de ponto de verificação sejam os mesmos usados no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="101cd-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="101cd-557">Observação: se estiver atualizando do Windows Server 2003, esse bit ainda não precisará ser especificado, pois o mecanismo atualizará automaticamente as extensões de arquivo se JET_paramCircularLog for definido como **true** ou manter a extensão de log mais antiga se JET_paramCircularLog for **false**.</span><span class="sxs-lookup"><span data-stu-id="101cd-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="101cd-558">**Observação**  Para definir um bit, o valor deve primeiro ser recuperado e, em seguida, "ou" no bit de compatibilidade desejado.</span><span class="sxs-lookup"><span data-stu-id="101cd-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-559">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="101cd-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="101cd-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="101cd-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-561">Tipo:</span><span class="sxs-lookup"><span data-stu-id="101cd-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="101cd-562">JET_GRBIT (inteiro)</span><span class="sxs-lookup"><span data-stu-id="101cd-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-563">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="101cd-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="101cd-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="101cd-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-565">Escopo:</span><span class="sxs-lookup"><span data-stu-id="101cd-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="101cd-566">Instância</span><span class="sxs-lookup"><span data-stu-id="101cd-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-567">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-568">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-569">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="101cd-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="101cd-570">No</span><span class="sxs-lookup"><span data-stu-id="101cd-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-571">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="101cd-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="101cd-572">Yes</span><span class="sxs-lookup"><span data-stu-id="101cd-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-573">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-574">No</span><span class="sxs-lookup"><span data-stu-id="101cd-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-575">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="101cd-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="101cd-576">No</span><span class="sxs-lookup"><span data-stu-id="101cd-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-577">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="101cd-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="101cd-578">No</span><span class="sxs-lookup"><span data-stu-id="101cd-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-579">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="101cd-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="101cd-580">Começando com o Windows Server 2008 e o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="101cd-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="101cd-581">Requisitos</span><span class="sxs-lookup"><span data-stu-id="101cd-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="101cd-582"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="101cd-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="101cd-583">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="101cd-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="101cd-584"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="101cd-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="101cd-585">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="101cd-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="101cd-586"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="101cd-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="101cd-587">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="101cd-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="101cd-588">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="101cd-588">See Also</span></span>

[<span data-ttu-id="101cd-589">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="101cd-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="101cd-590">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="101cd-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="101cd-591">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="101cd-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="101cd-592">JetInit</span><span class="sxs-lookup"><span data-stu-id="101cd-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="101cd-593">JetTerm</span><span class="sxs-lookup"><span data-stu-id="101cd-593">JetTerm</span></span>](./jetterm-function.md)
