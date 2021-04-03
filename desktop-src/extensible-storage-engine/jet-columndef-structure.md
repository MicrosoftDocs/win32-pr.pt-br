---
description: 'Saiba mais sobre: estrutura de JET_COLUMNDEF'
title: Estrutura JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922850"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="db900-103">Estrutura JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="db900-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="db900-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="db900-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="db900-105">Estrutura JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="db900-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="db900-106">A estrutura de **JET_COLUMNDEF** define os dados que podem ser armazenados em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="db900-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="db900-107">Membros</span><span class="sxs-lookup"><span data-stu-id="db900-107">Members</span></span>

<span data-ttu-id="db900-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="db900-108">**cbStruct**</span></span>

<span data-ttu-id="db900-109">O tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="db900-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="db900-110">Ele deve ser definido como sizeof (JET_COLUMNDEF).</span><span class="sxs-lookup"><span data-stu-id="db900-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="db900-111">**columnid**</span><span class="sxs-lookup"><span data-stu-id="db900-111">**columnid**</span></span>

<span data-ttu-id="db900-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="db900-112">Reserved.</span></span> <span data-ttu-id="db900-113">**columnid** deve ser definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="db900-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="db900-114">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="db900-114">**coltyp**</span></span>

<span data-ttu-id="db900-115">O tipo da coluna (por exemplo, texto, binário ou numérico).</span><span class="sxs-lookup"><span data-stu-id="db900-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="db900-116">Para obter mais informações, consulte [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="db900-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="db900-117">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="db900-117">**wCountry**</span></span>

<span data-ttu-id="db900-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="db900-118">Reserved.</span></span> <span data-ttu-id="db900-119">**wCountry** deve ser definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="db900-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="db900-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="db900-120">**langid**</span></span>

<span data-ttu-id="db900-121">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="db900-121">Obsolete.</span></span> <span data-ttu-id="db900-122">**LangID** deve ser definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="db900-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="db900-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="db900-123">**cp**</span></span>

<span data-ttu-id="db900-124">A página de código da coluna.</span><span class="sxs-lookup"><span data-stu-id="db900-124">The code page for the column.</span></span> <span data-ttu-id="db900-125">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="db900-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="db900-126">Um valor de zero significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="db900-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="db900-127">Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.</span><span class="sxs-lookup"><span data-stu-id="db900-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="db900-128">**wCollate**</span><span class="sxs-lookup"><span data-stu-id="db900-128">**wCollate**</span></span>

<span data-ttu-id="db900-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="db900-129">Reserved.</span></span> <span data-ttu-id="db900-130">**wCollate** deve ser definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="db900-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="db900-131">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="db900-131">**cbMax**</span></span>

<span data-ttu-id="db900-132">O comprimento máximo, em bytes, de uma coluna de comprimento variável ou o comprimento de uma coluna de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="db900-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="db900-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="db900-133">**grbit**</span></span>

