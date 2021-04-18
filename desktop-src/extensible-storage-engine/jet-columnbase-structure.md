---
description: 'Saiba mais sobre: estrutura de JET_COLUMNBASE'
title: Estrutura JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764718"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="4a11d-103">Estrutura JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="4a11d-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="4a11d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4a11d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="4a11d-105">Estrutura JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="4a11d-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="4a11d-106">A estrutura de **JET_COLUMNBASE** descreve os parâmetros de uma coluna base.</span><span class="sxs-lookup"><span data-stu-id="4a11d-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="4a11d-107">As funções [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usam a estrutura **JET_COLUMNBASE** .</span><span class="sxs-lookup"><span data-stu-id="4a11d-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="4a11d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4a11d-108">Members</span></span>

<span data-ttu-id="4a11d-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4a11d-109">**cbStruct**</span></span>

<span data-ttu-id="4a11d-110">O tamanho dessa estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4a11d-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="4a11d-111">Defina **cbStruct** como sizeof (JET_COLUMNBASE).</span><span class="sxs-lookup"><span data-stu-id="4a11d-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="4a11d-112">**columnid**</span><span class="sxs-lookup"><span data-stu-id="4a11d-112">**columnid**</span></span>

<span data-ttu-id="4a11d-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4a11d-113">Reserved.</span></span> <span data-ttu-id="4a11d-114">Defina **columnid** como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4a11d-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="4a11d-115">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="4a11d-115">**coltyp**</span></span>

<span data-ttu-id="4a11d-116">O tipo da coluna (por exemplo, texto, binário ou numérico).</span><span class="sxs-lookup"><span data-stu-id="4a11d-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="4a11d-117">Para obter mais informações, consulte [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="4a11d-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="4a11d-118">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="4a11d-118">**wCountry**</span></span>

<span data-ttu-id="4a11d-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4a11d-119">Reserved.</span></span> <span data-ttu-id="4a11d-120">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4a11d-120">Set to 0 (zero).</span></span>

<span data-ttu-id="4a11d-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="4a11d-121">**langid**</span></span>

<span data-ttu-id="4a11d-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4a11d-122">Reserved.</span></span> <span data-ttu-id="4a11d-123">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4a11d-123">Set to 0 (zero).</span></span>

<span data-ttu-id="4a11d-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="4a11d-124">**cp**</span></span>

<span data-ttu-id="4a11d-125">A página de código da coluna.</span><span class="sxs-lookup"><span data-stu-id="4a11d-125">The code page for the column.</span></span> <span data-ttu-id="4a11d-126">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="4a11d-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="4a11d-127">Um valor de zero significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="4a11d-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="4a11d-128">Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.</span><span class="sxs-lookup"><span data-stu-id="4a11d-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="4a11d-129">**wFiller**</span><span class="sxs-lookup"><span data-stu-id="4a11d-129">**wFiller**</span></span>

<span data-ttu-id="4a11d-130">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4a11d-130">Reserved.</span></span> <span data-ttu-id="4a11d-131">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4a11d-131">Set to 0 (zero).</span></span>

<span data-ttu-id="4a11d-132">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="4a11d-132">**cbMax**</span></span>

<span data-ttu-id="4a11d-133">O comprimento máximo, em bytes, de uma coluna de comprimento variável ou o comprimento real, em bytes, de uma coluna de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="4a11d-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="4a11d-134">**grbit**</span><span class="sxs-lookup"><span data-stu-id="4a11d-134">**grbit**</span></span>

