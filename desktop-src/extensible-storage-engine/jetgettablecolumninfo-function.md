---
description: 'Saiba mais sobre: função JetGetTableColumnInfo'
title: Função JetGetTableColumnInfo
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104173227"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="20761-103">Função JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="20761-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="20761-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20761-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="20761-105">Função JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="20761-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="20761-106">A função **JetGetTableColumnInfo** recupera informações sobre uma coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="20761-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="20761-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20761-107">Parameters</span></span>

<span data-ttu-id="20761-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="20761-108">*sesid*</span></span>

<span data-ttu-id="20761-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="20761-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="20761-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="20761-110">*tableid*</span></span>

<span data-ttu-id="20761-111">A tabela que contém a coluna para a qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="20761-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="20761-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="20761-112">*szColumnName*</span></span>

<span data-ttu-id="20761-113">O nome da coluna para a qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="20761-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="20761-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="20761-114">*pvResult*</span></span>

<span data-ttu-id="20761-115">Ponteiro para um buffer que receberá as informações.</span><span class="sxs-lookup"><span data-stu-id="20761-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="20761-116">O tipo do buffer é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="20761-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="20761-117">O chamador deve ser configurado para alinhar o buffer adequadamente.</span><span class="sxs-lookup"><span data-stu-id="20761-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="20761-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="20761-118">*cbMax*</span></span>

<span data-ttu-id="20761-119">O tamanho, em bytes, do buffer que foi passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="20761-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="20761-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="20761-120">*InfoLevel*</span></span>

<span data-ttu-id="20761-121">O tipo de informações que serão recuperadas para a coluna especificada por *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="20761-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="20761-122">O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="20761-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="20761-123">Para o esquema da tabela temporária, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="20761-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="20761-124">JET_ColInfoListSortColumnid classificará a tabela temporária por *columnid*.</span><span class="sxs-lookup"><span data-stu-id="20761-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="20761-125">JET_ColInfoListCompact compactará a saída.</span><span class="sxs-lookup"><span data-stu-id="20761-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="20761-126">Para obter mais informações sobre a saída compacta, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="20761-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="20761-127">As seguintes opções podem ser definidas para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="20761-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20761-128">Valor</span><span class="sxs-lookup"><span data-stu-id="20761-128">Value</span></span></p></th>
<th><p><span data-ttu-id="20761-129">Significado</span><span class="sxs-lookup"><span data-stu-id="20761-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20761-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="20761-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="20761-131"><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e os campos da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> são preenchidos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="20761-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="20761-132">JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="20761-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="20761-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="20761-134"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="20761-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="20761-135">Isso é semelhante a uma estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="20761-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="20761-136">Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="20761-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="20761-137">Se essa função falhar, a estrutura conterá dados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="20761-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="20761-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="20761-139"><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="20761-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="20761-140">JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="20761-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="20761-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="20761-142"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="20761-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="20761-143">Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="20761-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="20761-144">Uma tabela temporária é aberta e identificada pelo membro <em>TableName</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="20761-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="20761-145">A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="20761-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="20761-146">Se essa função falhar, a estrutura conterá dados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="20761-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="20761-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="20761-148"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="20761-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="20761-149">Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="20761-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="20761-150">Uma tabela temporária é aberta e identificada pelo membro <em>TableName</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="20761-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="20761-151">A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="20761-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="20761-152">Se essa função falhar, a estrutura conterá dados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="20761-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="20761-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="20761-154">O mesmo que JET_ColInfoList, no entanto, a tabela resultante é classificada por <em>columnid</em>, em vez do nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="20761-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="20761-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="20761-156">JET_ColInfoSysTabCursor for preterido e o uso dele retornará JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="20761-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="20761-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="20761-158">O mesmo que JET_ColInfoBase, <em>pvResult</em> é interpretado como um <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="20761-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="20761-159"><strong>Windows Vista:  </strong> Isso está disponível no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="20761-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="20761-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="20761-161">Retornar apenas colunas não derivadas (se a tabela for derivada de um modelo).</span><span class="sxs-lookup"><span data-stu-id="20761-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="20761-162">Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="20761-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="20761-163"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20761-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="20761-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="20761-165">Retorna apenas o nome da coluna e columnid de cada coluna.</span><span class="sxs-lookup"><span data-stu-id="20761-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="20761-166">Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="20761-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="20761-167"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20761-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="20761-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="20761-169">Classifique a lista de colunas retornada por ColumnID (o padrão é classificar a lista por nome de coluna).</span><span class="sxs-lookup"><span data-stu-id="20761-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="20761-170">Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="20761-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="20761-171"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20761-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="20761-172">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="20761-172">Return Value</span></span>

