---
description: 'Saiba mais sobre: função JetGetTableInfo'
title: Função JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922661"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="823e0-103">Função JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="823e0-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="823e0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="823e0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="823e0-105">Função JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="823e0-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="823e0-106">A função **JetGetTableInfo** recupera várias partes de informações sobre uma tabela em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="823e0-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="823e0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="823e0-107">Parameters</span></span>

<span data-ttu-id="823e0-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="823e0-108">*sesid*</span></span>

<span data-ttu-id="823e0-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="823e0-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="823e0-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="823e0-110">*tableid*</span></span>

<span data-ttu-id="823e0-111">A tabela à qual as informações se aplicam.</span><span class="sxs-lookup"><span data-stu-id="823e0-111">The table that the information applies to.</span></span>

<span data-ttu-id="823e0-112">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="823e0-112">*pvResult*</span></span>

<span data-ttu-id="823e0-113">Ponteiro para um buffer que receberá as informações.</span><span class="sxs-lookup"><span data-stu-id="823e0-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="823e0-114">O tipo do buffer é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="823e0-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="823e0-115">É responsabilidade do chamador alinhar o buffer adequadamente.</span><span class="sxs-lookup"><span data-stu-id="823e0-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="823e0-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="823e0-116">*cbMax*</span></span>

<span data-ttu-id="823e0-117">O tamanho, em bytes, do buffer que foi passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="823e0-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="823e0-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="823e0-118">*InfoLevel*</span></span>

<span data-ttu-id="823e0-119">O tipo de informações que serão recuperadas para a tabela especificada por *TableName*.</span><span class="sxs-lookup"><span data-stu-id="823e0-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="823e0-120">O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="823e0-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="823e0-121">As seguintes opções podem ser definidas para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="823e0-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="823e0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="823e0-122">Value</span></span></p></th>
<th><p><span data-ttu-id="823e0-123">Significado</span><span class="sxs-lookup"><span data-stu-id="823e0-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="823e0-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="823e0-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="823e0-125"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="823e0-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="823e0-126">Se o método tiver sucesso, a estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> será preenchida com os dados apropriados.</span><span class="sxs-lookup"><span data-stu-id="823e0-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="823e0-127">Se falhar, o conteúdo será indefinido.</span><span class="sxs-lookup"><span data-stu-id="823e0-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="823e0-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="823e0-129"><em>pvResult</em> é tratado como uma matriz de dois objetos <a href="gg269248(v=exchg.10).md">JET_DBID</a> .</span><span class="sxs-lookup"><span data-stu-id="823e0-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="823e0-130">O identificador de banco de dados do banco de dados que possui a tabela é armazenado nessa matriz duas vezes.</span><span class="sxs-lookup"><span data-stu-id="823e0-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="823e0-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="823e0-132">JET_TblInfoDumpTable é preterida.</span><span class="sxs-lookup"><span data-stu-id="823e0-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="823e0-133">A API retornará JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="823e0-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="823e0-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="823e0-135">JET_TblInfoName recupera o nome da tabela e a armazena em <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="823e0-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="823e0-136">Se o buffer for muito pequeno, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="823e0-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="823e0-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="823e0-138">JET_TblInfoMostMany recupera o nome da tabela e a armazena em <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="823e0-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="823e0-139">Se o buffer for muito pequeno, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="823e0-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="823e0-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="823e0-141">JET_TblInfoOLC é preterida.</span><span class="sxs-lookup"><span data-stu-id="823e0-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="823e0-142">A API retornará JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="823e0-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="823e0-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="823e0-144">JET_TblInfoRvt é preterida.</span><span class="sxs-lookup"><span data-stu-id="823e0-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="823e0-145">A API retornará JET_errQueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="823e0-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="823e0-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="823e0-147">JET_TblInfoResetOLC é preterida.</span><span class="sxs-lookup"><span data-stu-id="823e0-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="823e0-148">A API retornará JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="823e0-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="823e0-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="823e0-150"><em>pvResult</em> é interpretado como uma matriz de dois ULONGs:</span><span class="sxs-lookup"><span data-stu-id="823e0-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="823e0-151">O primeiro <strong>ULONG</strong> é o número de páginas na tabela.</span><span class="sxs-lookup"><span data-stu-id="823e0-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="823e0-152">O segundo <strong>ULONG</strong> é a densidade de destino das páginas da tabela.</span><span class="sxs-lookup"><span data-stu-id="823e0-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="823e0-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="823e0-154"><em>pvResult</em> é interpretado como um <strong>ULONG</strong>.</span><span class="sxs-lookup"><span data-stu-id="823e0-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="823e0-155">O <strong>ULONG</strong> é a soma do número de páginas que estão disponíveis na tabela, seus índices e a árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="823e0-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="823e0-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="823e0-157"><em>pvResult</em> é interpretado como um <strong>ULONG</strong>.</span><span class="sxs-lookup"><span data-stu-id="823e0-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="823e0-158">O <strong>ULONG</strong> é a soma do número de páginas pertencentes à tabela (incluindo seus índices e a árvore de valor longo e todas as páginas disponíveis aqui).</span><span class="sxs-lookup"><span data-stu-id="823e0-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="823e0-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="823e0-160">O comportamento da API depende do tamanho do buffer que é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="823e0-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="823e0-161">Dois valores de <em>cbMax</em> devem ser pelo menos (2 \* sizeof (ULong)).</span><span class="sxs-lookup"><span data-stu-id="823e0-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="823e0-162">Se <em>cbMax</em> for (2 \* sizeof (ULong)), <em>pvResult</em> será interpretado como uma matriz de dois ULONGs:</span><span class="sxs-lookup"><span data-stu-id="823e0-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="823e0-163">O primeiro <strong>ULONG</strong> é o número de extensões de propriedade da tabela.</span><span class="sxs-lookup"><span data-stu-id="823e0-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="823e0-164">O segundo <strong>ULONG</strong> é o número de extensões disponíveis da tabela.</span><span class="sxs-lookup"><span data-stu-id="823e0-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="823e0-165"><em>pvResult</em> é interpretado como uma matriz de:</span><span class="sxs-lookup"><span data-stu-id="823e0-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="823e0-166">O primeiro <strong>ULONG</strong> é o número de extensões de propriedade da tabela.</span><span class="sxs-lookup"><span data-stu-id="823e0-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="823e0-167">O segundo <strong>ULONG</strong> é o número de extensões disponíveis da tabela.</span><span class="sxs-lookup"><span data-stu-id="823e0-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="823e0-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="823e0-169"><em>pvResult</em> é interpretado como um buffer de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="823e0-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="823e0-170">O buffer deve ser pelo menos JET_cbNameMost + 1, incluindo o <strong>nulo</strong>de terminação.</span><span class="sxs-lookup"><span data-stu-id="823e0-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="823e0-171">Se a tabela for uma tabela derivada, o buffer será preenchido com o nome da tabela da qual a tabela derivada herdou sua DDL.</span><span class="sxs-lookup"><span data-stu-id="823e0-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="823e0-172">Se a tabela não for uma tabela derivada, o buffer será uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="823e0-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="823e0-173">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="823e0-173">Return Value</span></span>

