---
description: 'Saiba mais sobre: estrutura de JET_INDEXLIST'
title: Estrutura JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297048"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="c7caf-103">Estrutura JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="c7caf-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="c7caf-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c7caf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="c7caf-105">Estrutura JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="c7caf-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="c7caf-106">A estrutura de **JET_INDEXLIST** contém as informações necessárias para atravessar uma tabela temporária que é criada pelas funções [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c7caf-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="c7caf-107">Cada linha na tabela temporária descreve uma coluna de um índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="c7caf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c7caf-108">Members</span></span>

<span data-ttu-id="c7caf-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c7caf-109">**cbStruct**</span></span>

<span data-ttu-id="c7caf-110">O tamanho da estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="c7caf-110">The size of the structure in bytes.</span></span> <span data-ttu-id="c7caf-111">A chamada à API atualizará esse campo, de modo que o chamador deve garantir que esse valor corresponda a sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="c7caf-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="c7caf-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="c7caf-112">**tableid**</span></span>

<span data-ttu-id="c7caf-113">O identificador de tabela da tabela temporária que foi criada.</span><span class="sxs-lookup"><span data-stu-id="c7caf-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="c7caf-114">É responsabilidade do chamador fechar a tabela.</span><span class="sxs-lookup"><span data-stu-id="c7caf-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="c7caf-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="c7caf-115">**cRecord**</span></span>

<span data-ttu-id="c7caf-116">O número de registros na tabela temporária que foi criado.</span><span class="sxs-lookup"><span data-stu-id="c7caf-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="c7caf-117">**columnidindexname**</span><span class="sxs-lookup"><span data-stu-id="c7caf-117">**columnidindexname**</span></span>

<span data-ttu-id="c7caf-118">O identificador de coluna do nome do índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="c7caf-119">Esta coluna é uma [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-120">**columnidgrbitIndex**</span><span class="sxs-lookup"><span data-stu-id="c7caf-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="c7caf-121">O identificador de coluna do *grbits* usado no índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="c7caf-122">Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter uma lista de bits válidos.</span><span class="sxs-lookup"><span data-stu-id="c7caf-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="c7caf-123">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-124">**columnidcKey**</span><span class="sxs-lookup"><span data-stu-id="c7caf-124">**columnidcKey**</span></span>

<span data-ttu-id="c7caf-125">O identificador de coluna do número de chaves no índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="c7caf-126">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-127">**columnidcEntry**</span><span class="sxs-lookup"><span data-stu-id="c7caf-127">**columnidcEntry**</span></span>

<span data-ttu-id="c7caf-128">O identificador de coluna do número de entradas no índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="c7caf-129">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-130">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="c7caf-130">**columnidcPage**</span></span>

<span data-ttu-id="c7caf-131">O identificador de coluna do número de páginas que o índice usa. Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-132">**columnidcColumn**</span><span class="sxs-lookup"><span data-stu-id="c7caf-132">**columnidcColumn**</span></span>

<span data-ttu-id="c7caf-133">O identificador de coluna do número total de colunas que o índice abrange.</span><span class="sxs-lookup"><span data-stu-id="c7caf-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="c7caf-134">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-135">**columnidiColumn**</span><span class="sxs-lookup"><span data-stu-id="c7caf-135">**columnidiColumn**</span></span>

<span data-ttu-id="c7caf-136">O identificador de coluna do número de colunas no índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="c7caf-137">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c7caf-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="c7caf-138">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7caf-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c7caf-139">Value</span></span></p></th>
<th><p><span data-ttu-id="c7caf-140">Significado</span><span class="sxs-lookup"><span data-stu-id="c7caf-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-141">cIndexInfoCols</span><span class="sxs-lookup"><span data-stu-id="c7caf-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="c7caf-142">15</span><span class="sxs-lookup"><span data-stu-id="c7caf-142">15</span></span></p></td>
<td><p><span data-ttu-id="c7caf-143">Especifica que 15 colunas são permitidas.</span><span class="sxs-lookup"><span data-stu-id="c7caf-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7caf-144">cColumnInfoCols</span><span class="sxs-lookup"><span data-stu-id="c7caf-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="c7caf-145">14</span><span class="sxs-lookup"><span data-stu-id="c7caf-145">14</span></span></p></td>
<td><p><span data-ttu-id="c7caf-146">Especifica que 14 colunas são permitidas.</span><span class="sxs-lookup"><span data-stu-id="c7caf-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-147">cObjectInfoCols</span><span class="sxs-lookup"><span data-stu-id="c7caf-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="c7caf-148">9</span><span class="sxs-lookup"><span data-stu-id="c7caf-148">9</span></span></p></td>
<td><p><span data-ttu-id="c7caf-149">Especifica que são permitidas 9 colunas.</span><span class="sxs-lookup"><span data-stu-id="c7caf-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7caf-150">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="c7caf-150">**columnidcolumnid**</span></span>

<span data-ttu-id="c7caf-151">O identificador de coluna da coluna que é indexada. Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c7caf-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="c7caf-152">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-153">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="c7caf-153">**columnidcoltyp**</span></span>

<span data-ttu-id="c7caf-154">O identificador de coluna do coltyp da coluna que é indexada.</span><span class="sxs-lookup"><span data-stu-id="c7caf-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="c7caf-155">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c7caf-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="c7caf-156">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-157">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="c7caf-157">**columnidCountry**</span></span>

<span data-ttu-id="c7caf-158">O identificador de coluna do código de país da coluna que é indexada.</span><span class="sxs-lookup"><span data-stu-id="c7caf-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="c7caf-159">O código do país é preterido.</span><span class="sxs-lookup"><span data-stu-id="c7caf-159">The country code is deprecated.</span></span>

<span data-ttu-id="c7caf-160">Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-161">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="c7caf-161">**columnidLangid**</span></span>

<span data-ttu-id="c7caf-162">O identificador de coluna do identificador de idioma (LCID) sob o qual o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="c7caf-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="c7caf-163">Para obter mais informações, consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="c7caf-164">Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-165">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="c7caf-165">**columnidCp**</span></span>

<span data-ttu-id="c7caf-166">O identificador de coluna da página de código sob a qual o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="c7caf-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="c7caf-167">Para obter mais informações, consulte [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="c7caf-168">Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-169">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="c7caf-169">**columnidCollate**</span></span>

<span data-ttu-id="c7caf-170">O identificador de coluna da sequência de agrupamento sob a qual o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="c7caf-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="c7caf-171">A sequência de agrupamento foi preterida.</span><span class="sxs-lookup"><span data-stu-id="c7caf-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="c7caf-172">Esta coluna é uma [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-173">**columnidgrbitColumn**</span><span class="sxs-lookup"><span data-stu-id="c7caf-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="c7caf-174">O identificador de coluna do *grbits* que se aplica à ordem da coluna no índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="c7caf-175">Os dados desta coluna podem ser ordenados como JET_bitKeyAscending ou JET_bitKeyDescending.</span><span class="sxs-lookup"><span data-stu-id="c7caf-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="c7caf-176">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="c7caf-177">Por exemplo, um índice definido como "-Coluna1 \\ 0 + Coluna2 \\ 0" terá JET_bitKeyDescending para "Column1" e JET_bitKeyAscending para "Coluna2".</span><span class="sxs-lookup"><span data-stu-id="c7caf-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="c7caf-178">As opções a seguir são válidas para este membro.</span><span class="sxs-lookup"><span data-stu-id="c7caf-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7caf-179">Valor</span><span class="sxs-lookup"><span data-stu-id="c7caf-179">Value</span></span></p></th>
<th><p><span data-ttu-id="c7caf-180">Significado</span><span class="sxs-lookup"><span data-stu-id="c7caf-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="c7caf-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="c7caf-182">Um segmento de índice em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="c7caf-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7caf-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="c7caf-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="c7caf-184">Um segmento de índice em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="c7caf-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7caf-185">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="c7caf-185">**columnidcolumnname**</span></span>

<span data-ttu-id="c7caf-186">O identificador de coluna do nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="c7caf-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="c7caf-187">Esta coluna é uma [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="c7caf-188">**columnidLCMapFlags**</span><span class="sxs-lookup"><span data-stu-id="c7caf-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="c7caf-189">O identificador de coluna dos sinalizadores que são usados para criar o índice.</span><span class="sxs-lookup"><span data-stu-id="c7caf-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="c7caf-190">Para obter mais informações, consulte a seção **dwMapFlags** de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="c7caf-191">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c7caf-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="c7caf-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7caf-192">Remarks</span></span>

<span data-ttu-id="c7caf-193">Cada linha na tabela temporária corresponde a uma coluna em um índice específico.</span><span class="sxs-lookup"><span data-stu-id="c7caf-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="c7caf-194">Por exemplo, o índice "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0" tem mais de cinco colunas e ocupará cinco linhas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="c7caf-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="c7caf-195">Cada uma dessas cinco linhas terá um valor de 5 na coluna identificada pela coluna columnid.</span><span class="sxs-lookup"><span data-stu-id="c7caf-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="c7caf-196">Mas cada linha terá um valor diferente para a coluna columnid, variando de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="c7caf-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="c7caf-197">O número de chaves em um índice específico corresponde ao número de valores exclusivos para os quais um chamador pode buscar e obter uma correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="c7caf-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="c7caf-198">O número de entradas é o número de linhas que um índice corresponde.</span><span class="sxs-lookup"><span data-stu-id="c7caf-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="c7caf-199">Se um índice tiver uma restrição de exclusividade, o número de chaves será igual ao número de entradas.</span><span class="sxs-lookup"><span data-stu-id="c7caf-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="c7caf-200">Por exemplo, se uma tabela contiver as seguintes informações e um índice for criado na coluna chamada "Key", haverá três chaves (100, 200 e 500), mas haverá quatro entradas ("This", "is", "a" e "example").</span><span class="sxs-lookup"><span data-stu-id="c7caf-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7caf-201">Chave</span><span class="sxs-lookup"><span data-stu-id="c7caf-201">Key</span></span></p></th>
<th><p><span data-ttu-id="c7caf-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7caf-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-203">100</span><span class="sxs-lookup"><span data-stu-id="c7caf-203">100</span></span></p></td>
<td><p><span data-ttu-id="c7caf-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="c7caf-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7caf-205">100</span><span class="sxs-lookup"><span data-stu-id="c7caf-205">100</span></span></p></td>
<td><p><span data-ttu-id="c7caf-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="c7caf-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-207">200</span><span class="sxs-lookup"><span data-stu-id="c7caf-207">200</span></span></p></td>
<td><p><span data-ttu-id="c7caf-208">&quot;um&quot;</span><span class="sxs-lookup"><span data-stu-id="c7caf-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7caf-209">500</span><span class="sxs-lookup"><span data-stu-id="c7caf-209">500</span></span></p></td>
<td><p><span data-ttu-id="c7caf-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="c7caf-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c7caf-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7caf-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-212"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c7caf-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c7caf-213">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c7caf-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7caf-214"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c7caf-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c7caf-215">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c7caf-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7caf-216"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c7caf-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c7caf-217">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c7caf-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c7caf-218">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c7caf-218">See Also</span></span>

[<span data-ttu-id="c7caf-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="c7caf-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="c7caf-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="c7caf-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="c7caf-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c7caf-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="c7caf-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c7caf-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c7caf-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c7caf-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c7caf-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="c7caf-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="c7caf-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c7caf-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c7caf-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c7caf-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c7caf-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="c7caf-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="c7caf-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c7caf-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="c7caf-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c7caf-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
