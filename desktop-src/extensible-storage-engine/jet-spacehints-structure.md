---
description: 'Saiba mais sobre: estrutura de JET_SPACEHINTS'
title: Estrutura de JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
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
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762191"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="ee7dc-103">Estrutura de JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="ee7dc-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="ee7dc-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee7dc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="ee7dc-105">Estrutura de JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="ee7dc-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="ee7dc-106">A estrutura de **JET_SPACEHINTS** contém informações sobre padrões de alocação de espaço quando uma árvore b cresce por meio de divisões de Append ou Hotpoint.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="ee7dc-107">As divisões de acréscimo acontecem quando os registros são adicionados ao final de uma árvore b e as divisões de Hotpoint acontecem quando vários registros são adicionados ao mesmo ponto de inserção virtual (por exemplo, adicionar ' Maria ', ' Mark ', ' Martin' ', ' Mary ' ao meio de uma árvore b que é classificada alfabeticamente).</span><span class="sxs-lookup"><span data-stu-id="ee7dc-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="ee7dc-108">**Windows 7:** A estrutura de **JET_SPACEHINTS** é introduzida no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="ee7dc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ee7dc-109">Members</span></span>

<span data-ttu-id="ee7dc-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-110">**cbStruct**</span></span>

<span data-ttu-id="ee7dc-111">O tamanho, em bytes, dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="ee7dc-112">Defina este membro como sizeof (JET_SPACEHINTS).</span><span class="sxs-lookup"><span data-stu-id="ee7dc-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="ee7dc-113">**ulInitialDensity**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-113">**ulInitialDensity**</span></span>

<span data-ttu-id="ee7dc-114">O layout de densidade em (acréscimo).</span><span class="sxs-lookup"><span data-stu-id="ee7dc-114">The density at (append) layout.</span></span>

<span data-ttu-id="ee7dc-115">**cbInitial**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-115">**cbInitial**</span></span>

<span data-ttu-id="ee7dc-116">O tamanho inicial (em bytes) do objeto que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="ee7dc-117">Deve ser um múltiplo do tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="ee7dc-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-118">**grbit**</span></span>

<span data-ttu-id="ee7dc-119">Um grupo de bits que contém as opções a serem usadas para esta estrutura, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee7dc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ee7dc-120">Value</span></span></p></th>
<th><p><span data-ttu-id="ee7dc-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ee7dc-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee7dc-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="ee7dc-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="ee7dc-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee7dc-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="ee7dc-124">Altera a política de alocação interna para obter espaço heirarchically do pai imediato de uma árvore b.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7dc-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="ee7dc-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="ee7dc-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ee7dc-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="ee7dc-127">Permite que o comportamento da divisão de acréscimo cresça de acordo com a dinâmica de crescimento da tabela (definida por cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="ee7dc-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7dc-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="ee7dc-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="ee7dc-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ee7dc-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="ee7dc-130">Permite que o comportamento de divisão de Hotpoint cresça de acordo com a dinâmica de crescimento da tabela (definida por cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="ee7dc-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7dc-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="ee7dc-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="ee7dc-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee7dc-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="ee7dc-133">Se definido, o cliente indica que a verificação sequencial de encaminhamento é o padrão de uso predominante desta tabela.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7dc-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="ee7dc-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="ee7dc-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ee7dc-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="ee7dc-136">Se definido, o cliente indica que a verificação sequencial retroativa é o padrão de uso predominante desta tabela.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7dc-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="ee7dc-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="ee7dc-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ee7dc-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="ee7dc-139">Se definido, o aplicativo espera que essa tabela seja limpa em ordem sequencial, da chave mais baixa para a chave mais alta.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee7dc-140">**ulMaintDensity**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-140">**ulMaintDensity**</span></span>

<span data-ttu-id="ee7dc-141">densidade para mulMaintDensity</span><span class="sxs-lookup"><span data-stu-id="ee7dc-141">density to mulMaintDensity</span></span>

<span data-ttu-id="ee7dc-142">Densidade a ser mantida em.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-142">Density to maintain at.</span></span> <span data-ttu-id="ee7dc-143">Se as dicas de espaço especificarem JET_bitRetrieveHintTableScanForward ou JET_bitRetrieveHintTableScanBackward, a desfragmentação da tabela será disparada quando o espaço usado na tabela cair abaixo desse limite.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="ee7dc-144">A desfragmentação de tabela pode ser desabilitada definindo esse membro como zero.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="ee7dc-145">Definir esse membro como 100 fará com que a desfragmentação da tabela seja executada assim que uma página for liberada.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="ee7dc-146">**ulGrowth**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-146">**ulGrowth**</span></span>

<span data-ttu-id="ee7dc-147">O percentual de crescimento do último crescimento ou tamanho inicial, arredondado para o tamanho de alocação mais próximo do JET nativo.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="ee7dc-148">**cbMinExtent muito pequeno**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="ee7dc-149">Isso substitui ulGrowth se for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="ee7dc-150">**cbMaxExtent**</span><span class="sxs-lookup"><span data-stu-id="ee7dc-150">**cbMaxExtent**</span></span>

<span data-ttu-id="ee7dc-151">O valor máximo para crescimento em bytes.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="ee7dc-152">Este ulGrowth de Caps.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="ee7dc-153">Quando uma árvore b cresce através de divisões de Append ou Hotpoint (em oposição às inserções de registros aleatórios), a quantidade de espaço que a tabela aumentará é calculada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ee7dc-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="ee7dc-154">Na criação, fornecemos o cbInitial da árvore b, sempre.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="ee7dc-155">Durante a primeira alocação de uma determinada área, alocaremos: cbInitial \* ulGrowth/100 (arredondado para o tamanho da página do banco de dados) ou cbMinExtent se for maior.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="ee7dc-156">Durante a próxima alocação, cbLastAlloc \* ulGrowth/100 (arredondado para o tamanho da página do DB) ou cbMinExtent se for maior.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="ee7dc-157">Em alguma alocação (que pode ser a primeira alocação), o tamanho calculado excederá cbMaxExtent e esse será o tamanho de crescimento depois disso.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="ee7dc-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee7dc-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee7dc-159"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ee7dc-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7dc-160">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee7dc-161"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ee7dc-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7dc-162">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee7dc-163"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ee7dc-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee7dc-164">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ee7dc-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ee7dc-165">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ee7dc-165">See Also</span></span>

[<span data-ttu-id="ee7dc-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="ee7dc-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="ee7dc-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="ee7dc-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
