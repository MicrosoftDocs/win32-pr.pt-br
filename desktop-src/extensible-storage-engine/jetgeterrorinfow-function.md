---
description: 'Saiba mais sobre: função JetGetErrorInfoW'
title: Função JetGetErrorInfoW
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104092014"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="d326a-103">Função JetGetErrorInfoW</span><span class="sxs-lookup"><span data-stu-id="d326a-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="d326a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d326a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="d326a-105">Função JetGetErrorInfoW</span><span class="sxs-lookup"><span data-stu-id="d326a-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="d326a-106">A função **JetGetErrorInfoW** BAS_ do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d326a-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="d326a-107">Observação: esta documentação se baseia em uma versão preliminar do mecanismo de armazenamento extensível.</span><span class="sxs-lookup"><span data-stu-id="d326a-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="d326a-108">Essas informações estão sujeitas a alterações.</span><span class="sxs-lookup"><span data-stu-id="d326a-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="d326a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d326a-109">Parameters</span></span>

<span data-ttu-id="d326a-110">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="d326a-110">*pvContext*</span></span>

<span data-ttu-id="d326a-111">O contexto ou o valor de erro para o qual as informações de erro estendidas são necessárias.</span><span class="sxs-lookup"><span data-stu-id="d326a-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="d326a-112">O valor transmitido depende do valor do parâmetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="d326a-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="d326a-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="d326a-113">*pvResult*</span></span>

<span data-ttu-id="d326a-114">Um ponteiro para um buffer que receberá as informações.</span><span class="sxs-lookup"><span data-stu-id="d326a-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="d326a-115">O tipo do buffer depende do valor do parâmetro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="d326a-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="d326a-116">O chamador deve ser configurado para alinhar o buffer adequadamente.</span><span class="sxs-lookup"><span data-stu-id="d326a-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="d326a-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="d326a-117">*cbMax*</span></span>

<span data-ttu-id="d326a-118">O tamanho máximo da estrutura *pvResult* que é passada.</span><span class="sxs-lookup"><span data-stu-id="d326a-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="d326a-119">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="d326a-119">*InfoLevel*</span></span>

<span data-ttu-id="d326a-120">O tipo de informações que serão recuperadas para as informações de erro/contexto é especificado pelo parâmetro *pvContext* .</span><span class="sxs-lookup"><span data-stu-id="d326a-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="d326a-121">O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="d326a-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="d326a-122">A tabela a seguir lista os possíveis valores para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d326a-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d326a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d326a-123">Value</span></span></p></th>
<th><p><span data-ttu-id="d326a-124">Significado</span><span class="sxs-lookup"><span data-stu-id="d326a-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d326a-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="d326a-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="d326a-126"><em>pvContext</em> é interpretado como um código de/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>pvResult</em> é interpretado como um <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>e os campos da estrutura de <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> são preenchidos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="d326a-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d326a-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d326a-127">*grbit*</span></span>

<span data-ttu-id="d326a-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d326a-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="d326a-129">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d326a-129">Return Value</span></span>

<span data-ttu-id="d326a-130">Essa função retorna o tipo de dados [JET_ERR](./extensible-storage-engine-error-codes.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d326a-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="d326a-131">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d326a-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d326a-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d326a-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="d326a-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="d326a-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d326a-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d326a-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d326a-135">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d326a-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d326a-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d326a-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d326a-137">Um dos parâmetros fornecidos contém um valor inesperado ou contém um valor que não faz sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d326a-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="d326a-138">Isso pode ocorrer para <strong>JetGetErrorInfo</strong> quando ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d326a-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="d326a-139">O valor do parâmetro <em>InfoLevel</em> especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="d326a-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="d326a-140">O valor de <em>grbit</em> especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="d326a-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="d326a-141">O valor de <em>cbMax</em> do buffer de parâmetro <em>pvResult</em> especificado é menor que o tamanho necessário para a saída desse parâmetro <em>InfoLevel</em> .</span><span class="sxs-lookup"><span data-stu-id="d326a-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="d326a-142">Para <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, o valor de <a href="gg294092(v=exchg.10).md">JET_ERR</a> passado é desconhecido para o mecanismo.</span><span class="sxs-lookup"><span data-stu-id="d326a-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d326a-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="d326a-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="d326a-144">Se esse SKU do Windows não oferecer suporte a essa função, esse erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="d326a-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d326a-145">Em caso de sucesso, o buffer de saída apropriado para o contexto/valor de erro solicitado será definido para as informações de erro estendidas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="d326a-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="d326a-146">Em caso de falha, o estado dos buffers de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="d326a-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="d326a-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="d326a-147">Remarks</span></span>

<span data-ttu-id="d326a-148">A função [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) e [JET_ERRCAT](./jet-errcat.md) grupo de constantes contêm documentação sobre as informações de erro estendidas que são retornadas para *InfoLevel* = JET_ErrorInfoSpecificErr.</span><span class="sxs-lookup"><span data-stu-id="d326a-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="d326a-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d326a-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d326a-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d326a-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d326a-151">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d326a-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d326a-152"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d326a-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d326a-153">Requer o Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="d326a-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d326a-154"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d326a-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d326a-155">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d326a-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d326a-156"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d326a-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d326a-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d326a-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d326a-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d326a-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d326a-159">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d326a-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d326a-160"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d326a-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d326a-161">Observação: somente o <strong>JetGetErrorInfoW</strong> (Unicode) é implementado.</span><span class="sxs-lookup"><span data-stu-id="d326a-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="d326a-162">Esta API não tem uma versão (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d326a-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>
