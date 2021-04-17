---
description: 'Saiba mais sobre: estrutura de JET_COLUMNLIST'
title: Estrutura JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812384"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="e05cd-103">Estrutura JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="e05cd-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="e05cd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e05cd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="e05cd-105">Estrutura JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="e05cd-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="e05cd-106">A estrutura de **JET_COLUMNLIST** contém as informações necessárias para percorrer a tabela temporária que é criada pelas funções [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e05cd-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="e05cd-107">Cada linha na tabela temporária descreve uma coluna na tabela fornecida na chamada à API.</span><span class="sxs-lookup"><span data-stu-id="e05cd-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="e05cd-108">Essa estrutura é usada somente com [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="e05cd-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e05cd-109">Members</span></span>

<span data-ttu-id="e05cd-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e05cd-110">**cbStruct**</span></span>

<span data-ttu-id="e05cd-111">O tamanho da estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="e05cd-111">The size of the structure in bytes.</span></span> <span data-ttu-id="e05cd-112">A chamada à API atualizará esse campo, de modo que o chamador deve garantir que esse valor corresponda a sizeof (JET_COLUMNLIST).</span><span class="sxs-lookup"><span data-stu-id="e05cd-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="e05cd-113">**TableID**</span><span class="sxs-lookup"><span data-stu-id="e05cd-113">**tableid**</span></span>

<span data-ttu-id="e05cd-114">O identificador de tabela da tabela temporária que foi criada.</span><span class="sxs-lookup"><span data-stu-id="e05cd-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="e05cd-115">É responsabilidade do chamador fechar a tabela.</span><span class="sxs-lookup"><span data-stu-id="e05cd-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="e05cd-116">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="e05cd-116">**cRecord**</span></span>

<span data-ttu-id="e05cd-117">O número de registros na tabela temporária que foi criado pela chamada à API.</span><span class="sxs-lookup"><span data-stu-id="e05cd-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="e05cd-118">**columnidPresentationOrder**</span><span class="sxs-lookup"><span data-stu-id="e05cd-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="e05cd-119">O identificador de coluna da ordem de apresentação.</span><span class="sxs-lookup"><span data-stu-id="e05cd-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="e05cd-120">A ordem de apresentação é usada para classificar as linhas da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="e05cd-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="e05cd-121">A ordem de apresentação é uma [JET_coltypLong](./jet-coltyp.md)fixa.</span><span class="sxs-lookup"><span data-stu-id="e05cd-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="e05cd-122">Se o nível de informação especificado não for um nível compacto, ele também será marcado como JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="e05cd-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="e05cd-123">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="e05cd-123">**columnidcolumnname**</span></span>

<span data-ttu-id="e05cd-124">O identificador de coluna do nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="e05cd-125">Se o nível de informação especificado não foi compactado, ele também será marcado como JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="e05cd-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="e05cd-126">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="e05cd-126">**columnidcolumnid**</span></span>

<span data-ttu-id="e05cd-127">O identificador de coluna do identificador de coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="e05cd-128">O identificador de coluna é um [JET_coltypLong](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-129">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="e05cd-129">**columnidcoltyp**</span></span>

<span data-ttu-id="e05cd-130">O identificador de coluna do tipo de coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-130">The column identifier of the column type.</span></span>

<span data-ttu-id="e05cd-131">O tipo de coluna é um [JET_coltypLong](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-132">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="e05cd-132">**columnidCountry**</span></span>

<span data-ttu-id="e05cd-133">O identificador de coluna do código do país.</span><span class="sxs-lookup"><span data-stu-id="e05cd-133">The column identifier of the country code.</span></span>

<span data-ttu-id="e05cd-134">O código do país é um [JET_coltypShort](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-135">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="e05cd-135">**columnidLangid**</span></span>

<span data-ttu-id="e05cd-136">O identificador de coluna do identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="e05cd-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="e05cd-137">O identificador de idioma é um [JET_coltypShort](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-138">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="e05cd-138">**columnidCp**</span></span>

<span data-ttu-id="e05cd-139">O identificador de coluna da página de código.</span><span class="sxs-lookup"><span data-stu-id="e05cd-139">The column identifier of the code page.</span></span>

<span data-ttu-id="e05cd-140">A página de código é uma [JET_coltypShort](./jet-coltyp.md)fixa.</span><span class="sxs-lookup"><span data-stu-id="e05cd-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-141">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="e05cd-141">**columnidCollate**</span></span>

<span data-ttu-id="e05cd-142">O identificador de coluna da sequência de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="e05cd-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="e05cd-143">A sequência de agrupamento é um [JET_coltypShort](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-144">**columnidcbMax**</span><span class="sxs-lookup"><span data-stu-id="e05cd-144">**columnidcbMax**</span></span>

<span data-ttu-id="e05cd-145">O identificador de coluna do campo **cbMax** .</span><span class="sxs-lookup"><span data-stu-id="e05cd-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="e05cd-146">O **cbMax** é um [JET_coltypLong](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-147">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="e05cd-147">**columnidgrbit**</span></span>

<span data-ttu-id="e05cd-148">O identificador de coluna do *grbits* da coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="e05cd-149">O campo *grbit* é um [JET_coltypLong](./jet-coltyp.md)fixo.</span><span class="sxs-lookup"><span data-stu-id="e05cd-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="e05cd-150">Para obter mais informações sobre esses bits, consulte [JET_COLUMNDEF](./jet-columndef-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="e05cd-151">Estes são os valores possíveis para **columnidgrbit**:</span><span class="sxs-lookup"><span data-stu-id="e05cd-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="e05cd-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="e05cd-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="e05cd-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="e05cd-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="e05cd-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="e05cd-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="e05cd-155">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="e05cd-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="e05cd-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="e05cd-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="e05cd-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="e05cd-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="e05cd-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="e05cd-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="e05cd-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="e05cd-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="e05cd-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="e05cd-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="e05cd-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="e05cd-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="e05cd-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="e05cd-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="e05cd-163">**columnidDefault**</span><span class="sxs-lookup"><span data-stu-id="e05cd-163">**columnidDefault**</span></span>

<span data-ttu-id="e05cd-164">O identificador de coluna do valor padrão da coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="e05cd-165">O valor padrão é um [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-166">**columnidBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="e05cd-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="e05cd-167">O identificador de coluna do nome da tabela da qual a tabela foi derivada.</span><span class="sxs-lookup"><span data-stu-id="e05cd-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="e05cd-168">O nome da tabela é um [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-169">**columnidBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="e05cd-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="e05cd-170">O identificador de coluna do nome da coluna da qual a coluna foi derivada.</span><span class="sxs-lookup"><span data-stu-id="e05cd-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="e05cd-171">O nome da coluna é um [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="e05cd-172">**columnidDefinitionName**</span><span class="sxs-lookup"><span data-stu-id="e05cd-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="e05cd-173">O identificador de coluna do nome da definição de coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="e05cd-174">O nome da definição de coluna é um [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="e05cd-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="e05cd-175">Remarks</span></span>

<span data-ttu-id="e05cd-176">Por padrão, a ordem das linhas na tabela temporária é classificada pelo nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="e05cd-177">Ele também pode ser classificado por identificador de coluna.</span><span class="sxs-lookup"><span data-stu-id="e05cd-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="e05cd-178">Para obter mais informações sobre como classificar por identificador de coluna, consulte [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="e05cd-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="e05cd-179">A chamada para [JetGetColumnInfo](./jetgetcolumninfo-function.md) ou [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) pode especificar uma forma compacta de resultados.</span><span class="sxs-lookup"><span data-stu-id="e05cd-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="e05cd-180">Se alguma coluna tiver sido herdada de uma tabela de modelo, os resultados do Compact não serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="e05cd-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="e05cd-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e05cd-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e05cd-182"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e05cd-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e05cd-183">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e05cd-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05cd-184"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e05cd-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e05cd-185">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e05cd-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05cd-186"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e05cd-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e05cd-187">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e05cd-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e05cd-188">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e05cd-188">See Also</span></span>

[<span data-ttu-id="e05cd-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="e05cd-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="e05cd-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="e05cd-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="e05cd-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e05cd-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="e05cd-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e05cd-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="e05cd-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e05cd-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="e05cd-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e05cd-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="e05cd-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e05cd-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="e05cd-196">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="e05cd-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="e05cd-197">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="e05cd-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
