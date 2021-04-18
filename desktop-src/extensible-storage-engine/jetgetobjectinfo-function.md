---
description: 'Saiba mais sobre: função JetGetObjectInfo'
title: Função JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798095"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="d32ce-103">Função JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="d32ce-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="d32ce-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d32ce-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="d32ce-105">Função JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="d32ce-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="d32ce-106">A função **JetGetObjectInfo** recupera informações sobre objetos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d32ce-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="d32ce-107">Atualmente, há suporte apenas para tabelas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-107">Currently, only tables are supported.</span></span> <span data-ttu-id="d32ce-108">[JetGetTableInfo](./jetgettableinfo-function.md) pode ser usado para buscar mais informações do que **JetGetObjectInfo**.</span><span class="sxs-lookup"><span data-stu-id="d32ce-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="d32ce-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d32ce-109">Parameters</span></span>

<span data-ttu-id="d32ce-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d32ce-110">*sesid*</span></span>

<span data-ttu-id="d32ce-111">O contexto da sessão de banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d32ce-111">The database session context to use.</span></span>

<span data-ttu-id="d32ce-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="d32ce-112">*dbid*</span></span>

<span data-ttu-id="d32ce-113">O banco de dados do qual as informações são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="d32ce-114">*objtyp*</span><span class="sxs-lookup"><span data-stu-id="d32ce-114">*objtyp*</span></span>

<span data-ttu-id="d32ce-115">Os objetos que contêm informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="d32ce-116">Atualmente, há suporte apenas para JET_objtypNil e JET_objtypTable, os quais se comportam de forma idêntica.</span><span class="sxs-lookup"><span data-stu-id="d32ce-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="d32ce-117">Somente tabelas serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="d32ce-118">*szContainerName*</span><span class="sxs-lookup"><span data-stu-id="d32ce-118">*szContainerName*</span></span>

<span data-ttu-id="d32ce-119">Esse parâmetro é reservado para uso futuro e passa **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d32ce-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="d32ce-120">O nome dos tipos de objetos sobre os quais recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="d32ce-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="d32ce-121">*szObjectName*</span><span class="sxs-lookup"><span data-stu-id="d32ce-121">*szObjectName*</span></span>

<span data-ttu-id="d32ce-122">O nome do objeto que contém informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="d32ce-123">Quando *InfoLevel* usa as opções JET_ObjInfoList ou JET_ObjInfoListNoStats para recuperar uma lista de todos os objetos, esse valor deve ser **nulo** ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="d32ce-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="d32ce-124">Somente os nomes de tabela têm suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="d32ce-124">Only table names are currently supported.</span></span>

<span data-ttu-id="d32ce-125">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="d32ce-125">*pvResult*</span></span>

<span data-ttu-id="d32ce-126">Ponteiro para um buffer que recebe as informações especificadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="d32ce-127">O tamanho do buffer, em bytes, é passado em *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="d32ce-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="d32ce-128">Em caso de falha, o conteúdo de *pvResult* é indefinido.</span><span class="sxs-lookup"><span data-stu-id="d32ce-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="d32ce-129">As informações armazenadas no *pvResult* dependem do *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="d32ce-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="d32ce-130">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="d32ce-130">*cbMax*</span></span>

<span data-ttu-id="d32ce-131">O tamanho, em bytes, do buffer passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="d32ce-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="d32ce-132">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="d32ce-132">*InfoLevel*</span></span>

