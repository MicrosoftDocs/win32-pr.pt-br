---
description: 'Saiba mais sobre: JET_PFNREALLOC função de retorno de chamada'
title: JET_PFNREALLOC função de retorno de chamada
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172082"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="0d8a9-103">JET_PFNREALLOC função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="0d8a9-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="0d8a9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0d8a9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="0d8a9-105">JET_PFNREALLOC função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="0d8a9-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="0d8a9-106">A função JET_PFNREALLOC é um retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usado pelo [JetEnumerateColumns](./jetenumeratecolumns-function.md) para alocar memória para seus buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="0d8a9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d8a9-107">Parameters</span></span>

<span data-ttu-id="0d8a9-108">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="0d8a9-108">*pvContext*</span></span>

<span data-ttu-id="0d8a9-109">O ponteiro de contexto fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d8a9-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="0d8a9-110">Esse ponteiro de contexto pode ser usado para transmitir o estado do chamador de [JetEnumerateColumns](./jetenumeratecolumns-function.md) para a implementação desse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="0d8a9-111">*PV*</span><span class="sxs-lookup"><span data-stu-id="0d8a9-111">*pv*</span></span>

<span data-ttu-id="0d8a9-112">Se não for NULL, especifica um ponteiro para um bloco de memória alocado anteriormente por este retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="0d8a9-113">Se for NULL, um novo bloco de memória do tamanho solicitado será alocado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="0d8a9-114">*CB*</span><span class="sxs-lookup"><span data-stu-id="0d8a9-114">*cb*</span></span>

<span data-ttu-id="0d8a9-115">O novo tamanho do bloco de memória em bytes.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="0d8a9-116">Se esse parâmetro for 0 (zero) e um bloco de memória for especificado, esse bloco de memória será liberado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="0d8a9-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0d8a9-117">Return Value</span></span>

<span data-ttu-id="0d8a9-118">O sistema pode gerar códigos de êxito ou de falha como resultado de uma chamada para essa função.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="0d8a9-119">Para obter informações sobre como retornar esses códigos como HRESULTs, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0d8a9-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d8a9-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0d8a9-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="0d8a9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d8a9-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d8a9-122">Sucesso</span><span class="sxs-lookup"><span data-stu-id="0d8a9-122">Success</span></span></p></td>
<td><p><span data-ttu-id="0d8a9-123">Se um bloco de memória alocado anteriormente tiver sido especificado e um novo tamanho zero for especificado, esse bloco será liberado e nulo será retornado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="0d8a9-124">Se um bloco de memória alocado anteriormente tiver sido especificado e um novo tamanho diferente de zero tiver sido especificado, o bloco de memória realocada será retornado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="0d8a9-125">Se nenhum bloco de memória tiver sido especificado, um bloco de memória recentemente alocado do tamanho especificado será retornado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d8a9-126">Falha</span><span class="sxs-lookup"><span data-stu-id="0d8a9-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="0d8a9-127">NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-127">NULL will be returned.</span></span> <span data-ttu-id="0d8a9-128">Se um bloco de memória alocado anteriormente tiver sido fornecido, esse bloco permanecerá alocado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="0d8a9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d8a9-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d8a9-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0d8a9-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0d8a9-131">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d8a9-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="0d8a9-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0d8a9-133">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d8a9-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="0d8a9-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0d8a9-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0d8a9-136">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0d8a9-136">See Also</span></span>

[<span data-ttu-id="0d8a9-137">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="0d8a9-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
