---
description: 'Saiba mais sobre: função JetGetColumnInfo'
title: Função JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771435"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="8acb6-103">Função JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="8acb6-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="8acb6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8acb6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="8acb6-105">Função JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="8acb6-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="8acb6-106">A função **JetGetColumnInfo** recupera informações sobre uma coluna.</span><span class="sxs-lookup"><span data-stu-id="8acb6-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="8acb6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8acb6-107">Parameters</span></span>

<span data-ttu-id="8acb6-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8acb6-108">*sesid*</span></span>

<span data-ttu-id="8acb6-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="8acb6-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="8acb6-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="8acb6-110">*dbid*</span></span>

<span data-ttu-id="8acb6-111">Identifica, juntamente com *szTableName*, a tabela que contém a coluna da qual as informações são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="8acb6-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="8acb6-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="8acb6-112">*szTableName*</span></span>

<span data-ttu-id="8acb6-113">Identifica, juntamente com *DBID*, a tabela que contém a coluna da qual as informações são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="8acb6-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="8acb6-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="8acb6-114">*szColumnName*</span></span>

<span data-ttu-id="8acb6-115">O nome da coluna para a qual as informações são buscadas.</span><span class="sxs-lookup"><span data-stu-id="8acb6-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="8acb6-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="8acb6-116">*pvResult*</span></span>

<span data-ttu-id="8acb6-117">Ponteiro para um buffer que receberá as informações.</span><span class="sxs-lookup"><span data-stu-id="8acb6-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="8acb6-118">O tipo do buffer é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="8acb6-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="8acb6-119">O chamador deve ser configurado para alinhar o buffer adequadamente.</span><span class="sxs-lookup"><span data-stu-id="8acb6-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="8acb6-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="8acb6-120">*cbMax*</span></span>

<span data-ttu-id="8acb6-121">O tamanho, em bytes, do buffer que é passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="8acb6-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="8acb6-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="8acb6-122">*InfoLevel*</span></span>

<span data-ttu-id="8acb6-123">O tipo de informações a serem recuperadas para a coluna especificada por *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="8acb6-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="8acb6-124">O formato dos dados armazenados em *pvResult* depende desse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8acb6-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="8acb6-125">Para o esquema da tabela temporária, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="8acb6-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="8acb6-126">Esses *InfoLevels* são diferenciados por:</span><span class="sxs-lookup"><span data-stu-id="8acb6-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="8acb6-127">JET_ColInfoListSortColumnid classificará a tabela temporária por *columnid*.</span><span class="sxs-lookup"><span data-stu-id="8acb6-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="8acb6-128">JET_ColInfoListCompact compactará a saída.</span><span class="sxs-lookup"><span data-stu-id="8acb6-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="8acb6-129">Para obter mais informações sobre a saída compacta, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="8acb6-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="8acb6-130">As opções a seguir estão disponíveis para uso com esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8acb6-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8acb6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8acb6-131">Value</span></span></p></th>
<th><p><span data-ttu-id="8acb6-132">Significado</span><span class="sxs-lookup"><span data-stu-id="8acb6-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="8acb6-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="8acb6-134">JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="8acb6-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="8acb6-135"><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e os campos da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> são preenchidos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="8acb6-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="8acb6-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="8acb6-137"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="8acb6-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="8acb6-138">Isso é semelhante a uma estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="8acb6-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="8acb6-139">Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="8acb6-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="8acb6-140">Se essa função falhar, a estrutura conterá dados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="8acb6-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="8acb6-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="8acb6-142">Assim como JET_ColInfo, <em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="8acb6-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="8acb6-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="8acb6-144"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="8acb6-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="8acb6-145">Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="8acb6-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="8acb6-146">Uma tabela temporária é aberta e identificada pelo membro <strong>TableName</strong> da estrutura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="8acb6-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="8acb6-147">A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="8acb6-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="8acb6-148">Se essa função falhar, a estrutura conterá dados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="8acb6-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="8acb6-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="8acb6-150">O mesmo que JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="8acb6-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="8acb6-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="8acb6-152">O mesmo que JET_ColInfoList; no entanto, a tabela resultante é classificada por columnid, em vez de nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="8acb6-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="8acb6-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="8acb6-154">JET_ColInfoSysTabCursor for preterido e o uso dele retornará JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="8acb6-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="8acb6-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="8acb6-156">Assim como JET_ColInfoBase, <em>pvResult</em> é interpretado como um <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="8acb6-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="8acb6-157"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8acb6-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="8acb6-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="8acb6-159">Retornar apenas colunas não derivadas (se a tabela for derivada de um modelo).</span><span class="sxs-lookup"><span data-stu-id="8acb6-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="8acb6-160">Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="8acb6-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="8acb6-161"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8acb6-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="8acb6-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="8acb6-163">Retorna apenas o nome da coluna e columnid de cada coluna.</span><span class="sxs-lookup"><span data-stu-id="8acb6-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="8acb6-164">Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="8acb6-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="8acb6-165"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8acb6-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="8acb6-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="8acb6-167">Classifique a lista de colunas retornada por ColumnID (o padrão é classificar a lista por nome de coluna).</span><span class="sxs-lookup"><span data-stu-id="8acb6-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="8acb6-168">Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="8acb6-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="8acb6-169"><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8acb6-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8acb6-170">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8acb6-170">Return Value</span></span>

