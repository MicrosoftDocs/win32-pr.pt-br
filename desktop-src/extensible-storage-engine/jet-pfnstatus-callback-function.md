---
description: 'Saiba mais sobre: JET_PFNSTATUS função de retorno de chamada'
title: JET_PFNSTATUS função de retorno de chamada
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170545"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="9457f-103">JET_PFNSTATUS função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="9457f-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="9457f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9457f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="9457f-105">JET_PFNSTATUS função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="9457f-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="9457f-106">A função de retorno de chamada **JET_PFNSTATUS** recebe informações sobre o progresso de operações de longa execução, como operações de desfragmentação, backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="9457f-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="9457f-107">Durante essas operações, o mecanismo de banco de dados chama essa função de retorno de chamada para fornecer uma atualização no andamento da operação.</span><span class="sxs-lookup"><span data-stu-id="9457f-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="9457f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9457f-108">Parameters</span></span>

<span data-ttu-id="9457f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9457f-109">*sesid*</span></span>

<span data-ttu-id="9457f-110">A sessão do tipo [JET_SESID](./jet-sesid.md) com a qual a função de longa execução foi chamada.</span><span class="sxs-lookup"><span data-stu-id="9457f-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="9457f-111">*padrões*</span><span class="sxs-lookup"><span data-stu-id="9457f-111">*snp*</span></span>

<span data-ttu-id="9457f-112">O tipo de operação conforme especificado em [JET_SNP](./jet-snp.md).</span><span class="sxs-lookup"><span data-stu-id="9457f-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="9457f-113">Os tipos de operações incluem reparar, compactar, restaurar, fazer backup, atualizar, depurar e atualizar o formato do registro.</span><span class="sxs-lookup"><span data-stu-id="9457f-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="9457f-114">*snt*</span><span class="sxs-lookup"><span data-stu-id="9457f-114">*snt*</span></span>

<span data-ttu-id="9457f-115">O status de uma operação.</span><span class="sxs-lookup"><span data-stu-id="9457f-115">The status of an operation.</span></span> <span data-ttu-id="9457f-116">Os tipos de status incluem início, em andamento, conclusão ou falha.</span><span class="sxs-lookup"><span data-stu-id="9457f-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="9457f-117">O status será especificado com o terceiro parâmetro do tipo [JET_SNT](./jet-snt.md).</span><span class="sxs-lookup"><span data-stu-id="9457f-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="9457f-118">*PV*</span><span class="sxs-lookup"><span data-stu-id="9457f-118">*pv*</span></span>

<span data-ttu-id="9457f-119">Um ponteiro opcional para uma estrutura do tipo [JET_SNPROG](./jet-snprog-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9457f-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="9457f-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9457f-120">Return Value</span></span>

<span data-ttu-id="9457f-121">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9457f-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="9457f-122">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9457f-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="9457f-123">Em caso de sucesso, a operação que emitiu o retorno de chamada pode continuar normalmente.</span><span class="sxs-lookup"><span data-stu-id="9457f-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="9457f-124">Em alguns casos, o retorno de chamada pode retornar um aviso que influencia essa operação.</span><span class="sxs-lookup"><span data-stu-id="9457f-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="9457f-125">Em caso de falha, a operação que emitiu o retorno de chamada pode continuar normalmente ou pode falhar.</span><span class="sxs-lookup"><span data-stu-id="9457f-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="9457f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="9457f-126">Remarks</span></span>

<span data-ttu-id="9457f-127">Essa função de retorno de chamada será usada em uma notificação de progresso, na qual a estrutura indicará o estado atual do progresso.</span><span class="sxs-lookup"><span data-stu-id="9457f-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="9457f-128">Observe que a função de retorno de chamada pode ser chamada várias vezes para o andamento da operação.</span><span class="sxs-lookup"><span data-stu-id="9457f-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="9457f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9457f-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9457f-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9457f-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9457f-131">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9457f-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9457f-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9457f-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9457f-133">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9457f-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9457f-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9457f-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9457f-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9457f-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9457f-136">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9457f-136">See Also</span></span>

[<span data-ttu-id="9457f-137">Códigos de erro do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="9457f-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="9457f-138">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="9457f-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="9457f-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9457f-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9457f-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="9457f-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="9457f-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="9457f-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="9457f-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="9457f-142">JET_SNT</span></span>](./jet-snt.md)
