---
description: 'Saiba mais sobre: função JetGetInstanceMiscInfo'
title: Função JetGetInstanceMiscInfo
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011412"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="90a0d-103">Função JetGetInstanceMiscInfo</span><span class="sxs-lookup"><span data-stu-id="90a0d-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="90a0d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="90a0d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="90a0d-105">Função JetGetInstanceMiscInfo</span><span class="sxs-lookup"><span data-stu-id="90a0d-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="90a0d-106">A função **JetGetInstanceMiscInfo** recupera informações sobre a instância do, enquanto a instância está online.</span><span class="sxs-lookup"><span data-stu-id="90a0d-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="90a0d-107">**Windows Vista: o JetGetInstanceMiscInfo** é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90a0d-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="90a0d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90a0d-108">Parameters</span></span>

<span data-ttu-id="90a0d-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="90a0d-109">*instance*</span></span>

<span data-ttu-id="90a0d-110">Identifica a instância de banco de dados que será usada para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="90a0d-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="90a0d-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="90a0d-111">*pvResult*</span></span>

<span data-ttu-id="90a0d-112">Ponteiro para um buffer que receberá as informações.</span><span class="sxs-lookup"><span data-stu-id="90a0d-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="90a0d-113">O tipo do buffer é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="90a0d-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="90a0d-114">O chamador é responsável por alinhar o buffer adequadamente.</span><span class="sxs-lookup"><span data-stu-id="90a0d-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="90a0d-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="90a0d-115">*cbMax*</span></span>

<span data-ttu-id="90a0d-116">O tamanho, em bytes, do buffer passado em *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="90a0d-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="90a0d-117">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="90a0d-117">*InfoLevel*</span></span>

<span data-ttu-id="90a0d-118">Determina o tipo de informação que será recuperado para a instância especificada por *instância*.</span><span class="sxs-lookup"><span data-stu-id="90a0d-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="90a0d-119">O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="90a0d-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="90a0d-120">As opções a seguir estão disponíveis para uso com esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="90a0d-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90a0d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="90a0d-121">Value</span></span></p></th>
<th><p><span data-ttu-id="90a0d-122">Significado</span><span class="sxs-lookup"><span data-stu-id="90a0d-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90a0d-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="90a0d-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="90a0d-124"><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> da sequência do log de transações associada a essa instância.</span><span class="sxs-lookup"><span data-stu-id="90a0d-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="90a0d-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="90a0d-125">Return Value</span></span>

<span data-ttu-id="90a0d-126">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="90a0d-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="90a0d-127">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="90a0d-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90a0d-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="90a0d-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="90a0d-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="90a0d-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90a0d-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="90a0d-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="90a0d-131">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="90a0d-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a0d-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="90a0d-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="90a0d-133">O buffer era muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="90a0d-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a0d-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="90a0d-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="90a0d-135">Um <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> inválido ou um <em>InfoLevel</em> inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="90a0d-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="90a0d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a0d-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90a0d-137"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="90a0d-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="90a0d-138">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90a0d-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a0d-139"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="90a0d-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="90a0d-140">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="90a0d-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a0d-141"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="90a0d-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="90a0d-142">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="90a0d-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90a0d-143"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="90a0d-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="90a0d-144">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="90a0d-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90a0d-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="90a0d-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="90a0d-146">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="90a0d-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="90a0d-147">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="90a0d-147">See Also</span></span>

[<span data-ttu-id="90a0d-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="90a0d-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="90a0d-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="90a0d-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="90a0d-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="90a0d-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)
