---
description: 'Saiba mais sobre: função JetGetDatabaseFileInfo'
title: Função JetGetDatabaseFileInfo
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755743"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="94d74-103">Função JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="94d74-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="94d74-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="94d74-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="94d74-105">Função JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="94d74-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="94d74-106">A função **JetGetDatabaseFileInfo** recupera vários tipos de informações sobre o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="94d74-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="94d74-107">Essa API pode ser chamada enquanto um banco de dados estiver anexado ou online (com [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) ou enquanto o banco de dados ou o mecanismo de banco de dados estiver offline (com **JetGetDatabaseFileInfo**).</span><span class="sxs-lookup"><span data-stu-id="94d74-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="94d74-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94d74-108">Parameters</span></span>

<span data-ttu-id="94d74-109">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="94d74-109">*szDatabaseName*</span></span>

<span data-ttu-id="94d74-110">O caminho do banco de dados do qual recuperar as informações.</span><span class="sxs-lookup"><span data-stu-id="94d74-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="94d74-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="94d74-111">*pvResult*</span></span>

<span data-ttu-id="94d74-112">Ponteiro para um buffer que receberá as informações especificadas.</span><span class="sxs-lookup"><span data-stu-id="94d74-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="94d74-113">O tamanho do buffer, em bytes, é passado em *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="94d74-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="94d74-114">Se essa função falhar, o conteúdo de *pvResult* será indefinido.</span><span class="sxs-lookup"><span data-stu-id="94d74-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="94d74-115">As informações armazenadas no *pvResult* dependem do *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="94d74-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="94d74-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="94d74-116">*cbMax*</span></span>

<span data-ttu-id="94d74-117">O tamanho, em bytes, do buffer passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="94d74-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="94d74-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="94d74-118">*InfoLevel*</span></span>

<span data-ttu-id="94d74-119">*InfoLevel* especifica que tipo de informações devem ser recuperadas sobre o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="94d74-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="94d74-120">Ele afeta como o *pvResult* é interpretado.</span><span class="sxs-lookup"><span data-stu-id="94d74-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="94d74-121">Alguns objetos *InfoLevel* estão disponíveis somente na versão offline (**JetGetDatabaseFileInfo**) ou online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) da API.</span><span class="sxs-lookup"><span data-stu-id="94d74-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="94d74-122">Se o buffer *pvResult* fornecido for muito pequeno, JET_errInvalidBufferSize ou JET_errBufferTooSmall serão retornados, dependendo do *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="94d74-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94d74-123">Valor</span><span class="sxs-lookup"><span data-stu-id="94d74-123">Value</span></span></p></th>
<th><p><span data-ttu-id="94d74-124">Significado</span><span class="sxs-lookup"><span data-stu-id="94d74-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94d74-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="94d74-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="94d74-126"><em>pvResult</em> será interpretado como um QWORD (8 bytes).</span><span class="sxs-lookup"><span data-stu-id="94d74-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="94d74-127">Retorna o tamanho do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="94d74-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="94d74-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="94d74-129"><em>pvResult</em> será interpretado como um <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span><span class="sxs-lookup"><span data-stu-id="94d74-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="94d74-130">A estrutura de <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> será preenchida com informações referentes ao banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="94d74-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="94d74-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="94d74-132"><em>pvResult</em> será interpretado como um <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="94d74-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="94d74-133">A estrutura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> será preenchida com informações referentes ao banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="94d74-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="94d74-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="94d74-135"><em>pvResult</em> será interpretado como um bool (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="94d74-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="94d74-136">Isso retornará se o mecanismo de banco de dados tem, no momento, qualquer banco de dados aberto ou anexado.</span><span class="sxs-lookup"><span data-stu-id="94d74-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="94d74-137"><strong>Windows XP:  </strong> Esse valor é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="94d74-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="94d74-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="94d74-139"><em>pvResult</em> será interpretado como um longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="94d74-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="94d74-140">Isso retornará o tamanho da página do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="94d74-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="94d74-141"><strong>Windows XP:  </strong> Esse valor é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="94d74-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="94d74-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="94d74-143">Esses <em>InfoLevels</em> ainda não têm suporte e retornam valores padrão.</span><span class="sxs-lookup"><span data-stu-id="94d74-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="94d74-144">Não use esses <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="94d74-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="94d74-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="94d74-146">Esses <em>InfoLevels</em> ainda não têm suporte e retornam valores padrão.</span><span class="sxs-lookup"><span data-stu-id="94d74-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="94d74-147">Não use esses <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="94d74-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="94d74-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="94d74-149">O mesmo que JET_DbInfoCp.</span><span class="sxs-lookup"><span data-stu-id="94d74-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="94d74-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="94d74-151">Esses <em>InfoLevels</em> foram preteridos e não têm suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="94d74-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="94d74-152">Não use esses <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="94d74-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="94d74-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="94d74-154">O mesmo que JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="94d74-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="94d74-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="94d74-156"><strong>Windows Vista:  </strong> Esse valor de <em>InfoLevel</em> é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94d74-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="94d74-157"><em>pvResult</em> será tratado como um ponteiro para um DWORD.</span><span class="sxs-lookup"><span data-stu-id="94d74-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="94d74-158">Retorna um valor de enumeração, indicando que tipo de arquivo o mecanismo considera isso.</span><span class="sxs-lookup"><span data-stu-id="94d74-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="94d74-159">Os tipos de arquivo são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="94d74-159">File types are listed in the following table.</span></span> <span data-ttu-id="94d74-160">Para obter mais informações sobre esses tipos de arquivos e seu uso para o mecanismo, consulte <a href="gg294069(v=exchg.10).md">arquivos do mecanismo de armazenamento extensível</a>.</span><span class="sxs-lookup"><span data-stu-id="94d74-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94d74-161">Valor</span><span class="sxs-lookup"><span data-stu-id="94d74-161">Value</span></span></p></th>
<th><p><span data-ttu-id="94d74-162">Significado</span><span class="sxs-lookup"><span data-stu-id="94d74-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94d74-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="94d74-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="94d74-164">O tipo de arquivo é desconhecido ou não é um tipo de arquivo ESE.</span><span class="sxs-lookup"><span data-stu-id="94d74-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="94d74-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="94d74-166">O arquivo é um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="94d74-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="94d74-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="94d74-168">O arquivo é um arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="94d74-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="94d74-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="94d74-170">O arquivo é um arquivo de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="94d74-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="94d74-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="94d74-172">O arquivo é um arquivo de banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="94d74-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="94d74-173">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="94d74-173">Return Value</span></span>

