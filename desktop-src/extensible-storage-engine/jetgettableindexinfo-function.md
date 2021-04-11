---
description: 'Saiba mais sobre: função JetGetTableIndexInfo'
title: Função JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172076"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="df974-103">Função JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="df974-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="df974-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="df974-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="df974-105">Função JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="df974-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="df974-106">A função **JetGetTableIndexInfo** recupera informações sobre um índice.</span><span class="sxs-lookup"><span data-stu-id="df974-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="df974-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df974-107">Parameters</span></span>

<span data-ttu-id="df974-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="df974-108">*sesid*</span></span>

<span data-ttu-id="df974-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="df974-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="df974-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="df974-110">*tableid*</span></span>

<span data-ttu-id="df974-111">A tabela de banco de dados que contém o índice que contém as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="df974-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="df974-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="df974-112">*szIndexName*</span></span>

<span data-ttu-id="df974-113">O nome do índice que contém informações que serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="df974-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="df974-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="df974-114">*pvResult*</span></span>

<span data-ttu-id="df974-115">Ponteiro para um buffer que receberá as informações.</span><span class="sxs-lookup"><span data-stu-id="df974-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="df974-116">O buffer deve ser alinhado para conter o tipo necessário.</span><span class="sxs-lookup"><span data-stu-id="df974-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="df974-117">O tipo do buffer é dependente do parâmetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="df974-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="df974-118">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="df974-118">*cbResult*</span></span>

<span data-ttu-id="df974-119">O tamanho, em bytes, do buffer passado no parâmetro *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="df974-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="df974-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="df974-120">*InfoLevel*</span></span>

<span data-ttu-id="df974-121">Especifica quais informações serão armazenadas em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="df974-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="df974-122">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="df974-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df974-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df974-123">Value</span></span></p></th>
<th><p><span data-ttu-id="df974-124">Significado</span><span class="sxs-lookup"><span data-stu-id="df974-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df974-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="df974-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="df974-126"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="df974-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="df974-127">Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="df974-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="df974-128">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="df974-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="df974-130"><em>pvResult</em> é interpretado como um LCID.</span><span class="sxs-lookup"><span data-stu-id="df974-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="df974-131">Em caso de sucesso, o LCID mantém o identificador de localidade do índice.</span><span class="sxs-lookup"><span data-stu-id="df974-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="df974-132">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="df974-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="df974-134"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="df974-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="df974-135">Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="df974-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="df974-136">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="df974-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="df974-138">JET_IdxInfoOLC está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="df974-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="df974-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="df974-140">JET_IdxInfoResetOLC está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="df974-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="df974-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="df974-142"><em>pvResult</em> é interpretado como um ULONG.</span><span class="sxs-lookup"><span data-stu-id="df974-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="df974-143">Em caso de sucesso, o ULONG mantém o uso do espaço do índice.</span><span class="sxs-lookup"><span data-stu-id="df974-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="df974-144">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="df974-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="df974-146">JET_IdxInfoSysTabCursor está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="df974-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="df974-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="df974-148">JET_IdxInfoLangid é preterida.</span><span class="sxs-lookup"><span data-stu-id="df974-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="df974-149">Em vez disso, use JET_IdxInfoLCID e a macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="df974-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="df974-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="df974-151"><em>pvResult</em> é interpretado como um ULONG.</span><span class="sxs-lookup"><span data-stu-id="df974-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="df974-152">Em caso de sucesso, o ULONG mantém a contagem de índices na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="df974-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="df974-153"><em>szIndexName</em> é ignorado.</span><span class="sxs-lookup"><span data-stu-id="df974-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="df974-154">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="df974-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="df974-156"><em>pvResult</em> é interpretado como um ushort.</span><span class="sxs-lookup"><span data-stu-id="df974-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="df974-157">Em caso de sucesso, o USHORT mantém o valor de <em>cbVarSegMac</em> usado quando o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="df974-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="df974-158">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbVarSegMac</em>.</span><span class="sxs-lookup"><span data-stu-id="df974-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="df974-159">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="df974-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="df974-161"><em>pvResult</em> é interpretado como um <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="df974-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="df974-162">Em caso de sucesso, a estrutura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recebe informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="df974-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="df974-163">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="df974-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="df974-165"><em>pvResult</em> é interpretado como um ushort.</span><span class="sxs-lookup"><span data-stu-id="df974-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="df974-166">Em caso de sucesso, o USHORT mantém o valor de cbKeyMost usado quando o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="df974-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="df974-167">Consulte a estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de cbKeyMost.</span><span class="sxs-lookup"><span data-stu-id="df974-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="df974-168">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="df974-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="df974-170"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="df974-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="df974-171">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="df974-172"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df974-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="df974-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="df974-174"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="df974-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="df974-175">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="df974-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df974-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="df974-177">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="df974-177">Return Value</span></span>

<span data-ttu-id="df974-178">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="df974-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="df974-179">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="df974-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df974-180">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="df974-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="df974-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="df974-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df974-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="df974-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="df974-183">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="df974-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="df974-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="df974-185">O índice especificado não pode ser encontrado na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="df974-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="df974-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="df974-187">O buffer passado como <em>pvResult</em> era muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="df974-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="df974-188">O conteúdo do buffer está indefinido.</span><span class="sxs-lookup"><span data-stu-id="df974-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="df974-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="df974-189">Remarks</span></span>

<span data-ttu-id="df974-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) e **JetGetTableIndexInfo** recuperam informações idênticas sobre um índice.</span><span class="sxs-lookup"><span data-stu-id="df974-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="df974-191">A diferença está em como a tabela é especificada.</span><span class="sxs-lookup"><span data-stu-id="df974-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="df974-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) espera um banco de dados (*DBID*) e o nome de uma tabela (*szTableName*), enquanto **JetGetTableIndexInfo** espera um identificador de tabela (*TableName*).</span><span class="sxs-lookup"><span data-stu-id="df974-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="df974-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df974-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df974-194"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="df974-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="df974-195">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="df974-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-196"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="df974-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="df974-197">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="df974-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-198"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="df974-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="df974-199">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="df974-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-200"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="df974-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="df974-201">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="df974-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df974-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="df974-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="df974-203">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="df974-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df974-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="df974-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="df974-205">Implementado como <strong>JetGetTableIndexInfoW</strong> (Unicode) e <strong>JetGetTableIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="df974-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="df974-206">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="df974-206">See Also</span></span>

[<span data-ttu-id="df974-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="df974-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="df974-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="df974-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="df974-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="df974-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="df974-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="df974-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="df974-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="df974-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="df974-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="df974-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="df974-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="df974-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="df974-214">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="df974-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
