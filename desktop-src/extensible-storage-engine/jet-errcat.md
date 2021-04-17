---
description: 'Saiba mais sobre: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797606"
---
# <a name="jet_errcat"></a><span data-ttu-id="6b129-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="6b129-103">JET_ERRCAT</span></span>


<span data-ttu-id="6b129-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6b129-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="6b129-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="6b129-105">JET_ERRCAT</span></span>

<span data-ttu-id="6b129-106">O **JET_ERRCAT** grupo de constantes descreve as classificações de nível superior ou as categorias de erros.</span><span class="sxs-lookup"><span data-stu-id="6b129-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="6b129-107">Esse grupo de constantes permite que os aplicativos definam o tratamento padrão para uma classificação de erros, em vez de manipular cada caso de erro individualmente.</span><span class="sxs-lookup"><span data-stu-id="6b129-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="6b129-108">Ele também garante que o aplicativo não precise lidar com novas condições de erro incluídas nas classificações existentes.</span><span class="sxs-lookup"><span data-stu-id="6b129-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="6b129-109">Observação: esta documentação se baseia em uma versão preliminar do mecanismo de armazenamento extensível.</span><span class="sxs-lookup"><span data-stu-id="6b129-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="6b129-110">Essas informações estão sujeitas a alterações.</span><span class="sxs-lookup"><span data-stu-id="6b129-110">This information is subject to change.</span></span>

