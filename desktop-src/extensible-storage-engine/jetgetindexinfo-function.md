---
description: 'Saiba mais sobre: função JetGetIndexInfo'
title: Função JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748858"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="187fc-103">Função JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="187fc-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="187fc-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="187fc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="187fc-105">Função JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="187fc-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="187fc-106">A função **JetGetIndexInfo** recupera informações sobre um índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="187fc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="187fc-107">Parameters</span></span>

<span data-ttu-id="187fc-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="187fc-108">*sesid*</span></span>

<span data-ttu-id="187fc-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="187fc-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="187fc-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="187fc-110">*dbid*</span></span>

<span data-ttu-id="187fc-111">O identificador de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="187fc-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="187fc-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="187fc-112">*szTableName*</span></span>

<span data-ttu-id="187fc-113">O nome da tabela que contém o índice com as informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="187fc-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="187fc-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="187fc-114">*szIndexName*</span></span>

<span data-ttu-id="187fc-115">O nome do índice com as informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="187fc-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="187fc-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="187fc-116">*pvResult*</span></span>

<span data-ttu-id="187fc-117">Ponteiro para um buffer que receberá as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="187fc-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="187fc-118">O buffer deve ser alinhado para conter o tipo necessário.</span><span class="sxs-lookup"><span data-stu-id="187fc-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="187fc-119">O tipo do buffer é dependente do parâmetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="187fc-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="187fc-120">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="187fc-120">*cbResult*</span></span>

<span data-ttu-id="187fc-121">O tamanho, em bytes, do buffer passado como *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="187fc-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="187fc-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="187fc-122">*InfoLevel*</span></span>

<span data-ttu-id="187fc-123">As informações que serão armazenadas em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="187fc-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="187fc-124">As opções a seguir podem ser usadas para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="187fc-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="187fc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="187fc-125">Value</span></span></p></th>
<th><p><span data-ttu-id="187fc-126">Significado</span><span class="sxs-lookup"><span data-stu-id="187fc-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="187fc-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="187fc-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="187fc-128"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="187fc-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="187fc-129">Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="187fc-130">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="187fc-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="187fc-132"><em>pvResult</em> é interpretado como um ULONG.</span><span class="sxs-lookup"><span data-stu-id="187fc-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="187fc-133">Em caso de sucesso, o ULONG mantém a contagem de índices na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="187fc-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="187fc-134"><em>szIndexName</em> é ignorado.</span><span class="sxs-lookup"><span data-stu-id="187fc-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="187fc-135">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="187fc-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="187fc-137"><em>pvResult</em> é interpretado como um <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="187fc-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="187fc-138">Em caso de sucesso, a estrutura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recebe informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="187fc-139">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="187fc-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="187fc-141">JET_IdxInfoLangid é preterida.</span><span class="sxs-lookup"><span data-stu-id="187fc-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="187fc-142">Use JET_IdxInfoLCID e a macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> em vez disso.</span><span class="sxs-lookup"><span data-stu-id="187fc-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="187fc-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="187fc-144"><em>pvResult</em> é interpretado como um LCID.</span><span class="sxs-lookup"><span data-stu-id="187fc-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="187fc-145">Em caso de sucesso, o LCID mantém o identificador de localidade do índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="187fc-146">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="187fc-147"><strong>Windows XP:  </strong> O JET_IdxInfoLCID é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="187fc-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="187fc-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="187fc-149"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="187fc-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="187fc-150">Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="187fc-151">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="187fc-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="187fc-153">JET_IdxInfoOLC está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="187fc-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="187fc-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="187fc-155">JET_IdxInfoResetOLC está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="187fc-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="187fc-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="187fc-157"><em>pvResult</em> é interpretado como um ULONG.</span><span class="sxs-lookup"><span data-stu-id="187fc-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="187fc-158">Em caso de sucesso, o ULONG mantém o uso do espaço do índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="187fc-159">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="187fc-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="187fc-161">JET_IdxInfoSysTabCursor está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="187fc-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="187fc-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="187fc-163"><em>pvResult</em> é interpretado como um ushort.</span><span class="sxs-lookup"><span data-stu-id="187fc-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="187fc-164">Em caso de sucesso, o USHORT mantém o valor de <em>cbVarSegMac</em> usado quando o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="187fc-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="187fc-165">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbVarSegMac</em>.</span><span class="sxs-lookup"><span data-stu-id="187fc-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="187fc-166">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="187fc-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="187fc-168"><em>pvResult</em> é interpretado como um ushort.</span><span class="sxs-lookup"><span data-stu-id="187fc-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="187fc-169">Em caso de sucesso, o USHORT mantém o valor de <em>cbKeyMost</em> usado quando o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="187fc-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="187fc-170">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbKeyMost</em>.</span><span class="sxs-lookup"><span data-stu-id="187fc-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="187fc-171">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="187fc-172"><strong>Windows Vista:  </strong> O JET_IdxInfoKeyMost é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="187fc-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="187fc-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="187fc-174"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="187fc-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="187fc-175">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="187fc-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="187fc-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="187fc-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="187fc-178"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="187fc-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="187fc-179">Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="187fc-180"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="187fc-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="187fc-181">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="187fc-181">Return Value</span></span>

<span data-ttu-id="187fc-182">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="187fc-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="187fc-183">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="187fc-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="187fc-184">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="187fc-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="187fc-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="187fc-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="187fc-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="187fc-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="187fc-187">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="187fc-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="187fc-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="187fc-189">O índice especificado não pode ser encontrado na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="187fc-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="187fc-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="187fc-191">O buffer passado como <em>pvResult</em> era muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="187fc-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="187fc-192">O conteúdo do buffer está indefinido.</span><span class="sxs-lookup"><span data-stu-id="187fc-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="187fc-193">Comentários</span><span class="sxs-lookup"><span data-stu-id="187fc-193">Remarks</span></span>

<span data-ttu-id="187fc-194">**JetGetIndexInfo** e [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperam informações idênticas sobre um índice.</span><span class="sxs-lookup"><span data-stu-id="187fc-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="187fc-195">A diferença está em como a tabela é especificada.</span><span class="sxs-lookup"><span data-stu-id="187fc-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="187fc-196">**JetGetIndexInfo** espera um banco de dados (*DBID*) e o nome de uma tabela (*szTableName*), enquanto [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) espera um identificador de tabela (*TableName*).</span><span class="sxs-lookup"><span data-stu-id="187fc-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="187fc-197">Requisitos</span><span class="sxs-lookup"><span data-stu-id="187fc-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="187fc-198"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="187fc-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="187fc-199">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="187fc-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-200"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="187fc-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="187fc-201">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="187fc-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-202"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="187fc-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="187fc-203">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="187fc-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-204"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="187fc-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="187fc-205">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="187fc-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="187fc-206"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="187fc-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="187fc-207">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="187fc-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="187fc-208"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="187fc-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="187fc-209">Implementado como <strong>JetGetIndexInfoW</strong> (Unicode) e <strong>JetGetIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="187fc-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="187fc-210">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="187fc-210">See Also</span></span>

[<span data-ttu-id="187fc-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="187fc-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="187fc-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="187fc-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="187fc-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="187fc-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="187fc-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="187fc-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="187fc-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="187fc-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="187fc-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="187fc-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="187fc-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="187fc-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="187fc-218">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="187fc-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
