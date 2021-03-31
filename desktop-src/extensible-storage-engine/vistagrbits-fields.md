---
description: 'Saiba mais sobre: campos VistaGrbits'
title: Campos VistaGrbits (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: VistaGrbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104318
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3694dae8c55a5da838b8fcc058b369d7f0a59ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837445"
---
# <a name="vistagrbits-fields"></a><span data-ttu-id="77fc5-103">Campos VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="77fc5-103">VistaGrbits fields</span></span>

<span data-ttu-id="77fc5-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="77fc5-104">Include protected members</span></span>  
<span data-ttu-id="77fc5-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="77fc5-105">Include inherited members</span></span>  

<span data-ttu-id="77fc5-106">O tipo [VistaGrbits](./vistagrbits-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="77fc5-106">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="77fc5-107">Campos</span><span class="sxs-lookup"><span data-stu-id="77fc5-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="77fc5-108">Nome</span><span class="sxs-lookup"><span data-stu-id="77fc5-108">Name</span></span></th>
<th><span data-ttu-id="77fc5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="77fc5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="77fc5-113">A sessão de instantâneo continua após JetOSSnapshotThaw e exigirá uma chamada de função JetOSSnapshotEnd.</span><span class="sxs-lookup"><span data-stu-id="77fc5-113">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="77fc5-117">A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna com vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave.</span><span class="sxs-lookup"><span data-stu-id="77fc5-117">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="77fc5-118">Caso contrário, o índice teria apenas uma entrada para cada valor múltiplo na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usaria o primeiro valor múltiplo de outras colunas de chave que são colunas com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="77fc5-118">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="77fc5-119">Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores &quot; vermelho &quot; e &quot; azul &quot; e acima da coluna B que tem os valores &quot; 1 &quot; e &quot; 2 &quot; , as seguintes entradas de índice serão criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; vermelho &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="77fc5-119">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="77fc5-120">Caso contrário, as seguintes entradas de índice seriam criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="77fc5-120">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="77fc5-124">A especificação desse sinalizador fará com que qualquer atualização para o índice resulte em uma chave truncada falhe com <a href="hh564840(v=exchg.10).md">keytruncate</a>.</span><span class="sxs-lookup"><span data-stu-id="77fc5-124">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="77fc5-125">Caso contrário, as chaves serão truncadas silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="77fc5-125">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="77fc5-129">Indexar várias colunas com vários valores, mas apenas com valores do mesmo itagSequence.</span><span class="sxs-lookup"><span data-stu-id="77fc5-129">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="77fc5-133">Os logs de transações devem existir no diretório do arquivo de log (ou seja, não é possível iniciar automaticamente um novo fluxo).</span><span class="sxs-lookup"><span data-stu-id="77fc5-133">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="77fc5-137">Execute a recuperação, mas pare na fase de desfazer.</span><span class="sxs-lookup"><span data-stu-id="77fc5-137">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="77fc5-138">Permite que os logs presentes sejam reproduzidos e, posteriormente, os logs adicionais possam ser copiados e reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="77fc5-138">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="77fc5-142">Padrão de entrada de mapa de banco de dados ausente para o mesmo local.</span><span class="sxs-lookup"><span data-stu-id="77fc5-142">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="77fc5-146">O mecanismo pode marcar os cabeçalhos do banco de dados conforme apropriado (por exemplo, um backup completo concluído), mesmo que a chamada para truncar não tenha sido concluída.</span><span class="sxs-lookup"><span data-stu-id="77fc5-146">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="77fc5-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="77fc5-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="77fc5-150">Na recuperação reversível bem-sucedida, TRUNCATE os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="77fc5-150">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77fc5-151">Parte superior</span><span class="sxs-lookup"><span data-stu-id="77fc5-151">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="77fc5-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="77fc5-152">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77fc5-153">Referência</span><span class="sxs-lookup"><span data-stu-id="77fc5-153">Reference</span></span>

[<span data-ttu-id="77fc5-154">Classe VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="77fc5-154">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="77fc5-155">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="77fc5-155">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