<span data-ttu-id="6b129-111">As constantes **JET_ERRCAT** são organizadas em uma hierarquia específica de condições e subcondiçãos, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6b129-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="6b129-112">| Erro de---|---operação (al) | |---fatal | |---IO | |---recurso | |---memória | |---cota | |---disco | |---dados | |---corrupção | |---de estado inconsistente | |---fragmentação | |---</span><span class="sxs-lookup"><span data-stu-id="6b129-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="6b129-113">A tabela a seguir lista as constantes **JET_ERRCAT** e fornece uma descrição e informações de recuperação, conforme aplicável.</span><span class="sxs-lookup"><span data-stu-id="6b129-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b129-114">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6b129-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="6b129-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b129-115">Description</span></span></p></th>
<th><p><span data-ttu-id="6b129-116">Recuperação</span><span class="sxs-lookup"><span data-stu-id="6b129-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b129-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="6b129-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="6b129-118">Uma categoria de erro inválida.</span><span class="sxs-lookup"><span data-stu-id="6b129-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="6b129-119">N/D</span><span class="sxs-lookup"><span data-stu-id="6b129-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="6b129-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="6b129-121">A categoria de nível superior (nenhum erro deve ser dessa classe).</span><span class="sxs-lookup"><span data-stu-id="6b129-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="6b129-122">Consulte as constantes de erro específicas.</span><span class="sxs-lookup"><span data-stu-id="6b129-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="6b129-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="6b129-124">Representa os erros que podem ocorrer a qualquer momento devido a condições não controláveis e geralmente são temporários.</span><span class="sxs-lookup"><span data-stu-id="6b129-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="6b129-125">Consulte subcategorias, se especificado.</span><span class="sxs-lookup"><span data-stu-id="6b129-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="6b129-126">Tente novamente e, se o erro continuar, informe o operador.</span><span class="sxs-lookup"><span data-stu-id="6b129-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="6b129-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="6b129-128">Representa erros fatais que, quando ocorrem, criam um risco de que o ESE não possa continuar em uma maneira segura (geralmente transacional) e os dados possam ser corrompidos.</span><span class="sxs-lookup"><span data-stu-id="6b129-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="6b129-129">Reinicie a instância ou o processo.</span><span class="sxs-lookup"><span data-stu-id="6b129-129">Restart the instance or process.</span></span> <span data-ttu-id="6b129-130">Se o problema persistir, informe o operador.</span><span class="sxs-lookup"><span data-stu-id="6b129-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="6b129-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="6b129-132">Representa os erros de e/s, que vêm do sistema operacional e estão fora do controle do ESE.</span><span class="sxs-lookup"><span data-stu-id="6b129-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="6b129-133">Esse tipo de erro pode ser temporário.</span><span class="sxs-lookup"><span data-stu-id="6b129-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="6b129-134">Tente novamente e, se o erro continuar, peça ao operador para verificar o disco.</span><span class="sxs-lookup"><span data-stu-id="6b129-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="6b129-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="6b129-136">Representa uma categoria de erros relacionados à falta de condições de recurso.</span><span class="sxs-lookup"><span data-stu-id="6b129-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="6b129-137">Consulte subcategorias.</span><span class="sxs-lookup"><span data-stu-id="6b129-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="6b129-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="6b129-139">Representa um erro causado por falta de memória.</span><span class="sxs-lookup"><span data-stu-id="6b129-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="6b129-140">Tente novamente após um período de tempo, libere memória ou saia.</span><span class="sxs-lookup"><span data-stu-id="6b129-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="6b129-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="6b129-142">Determinados &quot; &quot; recursos de especialidade estão em pools de um determinado tamanho, facilitando a detecção de vazamentos desses recursos.</span><span class="sxs-lookup"><span data-stu-id="6b129-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="6b129-143">O aplicativo deve <strong>declarar ()</strong> para detectar esses problemas durante o desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="6b129-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="6b129-144">No entanto, no código de varejo, o aplicativo deve tratá-lo como um erro de memória.</span><span class="sxs-lookup"><span data-stu-id="6b129-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="6b129-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="6b129-146">Representa um erro causado por falta de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="6b129-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="6b129-147">Tente novamente mais tarde para determinar se há mais espaço em disco disponível ou peça ao operador para liberar espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="6b129-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="6b129-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="6b129-149">Representa uma categoria de nível superior para erros relacionados a dados.</span><span class="sxs-lookup"><span data-stu-id="6b129-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="6b129-150">Consulte subcategorias.</span><span class="sxs-lookup"><span data-stu-id="6b129-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="6b129-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="6b129-152">Representa um problema de corrupção, que geralmente é permanente sem ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="6b129-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="6b129-153">Restaure a partir do backup usando a operação de reparo de utilitários ESE (essa operação restaura somente os dados que são restantes/com perda).</span><span class="sxs-lookup"><span data-stu-id="6b129-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="6b129-154">Além disso, quando o método Recovery (JetInit) é usado, a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, consulte <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="6b129-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="6b129-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="6b129-156">Representa um erro no qual os arquivos de banco de dados e/ou de log estão em um estado inconsistente e não podem ser reconciliados.</span><span class="sxs-lookup"><span data-stu-id="6b129-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="6b129-157">Esse erro pode ser causado por um aplicativo/administrador indisponível.</span><span class="sxs-lookup"><span data-stu-id="6b129-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="6b129-158">Restaure a partir do backup usando a operação de reparo de utilitários ESE (que restaura apenas os dados que são restantes/com perda).</span><span class="sxs-lookup"><span data-stu-id="6b129-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="6b129-159">Também no caso da operação de <strong>recuperação (JetInit)</strong> , a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, consulte <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="6b129-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="6b129-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="6b129-161">Representa uma classe de erros em que um recurso interno persistente foi executado.</span><span class="sxs-lookup"><span data-stu-id="6b129-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="6b129-162">Para erros de banco de dados, a desfragmentação offline corrigirá o problema.</span><span class="sxs-lookup"><span data-stu-id="6b129-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="6b129-163">Para os arquivos de log, primeiro Recupere todos os bancos de dados anexados para um desligamento normal e, em seguida, exclua todos os arquivos de log e o ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="6b129-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="6b129-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="6b129-165">Consulte subcategorias.</span><span class="sxs-lookup"><span data-stu-id="6b129-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="6b129-166">Consulte subcategorias.</span><span class="sxs-lookup"><span data-stu-id="6b129-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="6b129-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="6b129-168">Representa um erro de uso.</span><span class="sxs-lookup"><span data-stu-id="6b129-168">Represents a usage error.</span></span> <span data-ttu-id="6b129-169">O código do cliente não passou os argumentos corretos para a API do <strong>Jet</strong> .</span><span class="sxs-lookup"><span data-stu-id="6b129-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="6b129-170">Esse erro persistirá com a repetição.</span><span class="sxs-lookup"><span data-stu-id="6b129-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="6b129-171">O código do cliente deve usar o método <strong>Assert ()</strong> para garantir que essa classe de erros não seja retornada, de modo que os problemas possam ser detectados durante o desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="6b129-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="6b129-172">No varejo, o aplicativo deve notificar o operador sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="6b129-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="6b129-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="6b129-174">Representa uma classe de mensagens que a API pode retornar para descrever o estado do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b129-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="6b129-175">Por exemplo, o método <a href="gg294103(v=exchg.10).md">JetSeek ()</a> pode retornar <strong>JET_errRecordNotFound</strong> quando o registro solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6b129-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="6b129-176">Varia de acordo com a API.</span><span class="sxs-lookup"><span data-stu-id="6b129-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="6b129-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="6b129-178">Representa os erros que são de uma versão anterior do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="6b129-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="6b129-179">Esses erros não devem ser retornados pelo mecanismo atual.</span><span class="sxs-lookup"><span data-stu-id="6b129-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="6b129-180">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6b129-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="6b129-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="6b129-182">Uma constante que indica o final da enumeração.</span><span class="sxs-lookup"><span data-stu-id="6b129-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="6b129-183">N/D</span><span class="sxs-lookup"><span data-stu-id="6b129-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="6b129-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b129-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b129-185"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-186">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6b129-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b129-187"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-188">Requer o Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="6b129-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b129-189"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6b129-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6b129-190">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6b129-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