<span data-ttu-id="db900-134">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="db900-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db900-135">Valor</span><span class="sxs-lookup"><span data-stu-id="db900-135">Value</span></span></p></th>
<th><p><span data-ttu-id="db900-136">Significado</span><span class="sxs-lookup"><span data-stu-id="db900-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db900-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="db900-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="db900-138">A coluna será corrigida.</span><span class="sxs-lookup"><span data-stu-id="db900-138">The column will be fixed.</span></span> <span data-ttu-id="db900-139">Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que está sendo armazenada na coluna.</span><span class="sxs-lookup"><span data-stu-id="db900-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="db900-140">JET_bitColumnFixed não pode ser usada com JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="db900-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="db900-141">Esse bit não pode ser usado com valores longos ( <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="db900-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="db900-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="db900-143">A coluna será marcada.</span><span class="sxs-lookup"><span data-stu-id="db900-143">The column will be tagged.</span></span> <span data-ttu-id="db900-144">As colunas marcadas não ocupam nenhum espaço no banco de dados se não contiverem.</span><span class="sxs-lookup"><span data-stu-id="db900-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="db900-145">Esse bit não pode ser usado com JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="db900-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-146">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="db900-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="db900-147">A coluna nunca deve ser definida como um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="db900-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="db900-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="db900-149">A coluna é uma coluna de versão que especifica a versão da linha.</span><span class="sxs-lookup"><span data-stu-id="db900-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="db900-150">O valor desta coluna começa em zero e será incrementado automaticamente para cada atualização na linha.</span><span class="sxs-lookup"><span data-stu-id="db900-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="db900-151">Esse bit só pode ser aplicado a <strong>JET_coltypLong</strong> colunas.</span><span class="sxs-lookup"><span data-stu-id="db900-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="db900-152">Esse bit não pode ser usado com JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate ou JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="db900-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="db900-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="db900-154">A coluna será incrementada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="db900-154">The column will automatically be incremented.</span></span> <span data-ttu-id="db900-155">O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="db900-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="db900-156">No entanto, os números podem não ser contínuos.</span><span class="sxs-lookup"><span data-stu-id="db900-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="db900-157">Por exemplo, se cinco linhas forem inseridas em uma tabela, a &quot; coluna AutoIncrement &quot; poderá conter os valores {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="db900-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="db900-158">Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="db900-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="db900-159"><strong>Windows 2000:  </strong> No Windows 2000, esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="db900-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="db900-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="db900-161">Esse bit é válido somente em chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="db900-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="db900-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="db900-163">Esse bit é válido somente em chamadas para <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="db900-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="db900-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="db900-165">Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="db900-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="db900-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="db900-167">A coluna pode ter valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="db900-167">The column can be multi-valued.</span></span> <span data-ttu-id="db900-168">Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela.</span><span class="sxs-lookup"><span data-stu-id="db900-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="db900-169">Os vários valores em uma coluna com valores múltiplos são identificados por um número chamado membro <strong>itagSequence</strong> , que pertence a várias estruturas, incluindo: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>e <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="db900-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="db900-170">Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ter colunas de comprimento fixo ou de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="db900-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="db900-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="db900-172">Especifica que uma coluna é uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="db900-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="db900-173">Uma coluna de atualização de caução pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manterá a consistência transacional.</span><span class="sxs-lookup"><span data-stu-id="db900-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="db900-174">Uma coluna de atualização de caução também deve atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="db900-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="db900-175">Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</span><span class="sxs-lookup"><span data-stu-id="db900-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="db900-176">Uma coluna de atualização de caução deve ser do tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="db900-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="db900-177">Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</span><span class="sxs-lookup"><span data-stu-id="db900-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="db900-178">JET_bitColumnEscrowUpdate não pode ser usado em conjunto com JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="db900-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="db900-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="db900-180">A coluna será criada em uma sem informações de versão.</span><span class="sxs-lookup"><span data-stu-id="db900-180">The column will be created in an without version information.</span></span> <span data-ttu-id="db900-181">Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão.</span><span class="sxs-lookup"><span data-stu-id="db900-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="db900-182">Esse bit só é útil com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="db900-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="db900-183">Ele não pode ser usado em uma transação.</span><span class="sxs-lookup"><span data-stu-id="db900-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="db900-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="db900-185">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="db900-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="db900-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="db900-187">Use JET_bitColumnDeleteOnZero em vez de JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="db900-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="db900-188">JET_bitColumnFinalize que uma coluna pode ser finalizada.</span><span class="sxs-lookup"><span data-stu-id="db900-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="db900-189">Quando uma coluna que pode ser finalizada tem uma coluna de atualização de caução que chega a zero, a linha será excluída.</span><span class="sxs-lookup"><span data-stu-id="db900-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="db900-190">Versões futuras podem invocar uma função de chamada de retorno (para obter mais informações, consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="db900-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="db900-191">Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="db900-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="db900-192">JET_bitColumnFinalize não pode ser usada com JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="db900-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="db900-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="db900-194">O valor padrão de uma coluna será fornecido por uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="db900-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="db900-195">Consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="db900-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="db900-196">Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada.</span><span class="sxs-lookup"><span data-stu-id="db900-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="db900-197">Especificar JET_bitColumnUserDefinedDefault significa que <strong>pvDefault</strong> deve apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve ser definido como sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span><span class="sxs-lookup"><span data-stu-id="db900-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="db900-198">JET_bitColumnUserDefinedDefault não pode ser usado em conjunto com JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="db900-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="db900-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="db900-200">A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído.</span><span class="sxs-lookup"><span data-stu-id="db900-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="db900-201">Um uso comum para uma coluna que pode ser finalizada é usá-lo como um campo de contagem de referência e, quando o campo atinge zero, o registro é excluído.</span><span class="sxs-lookup"><span data-stu-id="db900-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="db900-202">JET_bitColumnDeleteOnZero está relacionado a JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="db900-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="db900-203">Uma coluna Delete-on-zero deve ser uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="db900-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="db900-204">JET_bitColumnDeleteOnZero não pode ser usada com JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="db900-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="db900-205">JET_bitColumnDeleteOnZero não pode ser usado com colunas padrão definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="db900-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="db900-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db900-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db900-207"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="db900-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="db900-208">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="db900-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db900-209"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="db900-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="db900-210">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="db900-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db900-211"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="db900-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="db900-212">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="db900-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="db900-213">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="db900-213">See Also</span></span>

[<span data-ttu-id="db900-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="db900-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="db900-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="db900-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="db900-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="db900-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="db900-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="db900-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="db900-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="db900-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="db900-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="db900-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="db900-220">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="db900-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="db900-221">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="db900-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="db900-222">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="db900-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="db900-223">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="db900-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="db900-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="db900-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="db900-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="db900-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="db900-226">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="db900-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
