---
description: 'Saiba mais sobre: função JetGetThreadStats'
title: Função JetGetThreadStats
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791540"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="56216-103">Função JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="56216-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="56216-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56216-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="56216-105">Função JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="56216-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="56216-106">A função **JetGetThreadStats** recupera informações de desempenho do mecanismo de banco de dados para o thread atual.</span><span class="sxs-lookup"><span data-stu-id="56216-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="56216-107">Várias chamadas podem ser usadas para coletar estatísticas que refletem a atividade do mecanismo de banco de dados nesse thread entre essas chamadas.</span><span class="sxs-lookup"><span data-stu-id="56216-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="56216-108">**Windows Vista:** o **JetGetThreadStats** é introduzido no Windows Vista.  </span><span class="sxs-lookup"><span data-stu-id="56216-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="56216-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56216-109">Parameters</span></span>

<span data-ttu-id="56216-110">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="56216-110">*pvResult*</span></span>

<span data-ttu-id="56216-111">O buffer de saída que recebe os dados de estatísticas de thread.</span><span class="sxs-lookup"><span data-stu-id="56216-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="56216-112">O buffer contém uma estrutura de [JET_THREADSTATS](./jet-threadstats-structure.md) após uma chamada bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="56216-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="56216-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="56216-113">*cbMax*</span></span>

<span data-ttu-id="56216-114">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="56216-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="56216-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="56216-115">Return Value</span></span>

<span data-ttu-id="56216-116">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="56216-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56216-117">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56216-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56216-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="56216-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="56216-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="56216-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56216-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56216-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56216-121">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="56216-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56216-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="56216-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="56216-123">A operação falhou porque o buffer de saída fornecido era muito pequeno para conter os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="56216-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="56216-124">A função <strong>JetGetThreadStats</strong> retornará esse erro quando o buffer de saída for muito pequeno para conter a menor versão da estrutura de <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> suportada pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="56216-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56216-125">Em caso de sucesso, o buffer de saída conterá uma estrutura de [JET_THREADSTATS](./jet-threadstats-structure.md) que contém estatísticas do mecanismo de banco de dados para o thread atual.</span><span class="sxs-lookup"><span data-stu-id="56216-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="56216-126">Em caso de falha, o estado do buffer de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="56216-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="56216-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="56216-127">Remarks</span></span>

<span data-ttu-id="56216-128">As informações fornecidas por duas chamadas consecutivas dessa API devem ser usadas para computar a despesa de qualquer outra operação do mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="56216-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="56216-129">Em geral, isso é feito fazendo uma leitura anterior e posterior das estatísticas e subtraindo a contagem After da contagem before para obter a contagem líquida de operações executadas.</span><span class="sxs-lookup"><span data-stu-id="56216-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="56216-130">Por exemplo, um aplicativo poderia chamar **JetGetThreadStats** uma vez para obter uma leitura inicial das estatísticas para o thread atual.</span><span class="sxs-lookup"><span data-stu-id="56216-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="56216-131">Em seguida, ele pode chamar a função [JetMove](./jetmove-function.md) com o parâmetro de *galinha* definido como JET_MoveNext para mover para a próxima entrada de índice em um índice.</span><span class="sxs-lookup"><span data-stu-id="56216-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="56216-132">Em seguida, ele pode chamar **JetGetThreadStats** novamente para obter outra leitura das estatísticas do thread.</span><span class="sxs-lookup"><span data-stu-id="56216-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="56216-133">Em seguida, ele pode subtrair o contador cPageReferenced da segunda leitura do primeiro.</span><span class="sxs-lookup"><span data-stu-id="56216-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="56216-134">O resultado seria o número de páginas de banco de dados referenciadas pelo mecanismo de banco de dados para executar a operação [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="56216-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="56216-135">As estatísticas de cada thread são acumuladas durante o tempo de vida desse thread.</span><span class="sxs-lookup"><span data-stu-id="56216-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="56216-136">As estatísticas serão redefinidas se a DLL do mecanismo de banco de dados for descarregada do processo de host.</span><span class="sxs-lookup"><span data-stu-id="56216-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="56216-137">A estrutura de [JET_THREADSTATS](./jet-threadstats-structure.md) provavelmente será expandida no futuro para conter mais estatísticas.</span><span class="sxs-lookup"><span data-stu-id="56216-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="56216-138">Novas estatísticas serão adicionadas ao final da estrutura e poderão ser recuperadas com um tamanho de buffer de saída maior.</span><span class="sxs-lookup"><span data-stu-id="56216-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="56216-139">A presença de estatísticas adicionais pode ser inferida por um valor cbStruct maior.</span><span class="sxs-lookup"><span data-stu-id="56216-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="56216-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56216-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56216-141"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="56216-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56216-142">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56216-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56216-143"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="56216-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56216-144">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56216-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56216-145"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="56216-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56216-146">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="56216-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56216-147"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="56216-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56216-148">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="56216-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56216-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="56216-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56216-150">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="56216-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56216-151">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="56216-151">See Also</span></span>

[<span data-ttu-id="56216-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56216-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56216-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="56216-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="56216-154">JetMove</span><span class="sxs-lookup"><span data-stu-id="56216-154">JetMove</span></span>](./jetmove-function.md)