<span data-ttu-id="94d74-174">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="94d74-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="94d74-175">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="94d74-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94d74-176">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="94d74-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="94d74-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="94d74-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94d74-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="94d74-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="94d74-179">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="94d74-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="94d74-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="94d74-181">O <em>InfoLevel</em> solicitado foi JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="94d74-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="94d74-182">Isso não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="94d74-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="94d74-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="94d74-184">O buffer fornecido em <em>cbMax</em> é muito pequeno para as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="94d74-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="94d74-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="94d74-186">O buffer fornecido em <em>cbMax</em> não é o tamanho correto para as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="94d74-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="94d74-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="94d74-188">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="94d74-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="94d74-189">Esse erro será retornado por <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando a DBID fornecida não for um banco de dados válido (anexado).</span><span class="sxs-lookup"><span data-stu-id="94d74-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="94d74-190">Esse erro será retornado por <strong>JetGetDatabaseFileInfo</strong> e <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando um <em>InfoLevel</em> solicitado não for suportado por essa versão da função.</span><span class="sxs-lookup"><span data-stu-id="94d74-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="94d74-191">Se essa função for realizada com sucesso, os dados solicitados serão retornados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="94d74-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="94d74-192">Se essa função falhar, o buffer de saída estará em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="94d74-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="94d74-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d74-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94d74-194"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="94d74-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="94d74-195">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="94d74-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-196"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="94d74-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="94d74-197">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="94d74-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-198"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="94d74-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="94d74-199">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="94d74-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-200"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="94d74-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="94d74-201">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="94d74-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d74-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="94d74-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="94d74-203">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="94d74-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d74-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="94d74-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="94d74-205">Implementado como <strong>JetGetDatabaseFileInfoW</strong> (Unicode) e <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="94d74-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="94d74-206">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="94d74-206">See Also</span></span>

[<span data-ttu-id="94d74-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="94d74-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="94d74-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="94d74-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="94d74-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="94d74-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="94d74-210">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="94d74-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
