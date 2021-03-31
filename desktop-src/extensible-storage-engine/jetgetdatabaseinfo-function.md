---
description: 'Saiba mais sobre: função JetGetDatabaseInfo'
title: Função JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169784"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="3b3f0-103">Função JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="3b3f0-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="3b3f0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b3f0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="3b3f0-105">Função JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="3b3f0-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="3b3f0-106">A função **JetGetDatabaseInfo** recupera vários tipos de informações sobre o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="3b3f0-107">Essa API pode ser chamada enquanto um banco de dados estiver anexado ou online (com **JetGetDatabaseInfo**) ou enquanto o banco de dados ou o mecanismo de banco de dados estiver offline (com [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="3b3f0-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="3b3f0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b3f0-108">Parameters</span></span>

<span data-ttu-id="3b3f0-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3b3f0-109">*sesid*</span></span>

<span data-ttu-id="3b3f0-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-110">The session to use for this call.</span></span>

<span data-ttu-id="3b3f0-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="3b3f0-111">*dbid*</span></span>

<span data-ttu-id="3b3f0-112">O [JET_DBID](./jet-dbid.md) do banco de dados do qual recuperar as informações.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="3b3f0-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="3b3f0-113">*pvResult*</span></span>

<span data-ttu-id="3b3f0-114">Ponteiro para um buffer que receberá as informações especificadas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="3b3f0-115">O tamanho do buffer, em bytes, é passado em *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="3b3f0-116">Em caso de falha, o conteúdo de *pvResult* é indefinido.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="3b3f0-117">As informações armazenadas no *pvResult* dependem do *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="3b3f0-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="3b3f0-118">*cbMax*</span></span>

<span data-ttu-id="3b3f0-119">O tamanho, em bytes, do buffer que foi passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="3b3f0-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="3b3f0-120">*InfoLevel*</span></span>

<span data-ttu-id="3b3f0-121">*InfoLevel* especifica que tipo de informações devem ser recuperadas sobre o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="3b3f0-122">Ele afeta como o *pvResult* é interpretado.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="3b3f0-123">Alguns *InfoLevel* estão disponíveis somente na versão offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) ou online (**JetGetDatabaseInfo**) da API.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="3b3f0-124">Se o buffer *pvResult* fornecido for muito pequeno, JET_errInvalidBufferSize ou JET_errBufferTooSmall serão retornados, dependendo do *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b3f0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3b3f0-125">Value</span></span></p></th>
<th><p><span data-ttu-id="3b3f0-126">Significado</span><span class="sxs-lookup"><span data-stu-id="3b3f0-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="3b3f0-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-128">Ainda não tem suporte e retorna valores padrão.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-128">Not yet supported and return default values.</span></span> <span data-ttu-id="3b3f0-129">Não use.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="3b3f0-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-131">Esses <em>InfoLevels</em> foram preteridos e não têm suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="3b3f0-132">Não use.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="3b3f0-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-134">Ainda não tem suporte e retorna valores padrão.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-134">Not yet supported and return default values.</span></span> <span data-ttu-id="3b3f0-135">Não use.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="3b3f0-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-137">Ainda não tem suporte e retorna valores padrão.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-137">Not yet supported and return default values.</span></span> <span data-ttu-id="3b3f0-138">Não use.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="3b3f0-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-140"><em>pvResult</em> será interpretado como um buffer de cadeia de caracteres (Char \*).</span><span class="sxs-lookup"><span data-stu-id="3b3f0-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="3b3f0-141">Um buffer de MAX_PATH é sugerido, porém não obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="3b3f0-142">Se o buffer não for longo o suficiente, JET_errBufferTooSmall será retornado.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="3b3f0-143">A cadeia de caracteres será populada com o caminho do banco de dados para esta DBID.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="3b3f0-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-145"><em>pvResult</em> será interpretado como um DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="3b3f0-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="3b3f0-146">Retorna o tamanho do banco de dados em páginas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="3b3f0-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-148">Esses <em>InfoLevels</em> foram preteridos e não têm suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="3b3f0-149">Não use.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="3b3f0-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-151">(Windows XP e posterior) Este <em>InfoLevel</em> foi originalmente especificado como: JET_DbInfoLangid (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="3b3f0-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="3b3f0-152"><em>pvResult</em> será interpretado como um longo.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="3b3f0-153">Isso retorna o LCID (identificador de localidade) associado a este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="3b3f0-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-155"><em>pvResult</em> será interpretado como um <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="3b3f0-156">A estrutura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> será preenchida com informações relacionadas ao banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="3b3f0-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-158"><em>pvResult</em> será interpretado como um <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span><span class="sxs-lookup"><span data-stu-id="3b3f0-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="3b3f0-159">Isso retorna se o banco de dados está aberto em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="3b3f0-160">Se o banco de dados estiver em modo exclusivo JET_bitDbExclusive será definido no <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fornecido, caso contrário, zero será definido.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="3b3f0-161">Observe que outras opções de <em>grbit</em> de banco de dados para <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> e <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="3b3f0-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-163">Disponível apenas no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="3b3f0-164"><em>pvResult</em> será interpretado como um longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="3b3f0-165">Isso retornará o tamanho da página do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="3b3f0-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-167"><em>pvResult</em> será interpretado como um DWORD.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="3b3f0-168">Isso retorna o espaço disponível para o banco de dados em páginas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="3b3f0-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-170"><em>pvResult</em> será interpretado como um DWORD.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="3b3f0-171">Isso retorna o espaço de Propriedade do banco de dados em páginas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="3b3f0-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-173"><em>pvResult</em> será interpretado como um longo.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="3b3f0-174">Isso retornará um maior que o nível máximo para o qual as transações podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="3b3f0-175">Se <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for chamado (em um modo de aninhamento, ou seja, na mesma sessão, sem uma confirmação ou reversão) quantas vezes esse valor, na última chamada JET_errTransTooDeep será retornado de <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="3b3f0-176">Observe que o valor no Windows 2000, no Windows XP e no Windows Server 2003 é 7.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="3b3f0-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-178"><em>pvResult</em> será interpretado como um longo.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="3b3f0-179">Isso retorna a versão principal nativa do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="3b3f0-180">Esse valor é 0x620 para Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3b3f0-181">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3b3f0-181">Return Value</span></span>

<span data-ttu-id="3b3f0-182">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3b3f0-183">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b3f0-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b3f0-184">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b3f0-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b3f0-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b3f0-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b3f0-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-187">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="3b3f0-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-189">O tamanho do buffer fornecido em <em>cbMax</em> era muito pequeno (ou não está correto) para manter as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="3b3f0-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-191">O <em>InfoLevel</em> solicitado foi JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="3b3f0-192">Isso não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="3b3f0-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-194">O tamanho do buffer fornecido em <em>cbMax</em> era muito pequeno (ou não está correto) para manter as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3b3f0-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3b3f0-196">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="3b3f0-197">Esse erro será retornado por <strong>JetGetDatabaseInfo</strong> quando o <a href="gg269248(v=exchg.10).md">JET_DBID</a> fornecido não for um banco de dados (anexado) válido.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="3b3f0-198">Esse erro será retornado por <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> e <strong>JetGetDatabaseInfo</strong> quando um <em>InfoLevel</em> solicitado não for suportado por essa versão da função.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b3f0-199">Em caso de sucesso, os dados solicitados serão retornados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="3b3f0-200">Em caso de falha, o buffer de saída estará em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b3f0-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b3f0-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3b3f0-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b3f0-203">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-204"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3b3f0-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b3f0-205">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-206"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3b3f0-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b3f0-207">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-208"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3b3f0-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b3f0-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b3f0-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b3f0-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b3f0-211">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b3f0-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b3f0-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3b3f0-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3b3f0-213">Implementado como <strong>JetGetDatabaseInfoW</strong> (Unicode) e <strong>JetGetDatabaseInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3b3f0-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b3f0-214">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3b3f0-214">See Also</span></span>

[<span data-ttu-id="3b3f0-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="3b3f0-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="3b3f0-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b3f0-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b3f0-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3b3f0-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3b3f0-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3b3f0-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3b3f0-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="3b3f0-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="3b3f0-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="3b3f0-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="3b3f0-221">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="3b3f0-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