<span data-ttu-id="823e0-174">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="823e0-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="823e0-175">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="823e0-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="823e0-176">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="823e0-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="823e0-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="823e0-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="823e0-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="823e0-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="823e0-179">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="823e0-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="823e0-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="823e0-181">O buffer era muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="823e0-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="823e0-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="823e0-183">Foi especificado um <em>InfoLevel</em> preterido.</span><span class="sxs-lookup"><span data-stu-id="823e0-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="823e0-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="823e0-185">O buffer não era o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="823e0-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="823e0-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="823e0-187">A tabela que foi passada era uma tabela temporária e o <em>InfoLevel</em> solicitado não pode ser recuperado para uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="823e0-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="823e0-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="823e0-189">A tabela que foi passada era uma tabela temporária e o <em>InfoLevel</em> solicitado não pode ser recuperado para uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="823e0-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="823e0-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="823e0-191">Não há suporte para o <em>InfoLevel</em> .</span><span class="sxs-lookup"><span data-stu-id="823e0-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="823e0-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="823e0-193">A tabela está sendo usada por outra operação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="823e0-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="823e0-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="823e0-195">A tabela está bloqueada por outra operação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="823e0-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="823e0-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="823e0-197">A tabela está sendo usada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="823e0-197">The table is being used by the system.</span></span> <span data-ttu-id="823e0-198">Este aviso é não fatal.</span><span class="sxs-lookup"><span data-stu-id="823e0-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="823e0-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="823e0-199">Remarks</span></span>

<span data-ttu-id="823e0-200">Algumas informações não são válidas para tabelas temporárias (consulte [JetOpenTempTable](./jetopentemptable-function.md)).</span><span class="sxs-lookup"><span data-stu-id="823e0-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="823e0-201">As estatísticas de tabela incluem o número de registros e o número de páginas no índice clusterizado (ou seja, o índice que contém os dados de registro).</span><span class="sxs-lookup"><span data-stu-id="823e0-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="823e0-202">As estatísticas de índice são acessadas separadamente por nome, usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="823e0-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="823e0-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="823e0-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="823e0-204"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="823e0-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="823e0-205">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="823e0-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-206"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="823e0-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="823e0-207">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="823e0-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-208"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="823e0-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="823e0-209">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="823e0-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-210"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="823e0-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="823e0-211">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="823e0-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823e0-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="823e0-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="823e0-213">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="823e0-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823e0-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="823e0-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="823e0-215">Implementado como <strong>JetGetTableInfoW</strong> (Unicode) e <strong>JetGetTableInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="823e0-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="823e0-216">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="823e0-216">See Also</span></span>

[<span data-ttu-id="823e0-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="823e0-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="823e0-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="823e0-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="823e0-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="823e0-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="823e0-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="823e0-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="823e0-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="823e0-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="823e0-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="823e0-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="823e0-223">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="823e0-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="823e0-224">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="823e0-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="823e0-225">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="823e0-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
