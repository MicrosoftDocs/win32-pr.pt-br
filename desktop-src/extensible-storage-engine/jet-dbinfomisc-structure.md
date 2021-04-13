---
description: 'Saiba mais sobre: estrutura de JET_DBINFOMISC'
title: Estrutura JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501322"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="60c57-103">Estrutura JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="60c57-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="60c57-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60c57-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="60c57-105">Estrutura JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="60c57-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="60c57-106">A estrutura de **JET_DBINFOMISC** contém informações diversas sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60c57-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="60c57-107">Essas são as informações contidas no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60c57-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="60c57-108">Membros</span><span class="sxs-lookup"><span data-stu-id="60c57-108">Members</span></span>

<span data-ttu-id="60c57-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="60c57-109">**ulVersion**</span></span>

<span data-ttu-id="60c57-110">A versão nativa do mecanismo de banco de dados que criou o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60c57-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="60c57-111">Consulte [JetGetVersion](./jetgetversion-function.md) para recuperar a versão nativa para o mecanismo de banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="60c57-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="60c57-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="60c57-112">**ulUpdate**</span></span>

<span data-ttu-id="60c57-113">Rastreia atualizações de formato de banco de dados incremental que são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="60c57-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60c57-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="60c57-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="60c57-115">Significado</span><span class="sxs-lookup"><span data-stu-id="60c57-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60c57-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="60c57-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="60c57-117">Formato beta do sistema operacional original (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="60c57-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="60c57-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="60c57-119">Adicione colunas no catálogo para indexação condicional e antigo (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="60c57-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="60c57-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="60c57-121">Adicione o sinalizador fLocalizedText no IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="60c57-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="60c57-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="60c57-123">Adicione SPLIT_BUFFER às páginas raiz da árvore de espaço (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="60c57-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="60c57-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="60c57-125">Reverta a revisão para que ESE97 permaneça compatível com o encaminhamento (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="60c57-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="60c57-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="60c57-127">Adicione novas colunas marcadas ao catálogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="60c57-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="60c57-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="60c57-129">Suporte a SLV: signSLV, fSLVExists no cabeçalho do BD (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="60c57-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="60c57-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="60c57-131">Nova árvore de espaço do SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="60c57-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="60c57-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="60c57-133">Mapa de espaço do SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="60c57-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="60c57-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="60c57-135">IDXSEG de 4 bytes (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="60c57-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="60c57-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="60c57-137">Novo formato de coluna de modelo (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="60c57-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="60c57-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="60c57-139">Colunas de modelo classificadas (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="60c57-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-140">0x623, 0</span><span class="sxs-lookup"><span data-stu-id="60c57-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="60c57-141">Novo Gerenciador de espaço (5/15/99).</span><span class="sxs-lookup"><span data-stu-id="60c57-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60c57-142">**signDb**</span><span class="sxs-lookup"><span data-stu-id="60c57-142">**signDb**</span></span>

<span data-ttu-id="60c57-143">Assinatura do banco de dados (incluindo a hora de criação).</span><span class="sxs-lookup"><span data-stu-id="60c57-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="60c57-144">Essa estrutura é de 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="60c57-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="60c57-145">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="60c57-145">**dbstate**</span></span>

<span data-ttu-id="60c57-146">Esse é o estado do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60c57-146">This is the database state.</span></span>

<span data-ttu-id="60c57-147">As opções a seguir estão disponíveis para este membro.</span><span class="sxs-lookup"><span data-stu-id="60c57-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60c57-148">Valor</span><span class="sxs-lookup"><span data-stu-id="60c57-148">Value</span></span></p></th>
<th><p><span data-ttu-id="60c57-149">Significado</span><span class="sxs-lookup"><span data-stu-id="60c57-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60c57-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="60c57-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="60c57-151">1</span><span class="sxs-lookup"><span data-stu-id="60c57-151">1</span></span></p></td>
<td><p><span data-ttu-id="60c57-152">O banco de dados acabou de ser criado.</span><span class="sxs-lookup"><span data-stu-id="60c57-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="60c57-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="60c57-154">2</span><span class="sxs-lookup"><span data-stu-id="60c57-154">2</span></span></p></td>
<td><p><span data-ttu-id="60c57-155">O banco de dados requer a execução de recuperação rígida ou flexível para tornar-se utilizável ou móvel.</span><span class="sxs-lookup"><span data-stu-id="60c57-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="60c57-156">Um não deve tentar mover bancos de dados nesse estado.</span><span class="sxs-lookup"><span data-stu-id="60c57-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="60c57-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="60c57-158">3</span><span class="sxs-lookup"><span data-stu-id="60c57-158">3</span></span></p></td>
<td><p><span data-ttu-id="60c57-159">O banco de dados está em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="60c57-159">The database is in a clean state.</span></span> <span data-ttu-id="60c57-160">O banco de dados pode ser anexado sem nenhum arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="60c57-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="60c57-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="60c57-162">4</span><span class="sxs-lookup"><span data-stu-id="60c57-162">4</span></span></p></td>
<td><p><span data-ttu-id="60c57-163">O banco de dados está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="60c57-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="60c57-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="60c57-165">5</span><span class="sxs-lookup"><span data-stu-id="60c57-165">5</span></span></p></td>
<td><p><span data-ttu-id="60c57-166">Interno.</span><span class="sxs-lookup"><span data-stu-id="60c57-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60c57-167">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="60c57-167">**lgposConsistent**</span></span>

<span data-ttu-id="60c57-168">NULL se o banco de dados estiver em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="60c57-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="60c57-169">Esta é a posição de log que foi usada quando o banco de dados foi trazido pela última vez para um estado de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="60c57-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="60c57-170">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="60c57-170">**logtimeConsistent**</span></span>

<span data-ttu-id="60c57-171">NULL se o banco de dados estiver em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="60c57-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="60c57-172">Essa é a hora em que o banco de dados foi trazido pela última vez para um estado de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="60c57-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="60c57-173">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="60c57-173">**logtimeAttach**</span></span>

<span data-ttu-id="60c57-174">A hora em que o banco de dados foi anexado pela última vez com [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="60c57-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="60c57-175">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="60c57-175">**lgposAttach**</span></span>

<span data-ttu-id="60c57-176">A posição do log que foi usada na última vez em que o banco de dados foi anexado com [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="60c57-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="60c57-177">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="60c57-177">**logtimeDetach**</span></span>

<span data-ttu-id="60c57-178">A hora em que o banco de dados foi desanexado pela última vez com [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="60c57-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="60c57-179">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="60c57-179">**lgposDetach**</span></span>

<span data-ttu-id="60c57-180">A posição do log que foi usada na última vez em que o banco de dados foi desanexado com [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="60c57-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="60c57-181">**signLog**</span><span class="sxs-lookup"><span data-stu-id="60c57-181">**signLog**</span></span>

<span data-ttu-id="60c57-182">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="60c57-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60c57-183">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="60c57-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="60c57-184">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="60c57-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60c57-185">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="60c57-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="60c57-186">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="60c57-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60c57-187">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="60c57-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="60c57-188">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="60c57-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60c57-189">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="60c57-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="60c57-190">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="60c57-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60c57-191">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="60c57-191">**fUpgradeDb**</span></span>

<span data-ttu-id="60c57-192">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="60c57-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60c57-193">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="60c57-193">**dwMajorVersion**</span></span>

<span data-ttu-id="60c57-194">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="60c57-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60c57-195">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="60c57-195">Used for updating indexes.</span></span>

<span data-ttu-id="60c57-196">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="60c57-196">**dwMinorVersion**</span></span>

<span data-ttu-id="60c57-197">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="60c57-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60c57-198">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="60c57-198">Used for updating indexes.</span></span>

<span data-ttu-id="60c57-199">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="60c57-199">**dwBuildNumber**</span></span>

<span data-ttu-id="60c57-200">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="60c57-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60c57-201">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="60c57-201">Used for updating indexes.</span></span>

<span data-ttu-id="60c57-202">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="60c57-202">**lSPNumber**</span></span>

<span data-ttu-id="60c57-203">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="60c57-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60c57-204">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="60c57-204">Used for updating indexes.</span></span>

<span data-ttu-id="60c57-205">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="60c57-205">**cbPageSize**</span></span>

<span data-ttu-id="60c57-206">Tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60c57-206">Database page size.</span></span> <span data-ttu-id="60c57-207">0 significa que o tamanho da página é de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="60c57-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="60c57-208">Esse valor será recuperado somente se JET_DbInfoMisc foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="60c57-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="60c57-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c57-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60c57-210"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="60c57-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60c57-211">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="60c57-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60c57-212"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="60c57-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60c57-213">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="60c57-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60c57-214"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="60c57-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60c57-215">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="60c57-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="60c57-216">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="60c57-216">See Also</span></span>

[<span data-ttu-id="60c57-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="60c57-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="60c57-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="60c57-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="60c57-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="60c57-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="60c57-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="60c57-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="60c57-221">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="60c57-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="60c57-222">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="60c57-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
