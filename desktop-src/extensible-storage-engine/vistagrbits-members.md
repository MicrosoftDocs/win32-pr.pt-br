---
description: 'Saiba mais sobre: membros do VistaGrbits'
title: Membros VistaGrbits (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565616"
---
# <a name="vistagrbits-members"></a><span data-ttu-id="f33b4-103">Membros do VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="f33b4-103">VistaGrbits members</span></span>

<span data-ttu-id="f33b4-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="f33b4-104">Include protected members</span></span>  
<span data-ttu-id="f33b4-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="f33b4-105">Include inherited members</span></span>  

<span data-ttu-id="f33b4-106">Grbits que foram adicionados à versão vista do ESENT.</span><span class="sxs-lookup"><span data-stu-id="f33b4-106">Grbits that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="f33b4-107">O tipo [VistaGrbits](./vistagrbits-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f33b4-107">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="f33b4-108">Campos</span><span class="sxs-lookup"><span data-stu-id="f33b4-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f33b4-109">Nome</span><span class="sxs-lookup"><span data-stu-id="f33b4-109">Name</span></span></th>
<th><span data-ttu-id="f33b4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f33b4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="f33b4-114">A sessão de instantâneo continua após JetOSSnapshotThaw e exigirá uma chamada de função JetOSSnapshotEnd.</span><span class="sxs-lookup"><span data-stu-id="f33b4-114">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="f33b4-118">A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna com vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave.</span><span class="sxs-lookup"><span data-stu-id="f33b4-118">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="f33b4-119">Caso contrário, o índice teria apenas uma entrada para cada valor múltiplo na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usaria o primeiro valor múltiplo de outras colunas de chave que são colunas com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="f33b4-119">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="f33b4-120">Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores &quot; vermelho &quot; e &quot; azul &quot; e acima da coluna B que tem os valores &quot; 1 &quot; e &quot; 2 &quot; , as seguintes entradas de índice serão criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; vermelho &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="f33b4-120">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="f33b4-121">Caso contrário, as seguintes entradas de índice seriam criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="f33b4-121">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="f33b4-125">A especificação desse sinalizador fará com que qualquer atualização para o índice resulte em uma chave truncada falhe com <a href="hh564840(v=exchg.10).md">keytruncate</a>.</span><span class="sxs-lookup"><span data-stu-id="f33b4-125">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="f33b4-126">Caso contrário, as chaves serão truncadas silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="f33b4-126">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="f33b4-130">Indexar várias colunas com vários valores, mas apenas com valores do mesmo itagSequence.</span><span class="sxs-lookup"><span data-stu-id="f33b4-130">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="f33b4-134">Os logs de transações devem existir no diretório do arquivo de log (ou seja, não é possível iniciar automaticamente um novo fluxo).</span><span class="sxs-lookup"><span data-stu-id="f33b4-134">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="f33b4-138">Execute a recuperação, mas pare na fase de desfazer.</span><span class="sxs-lookup"><span data-stu-id="f33b4-138">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="f33b4-139">Permite que os logs presentes sejam reproduzidos e, posteriormente, os logs adicionais possam ser copiados e reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="f33b4-139">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="f33b4-143">Padrão de entrada de mapa de banco de dados ausente para o mesmo local.</span><span class="sxs-lookup"><span data-stu-id="f33b4-143">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="f33b4-147">O mecanismo pode marcar os cabeçalhos do banco de dados conforme apropriado (por exemplo, um backup completo concluído), mesmo que a chamada para truncar não tenha sido concluída.</span><span class="sxs-lookup"><span data-stu-id="f33b4-147">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f33b4-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="f33b4-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="f33b4-151">Na recuperação reversível bem-sucedida, TRUNCATE os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="f33b4-151">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f33b4-152">Parte superior</span><span class="sxs-lookup"><span data-stu-id="f33b4-152">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f33b4-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="f33b4-153">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f33b4-154">Referência</span><span class="sxs-lookup"><span data-stu-id="f33b4-154">Reference</span></span>

[<span data-ttu-id="f33b4-155">Classe VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="f33b4-155">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="f33b4-156">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="f33b4-156">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
