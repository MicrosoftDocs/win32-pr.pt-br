---
description: 'Saiba mais sobre: função JetGetInstanceInfo'
title: Função JetGetInstanceInfo
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829242"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="ca505-103">Função JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="ca505-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="ca505-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ca505-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="ca505-105">Função JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="ca505-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="ca505-106">A função **JetGetInstanceInfo** recupera informações sobre as instâncias que estão em execução.</span><span class="sxs-lookup"><span data-stu-id="ca505-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="ca505-107">**Windows XP: o JetGetInstanceInfo** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca505-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="ca505-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca505-108">Parameters</span></span>

<span data-ttu-id="ca505-109">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="ca505-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="ca505-110">Um ponteiro para um buffer que receberá o número de elementos armazenados em *paInstanceInfo*.</span><span class="sxs-lookup"><span data-stu-id="ca505-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="ca505-111">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="ca505-111">*paInstanceInfo*</span></span>

<span data-ttu-id="ca505-112">Um ponteiro para um buffer que receberá o endereço do primeiro elemento de uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="ca505-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="ca505-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ca505-113">Return Value</span></span>

<span data-ttu-id="ca505-114">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca505-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ca505-115">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ca505-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca505-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ca505-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="ca505-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca505-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca505-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ca505-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ca505-119">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ca505-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca505-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ca505-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ca505-121">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca505-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ca505-122">Esse erro será retornado por <strong>JetGetInstanceInfo</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="ca505-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="ca505-123"><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> são nulos.</span><span class="sxs-lookup"><span data-stu-id="ca505-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca505-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="ca505-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="ca505-125">Memória insuficiente para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ca505-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ca505-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca505-126">Remarks</span></span>

<span data-ttu-id="ca505-127">O mecanismo de banco de dados irá alocar uma matriz de estruturas de [JET_INSTANCE_INFO](./jet-instance-info-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="ca505-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="ca505-128">O chamador é responsável por liberar essa memória com [JetFreeBuffer](./jetfreebuffer-function.md).</span><span class="sxs-lookup"><span data-stu-id="ca505-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="ca505-129">Se não houver nenhuma instância ativa, **JetGetInstanceInfo** retornará JET_errSuccess e *pcInstanceInfo* receberá o valor 0.</span><span class="sxs-lookup"><span data-stu-id="ca505-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ca505-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca505-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca505-131"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ca505-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ca505-132">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca505-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca505-133"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ca505-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ca505-134">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ca505-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca505-135"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ca505-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ca505-136">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ca505-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca505-137"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="ca505-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ca505-138">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ca505-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca505-139"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ca505-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ca505-140">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ca505-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca505-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ca505-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ca505-142">Implementado como <strong>JetGetInstanceInfoW</strong> (Unicode) e <strong>JetGetInstanceInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ca505-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ca505-143">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ca505-143">See Also</span></span>

[<span data-ttu-id="ca505-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ca505-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ca505-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ca505-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ca505-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ca505-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="ca505-147">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ca505-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)