<span data-ttu-id="4a11d-135">Opções para a coluna, incluindo zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a11d-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a11d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4a11d-136">Value</span></span></p></th>
<th><p><span data-ttu-id="4a11d-137">Significado</span><span class="sxs-lookup"><span data-stu-id="4a11d-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="4a11d-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="4a11d-139">A coluna é fixada e ocupa a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que ela contém.</span><span class="sxs-lookup"><span data-stu-id="4a11d-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="4a11d-140">JET_bitColumnFixed não pode ser combinada com JET_bitColumnTagged e não pode ser usada quando o membro <strong>coltyp</strong> está definido como <strong>JET_coltypLongText</strong> ou <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="4a11d-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="4a11d-142">A coluna será marcada e ocupará espaço no banco de dados somente se ele contiver dado.</span><span class="sxs-lookup"><span data-stu-id="4a11d-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="4a11d-143">JET_bitColumnTagged não pode ser combinado com JET_bitColumnFixed, JET_bitColumnVersion ou JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="4a11d-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-144">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="4a11d-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="4a11d-145">A coluna não deve ser definida como um valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="4a11d-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="4a11d-146">JET_bitColumnNotNULL não pode ser combinado com JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="4a11d-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="4a11d-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="4a11d-148">A coluna é uma coluna de versão que especifica a versão da linha.</span><span class="sxs-lookup"><span data-stu-id="4a11d-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="4a11d-149">O valor dessa coluna começa em zero e é incrementado automaticamente para cada atualização da linha.</span><span class="sxs-lookup"><span data-stu-id="4a11d-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="4a11d-150">JET_bitColumnVersion pode ser usado somente quando o membro <strong>coltyp</strong> está definido como <strong>JET_coltypLong</strong> e não pode ser combinado com JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged ou JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="4a11d-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="4a11d-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="4a11d-152">A coluna é incrementada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4a11d-152">The column is automatically incremented.</span></span> <span data-ttu-id="4a11d-153">O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="4a11d-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="4a11d-154">No entanto, os números podem não ser sequenciais.</span><span class="sxs-lookup"><span data-stu-id="4a11d-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="4a11d-155">Por exemplo, se cinco linhas forem inseridas em uma tabela, a coluna incrementada automaticamente poderá conter os valores {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="4a11d-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="4a11d-156">JET_bitColumnAutoincrement pode ser usado somente quando o membro <strong>coltyp</strong> é definido como <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong> e não pode ser combinado com JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault ou JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="4a11d-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="4a11d-157"><strong>Windows 2000:  </strong> JET_bitColumnVersion pode ser usado somente quando o membro <strong>coltyp</strong> é definido como <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="4a11d-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="4a11d-159">Válido somente para chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="4a11d-160">JET_bitColumnUpdatable não pode ser combinado com JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="4a11d-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="4a11d-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="4a11d-162">Válido somente em chamadas para <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="4a11d-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="4a11d-164">Válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="4a11d-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="4a11d-166">A coluna pode ter valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="4a11d-166">The column can be multi-valued.</span></span> <span data-ttu-id="4a11d-167">Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela.</span><span class="sxs-lookup"><span data-stu-id="4a11d-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="4a11d-168">Os vários valores em uma coluna com valores múltiplos são identificados por um número no membro <strong>itagSequence</strong> de várias estruturas, por exemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="4a11d-169">Colunas com valores múltiplos devem ser colunas marcadas; ou seja, elas podem não ser colunas de comprimento fixo ou de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="4a11d-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4a11d-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="4a11d-171">Especifica que uma coluna é uma coluna de atualização de caução que pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e terá consistência transacional.</span><span class="sxs-lookup"><span data-stu-id="4a11d-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="4a11d-172">Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</span><span class="sxs-lookup"><span data-stu-id="4a11d-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="4a11d-173">Para uma coluna de atualização de caução, o membro <strong>coltyp</strong> deve ser definido como <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="4a11d-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="4a11d-174">Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</span><span class="sxs-lookup"><span data-stu-id="4a11d-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="4a11d-175">JET_bitColumnEscrowUpdate não pode ser combinado com JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="4a11d-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="4a11d-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="4a11d-177">A coluna é criada sem um número de versão.</span><span class="sxs-lookup"><span data-stu-id="4a11d-177">The column is created without a version number.</span></span> <span data-ttu-id="4a11d-178">Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão.</span><span class="sxs-lookup"><span data-stu-id="4a11d-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="4a11d-179">JET_bitColumnUnversioned é usado somente com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="4a11d-180">Ele não pode ser usado em uma transação.</span><span class="sxs-lookup"><span data-stu-id="4a11d-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="4a11d-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="4a11d-182">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4a11d-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="4a11d-183">JET_bitColumnMaybeNull não pode ser combinado com JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="4a11d-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="4a11d-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="4a11d-185">Não use.</span><span class="sxs-lookup"><span data-stu-id="4a11d-185">Do not use.</span></span> <span data-ttu-id="4a11d-186">Em vez disso, use JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="4a11d-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="4a11d-187">A coluna pode ser finalizada.</span><span class="sxs-lookup"><span data-stu-id="4a11d-187">The column can be finalized.</span></span> <span data-ttu-id="4a11d-188">Uma coluna que pode ser finalizada é uma coluna de atualização de caução que faz com que a linha seja excluída quando a coluna chega a zero.</span><span class="sxs-lookup"><span data-stu-id="4a11d-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="4a11d-189">Versões futuras podem invocar uma função de retorno de chamada em vez disso (consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="4a11d-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="4a11d-190">Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="4a11d-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="4a11d-191">JET_bitColumnFinalize não pode ser combinado com JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="4a11d-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="4a11d-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="4a11d-193">O valor padrão de uma coluna será fornecido por uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4a11d-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="4a11d-194">Consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="4a11d-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="4a11d-195">Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada.</span><span class="sxs-lookup"><span data-stu-id="4a11d-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="4a11d-196">Se JET_bitColumnUserDefinedDefault for especificado, o <strong>pvDefault</strong> deverá apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deverá ser definido como sizeof (JET_USERDEFINEDDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="4a11d-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="4a11d-197">JET_bitColumnUserDefinedDefault não pode ser combinado com JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="4a11d-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="4a11d-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="4a11d-199">A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído.</span><span class="sxs-lookup"><span data-stu-id="4a11d-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="4a11d-200">Um uso comum para colunas Delete-on-zero é como campos de contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="4a11d-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="4a11d-201">Quando o número de referências cair em zero, o registro será excluído.</span><span class="sxs-lookup"><span data-stu-id="4a11d-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="4a11d-202">Uma coluna Delete-on-zero deve ser uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="4a11d-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="4a11d-203">JET_bitColumnDeleteOnZero substitui JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="4a11d-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="4a11d-204">JET_bitColumnDeleteOnZero não pode ser combinada com JET_bitColumnFinalize ou JET_bitColumnUserDefinedDefault e não pode ser usada com colunas padrão definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4a11d-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a11d-205">**szBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="4a11d-205">**szBaseTableName**</span></span>

<span data-ttu-id="4a11d-206">A tabela da qual a tabela atual herda seu DDL.</span><span class="sxs-lookup"><span data-stu-id="4a11d-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="4a11d-207">**szBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="4a11d-207">**szBaseColumnName**</span></span>

<span data-ttu-id="4a11d-208">O nome da coluna na tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="4a11d-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="4a11d-209">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a11d-209">Remarks</span></span>

<span data-ttu-id="4a11d-210">**JET_COLUMNBASE** contém grande parte das mesmas informações que [JET_COLUMNDEF](./jet-columndef-structure.md), mas adiciona campos de cadeia de caracteres para descrever a tabela base (se um DDL hierárquico foi usado).</span><span class="sxs-lookup"><span data-stu-id="4a11d-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="4a11d-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a11d-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-212"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4a11d-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a11d-213">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4a11d-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-214"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4a11d-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a11d-215">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4a11d-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a11d-216"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4a11d-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a11d-217">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4a11d-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a11d-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4a11d-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4a11d-219">Implementado como <strong>JET_COLUMNBASE_W</strong> (Unicode) e <strong>JET_COLUMNBASE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4a11d-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4a11d-220">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4a11d-220">See Also</span></span>

[<span data-ttu-id="4a11d-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="4a11d-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="4a11d-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="4a11d-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="4a11d-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="4a11d-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="4a11d-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4a11d-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="4a11d-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4a11d-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4a11d-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4a11d-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4a11d-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4a11d-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4a11d-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4a11d-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="4a11d-229">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="4a11d-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="4a11d-230">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="4a11d-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="4a11d-231">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="4a11d-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