<span data-ttu-id="d32ce-133">Especifica o tipo de informações a serem recuperadas para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d32ce-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="d32ce-134">Ele afeta como o *pvResult* é interpretado.</span><span class="sxs-lookup"><span data-stu-id="d32ce-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="d32ce-135">As opções a seguir estão disponíveis para serem definidas para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d32ce-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d32ce-136">Valor</span><span class="sxs-lookup"><span data-stu-id="d32ce-136">Value</span></span></p></th>
<th><p><span data-ttu-id="d32ce-137">Significado</span><span class="sxs-lookup"><span data-stu-id="d32ce-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="d32ce-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="d32ce-139"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="d32ce-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="d32ce-140">A estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> é preenchida com informações referentes ao objeto nomeado em <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="d32ce-141">Se o chamador não quiser saber o número de registros e páginas do objeto, considere usar JET_ObjInfoNoStats nível de informações, o que pode ser mais rápido, pois as estatísticas não são incluídas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="d32ce-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="d32ce-143"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="d32ce-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="d32ce-144">As informações sobre todos os objetos são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="d32ce-145">Uma tabela temporária será criada e as informações necessárias para atravessar a tabela temporária serão descritas na estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="d32ce-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="d32ce-146">Para obter mais informações, consulte <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="d32ce-147">Se o chamador não quiser saber o número de registros e páginas do objeto, considere o uso de JET_ObjInfoListNoStats, que pode ser mais rápido.</span><span class="sxs-lookup"><span data-stu-id="d32ce-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="d32ce-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="d32ce-149">Preterido e não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="d32ce-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="d32ce-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="d32ce-151"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="d32ce-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="d32ce-152">As informações sobre todos os objetos são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="d32ce-153">Uma tabela temporária será criada e as informações necessárias para atravessar a tabela temporária serão descritas na estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="d32ce-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="d32ce-154">Para obter mais informações, consulte <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="d32ce-155">JET_ObjInfoListNoStats é idêntico a JET_ObjInfoList, exceto que as colunas que relatam o número de registros (<em>columnidcRecord</em>) e as páginas (<em>columnidcPage</em>) não serão atualizadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="d32ce-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="d32ce-157"><em>pvResult</em> é interpretado como um <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="d32ce-158">O tamanho máximo do objeto está em páginas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="d32ce-159">No momento, apenas tabelas serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="d32ce-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="d32ce-161"><em>pvResult</em> é interpretado como um <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="d32ce-162">Informações sobre apenas o objeto fornecido em <em>szObjectName</em> serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="d32ce-163">A estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> será preenchida com informações referentes ao objeto nomeado em <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="d32ce-164">JET_ObjInfoNoStats é idêntico a JET_ObjInfo, exceto que os campos que relatam o número de registros e páginas são definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="d32ce-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="d32ce-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="d32ce-166">Preterido e não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="d32ce-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="d32ce-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="d32ce-168">Preterido e não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="d32ce-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="d32ce-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="d32ce-170">Preterido e não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="d32ce-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d32ce-171">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d32ce-171">Return Value</span></span>

<span data-ttu-id="d32ce-172">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d32ce-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d32ce-173">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d32ce-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d32ce-174">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d32ce-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="d32ce-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="d32ce-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d32ce-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d32ce-177">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d32ce-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d32ce-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="d32ce-179">O tamanho do buffer fornecido em <em>cbMax</em> era muito pequeno para conter as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="d32ce-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="d32ce-181">Um nome inválido foi fornecido em <em>szObjectName</em> ou <em>szContainerName</em>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d32ce-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d32ce-183">Um parâmetro inadequado foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="d32ce-183">A bad parameter was given.</span></span> <span data-ttu-id="d32ce-184">É possível que um nível inadequado seja passado para <em>InfoLevel</em>.</span><span class="sxs-lookup"><span data-stu-id="d32ce-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d32ce-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="d32ce-185">Remarks</span></span>

<span data-ttu-id="d32ce-186">Se **JetGetObjectInfo** criar com êxito uma tabela temporária (por exemplo, JET_ObjInfoList ou JET_ObjInfoNoStats), o chamador será responsável por fechar a tabela temporária com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="d32ce-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="d32ce-187">Atualmente, o **JetGetObjectInfo** dá suporte apenas à recuperação de informações sobre tabelas.</span><span class="sxs-lookup"><span data-stu-id="d32ce-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d32ce-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d32ce-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-189"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d32ce-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d32ce-190">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d32ce-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-191"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d32ce-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d32ce-192">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d32ce-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-193"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d32ce-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d32ce-194">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d32ce-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-195"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d32ce-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d32ce-196">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d32ce-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32ce-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d32ce-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d32ce-198">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d32ce-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32ce-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d32ce-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d32ce-200">Implementado como <strong>JetGetObjectInfoW</strong> (Unicode) e <strong>JetGetObjectInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d32ce-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d32ce-201">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d32ce-201">See Also</span></span>

[<span data-ttu-id="d32ce-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d32ce-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d32ce-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d32ce-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d32ce-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="d32ce-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="d32ce-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d32ce-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d32ce-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d32ce-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d32ce-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="d32ce-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="d32ce-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="d32ce-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="d32ce-209">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d32ce-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="d32ce-210">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="d32ce-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
