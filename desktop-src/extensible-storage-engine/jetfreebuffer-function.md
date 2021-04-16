---
description: 'Saiba mais sobre: função JetFreeBuffer'
title: Função JetFreeBuffer
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782550"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="9298b-103">Função JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9298b-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="9298b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9298b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="9298b-105">Função JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9298b-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="9298b-106">A função **JetFreeBuffer** libera a memória que foi alocada por uma chamada do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9298b-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="9298b-107">**Windows XP: o JetFreeBuffer** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9298b-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="9298b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9298b-108">Parameters</span></span>

<span data-ttu-id="9298b-109">*pbBuf*</span><span class="sxs-lookup"><span data-stu-id="9298b-109">*pbBuf*</span></span>

<span data-ttu-id="9298b-110">Ponteiro para uma região de memória que foi alocada anteriormente por uma chamada para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9298b-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="9298b-111">**NULL** é aceitável e será ignorado.</span><span class="sxs-lookup"><span data-stu-id="9298b-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="9298b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9298b-112">Return Value</span></span>

<span data-ttu-id="9298b-113">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="9298b-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9298b-114">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9298b-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9298b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9298b-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="9298b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9298b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9298b-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9298b-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9298b-118">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9298b-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="9298b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9298b-119">Remarks</span></span>

<span data-ttu-id="9298b-120">É um comportamento indefinido para passar a memória que não foi alocada pelo mecanismo de banco de dados no para *pbBuf*.</span><span class="sxs-lookup"><span data-stu-id="9298b-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9298b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9298b-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9298b-122"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9298b-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9298b-123">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9298b-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9298b-124"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9298b-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9298b-125">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9298b-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9298b-126"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9298b-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9298b-127">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9298b-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9298b-128"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="9298b-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9298b-129">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9298b-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9298b-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9298b-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9298b-131">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9298b-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9298b-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9298b-132">See Also</span></span>

[<span data-ttu-id="9298b-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9298b-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9298b-134">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="9298b-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