<span data-ttu-id="8acb6-171">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="8acb6-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8acb6-172">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8acb6-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8acb6-173">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8acb6-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="8acb6-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="8acb6-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8acb6-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8acb6-176">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8acb6-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="8acb6-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="8acb6-178">A coluna denominada <em>szColumnName</em> não foi encontrada na tabela.</span><span class="sxs-lookup"><span data-stu-id="8acb6-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="8acb6-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="8acb6-180">Um <em>InfoLevel</em> inadequado foi especificado.</span><span class="sxs-lookup"><span data-stu-id="8acb6-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="8acb6-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="8acb6-182">Esse erro pode ser retornado se:</span><span class="sxs-lookup"><span data-stu-id="8acb6-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="8acb6-183">Um nome inadequado para <em>szTableName</em> foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="8acb6-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="8acb6-184">Um nome inadequado para <em>szColumnName</em> foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="8acb6-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8acb6-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8acb6-186">Esse erro pode ser retornado se:</span><span class="sxs-lookup"><span data-stu-id="8acb6-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="8acb6-187">Um <em>InfoLevel</em> inadequado foi especificado.</span><span class="sxs-lookup"><span data-stu-id="8acb6-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="8acb6-188">Um <em>SZTABLENAME</em> nulo foi passado.</span><span class="sxs-lookup"><span data-stu-id="8acb6-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="8acb6-189">O buffer é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="8acb6-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="8acb6-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="8acb6-190">Remarks</span></span>

<span data-ttu-id="8acb6-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) e **JetGetColumnInfo** recuperam informações sobre uma coluna.</span><span class="sxs-lookup"><span data-stu-id="8acb6-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="8acb6-192">A diferença entre eles é como a tabela é identificada:</span><span class="sxs-lookup"><span data-stu-id="8acb6-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="8acb6-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica uma tabela por *TableName*.</span><span class="sxs-lookup"><span data-stu-id="8acb6-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="8acb6-194">**JetGetColumnInfo** identifica uma tabela pela combinação de *DBID* e *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="8acb6-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="8acb6-195">Ao recuperar dados com JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, uma tabela temporária será aberta.</span><span class="sxs-lookup"><span data-stu-id="8acb6-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="8acb6-196">A tabela temporária contém dados e a estrutura de [JET_COLUMNLIST](./jet-columnlist-structure.md) contém informações suficientes para atravessar a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="8acb6-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="8acb6-197">A tabela temporária deve ser fechada com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="8acb6-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="8acb6-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8acb6-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-199"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8acb6-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8acb6-200">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8acb6-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-201"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="8acb6-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8acb6-202">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8acb6-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-203"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="8acb6-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8acb6-204">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8acb6-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-205"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="8acb6-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8acb6-206">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8acb6-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acb6-207"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8acb6-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8acb6-208">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8acb6-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acb6-209"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8acb6-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8acb6-210">Implementado como <strong>JetGetColumnInfoW</strong> (Unicode) e <strong>JetGetColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8acb6-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8acb6-211">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8acb6-211">See Also</span></span>

[<span data-ttu-id="8acb6-212">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="8acb6-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="8acb6-213">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="8acb6-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="8acb6-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="8acb6-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="8acb6-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="8acb6-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="8acb6-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="8acb6-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="8acb6-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="8acb6-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="8acb6-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8acb6-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8acb6-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8acb6-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8acb6-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8acb6-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8acb6-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8acb6-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8acb6-222">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="8acb6-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="8acb6-223">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="8acb6-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