<span data-ttu-id="20761-173">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="20761-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="20761-174">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="20761-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20761-175">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="20761-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="20761-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="20761-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20761-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20761-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20761-178">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="20761-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="20761-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="20761-180">A coluna denominada <em>szColumnName</em> não foi encontrada na tabela.</span><span class="sxs-lookup"><span data-stu-id="20761-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="20761-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="20761-182">Um <em>InfoLevel</em> inadequado foi especificado.</span><span class="sxs-lookup"><span data-stu-id="20761-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="20761-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="20761-184">Esse erro pode ser retornado se:</span><span class="sxs-lookup"><span data-stu-id="20761-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="20761-185">Um nome inadequado para <em>szTableName</em> foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="20761-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="20761-186">Um nome inadequado para <em>szColumnName</em> foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="20761-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="20761-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="20761-188">Esse erro pode ser retornado se:</span><span class="sxs-lookup"><span data-stu-id="20761-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="20761-189">Um <em>InfoLevel</em> inadequado foi especificado.</span><span class="sxs-lookup"><span data-stu-id="20761-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="20761-190">Um <em>SZTABLENAME</em> nulo foi passado.</span><span class="sxs-lookup"><span data-stu-id="20761-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="20761-191">O buffer é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="20761-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="20761-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="20761-192">Remarks</span></span>

<span data-ttu-id="20761-193">**JetGetTableColumnInfo** e [JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperam informações sobre uma coluna.</span><span class="sxs-lookup"><span data-stu-id="20761-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="20761-194">A diferença entre eles é como a tabela é identificada:</span><span class="sxs-lookup"><span data-stu-id="20761-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="20761-195">**JetGetTableColumnInfo** identifica uma tabela por *TableName*.</span><span class="sxs-lookup"><span data-stu-id="20761-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="20761-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifica uma tabela pela combinação de *DBID* e *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="20761-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="20761-197">Ao recuperar dados com JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, uma tabela temporária será aberta.</span><span class="sxs-lookup"><span data-stu-id="20761-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="20761-198">A tabela temporária contém dados e a estrutura de [JET_COLUMNLIST](./jet-columnlist-structure.md) contém informações suficientes para atravessar a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="20761-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="20761-199">A tabela temporária deve ser fechada com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="20761-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="20761-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20761-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20761-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="20761-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20761-202">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20761-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-203"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="20761-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20761-204">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20761-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-205"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="20761-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20761-206">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="20761-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-207"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="20761-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20761-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="20761-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20761-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="20761-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20761-210">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="20761-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20761-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="20761-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="20761-212">Implementado como <strong>JetGetTableColumnInfoW</strong> (Unicode) e <strong>JetGetTableColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="20761-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20761-213">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="20761-213">See Also</span></span>

[<span data-ttu-id="20761-214">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="20761-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="20761-215">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="20761-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="20761-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="20761-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="20761-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="20761-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="20761-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="20761-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="20761-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="20761-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="20761-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20761-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20761-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="20761-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="20761-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="20761-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="20761-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="20761-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="20761-224">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="20761-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="20761-225">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="20761-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="20761-226">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="20761-226">JetGetTableColumnInfo</span></span>]()
