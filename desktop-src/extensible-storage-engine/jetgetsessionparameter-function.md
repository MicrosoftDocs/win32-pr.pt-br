---
description: 'Saiba mais sobre: função JetGetSessionParameter'
title: Função JetGetSessionParameter
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826796"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="3d5db-103">Função JetGetSessionParameter</span><span class="sxs-lookup"><span data-stu-id="3d5db-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="3d5db-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3d5db-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="3d5db-105">A função **JetGetSessionParameter** lê o parâmetro de sessão para a sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="3d5db-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="3d5db-106">A função **JetGetSessionParameter** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d5db-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="3d5db-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d5db-107">Parameters</span></span>

<span data-ttu-id="3d5db-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3d5db-108">*sesid*</span></span>

<span data-ttu-id="3d5db-109">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3d5db-109">The session to use for this call.</span></span>

<span data-ttu-id="3d5db-110">Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.</span><span class="sxs-lookup"><span data-stu-id="3d5db-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="3d5db-111">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="3d5db-111">*sesparamid*</span></span>

<span data-ttu-id="3d5db-112">A ID do parâmetro de sessão a ser definido.</span><span class="sxs-lookup"><span data-stu-id="3d5db-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="3d5db-113">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="3d5db-113">*pvParam*</span></span>

<span data-ttu-id="3d5db-114">Dados neste parâmetro de sessão.</span><span class="sxs-lookup"><span data-stu-id="3d5db-114">Data in this session parameter.</span></span>

<span data-ttu-id="3d5db-115">*cbParamMax*</span><span class="sxs-lookup"><span data-stu-id="3d5db-115">*cbParamMax*</span></span>

<span data-ttu-id="3d5db-116">O tamanho máximo do conjunto de dados neste parâmetro de sessão.</span><span class="sxs-lookup"><span data-stu-id="3d5db-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="3d5db-117">*pcbParamActual*</span><span class="sxs-lookup"><span data-stu-id="3d5db-117">*pcbParamActual*</span></span>

<span data-ttu-id="3d5db-118">O tamanho real do conjunto de dados neste parâmetro de sessão.</span><span class="sxs-lookup"><span data-stu-id="3d5db-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="3d5db-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d5db-119">Return value</span></span>

<span data-ttu-id="3d5db-120">Em caso de sucesso, o buffer de saída apropriado para o parâmetro de sessão solicitado será definido como o valor desse parâmetro de sessão.</span><span class="sxs-lookup"><span data-stu-id="3d5db-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="3d5db-121">Em caso de falha, o estado dos buffers de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="3d5db-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3d5db-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d5db-122">Remarks</span></span>

<span data-ttu-id="3d5db-123">O parâmetro Session é usado para o tempo de vida da sessão ou até que o valor seja redefinido.</span><span class="sxs-lookup"><span data-stu-id="3d5db-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3d5db-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d5db-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d5db-125"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3d5db-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3d5db-126">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d5db-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d5db-127"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3d5db-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3d5db-128">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3d5db-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d5db-129"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3d5db-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3d5db-130">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3d5db-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d5db-131"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3d5db-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3d5db-132">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3d5db-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d5db-133"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3d5db-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3d5db-134">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3d5db-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3d5db-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d5db-135">See also</span></span>

[<span data-ttu-id="3d5db-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="3d5db-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="3d5db-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3d5db-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3d5db-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3d5db-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="3d5db-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3d5db-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3d5db-140">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="3d5db-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="3d5db-141">JetInit</span><span class="sxs-lookup"><span data-stu-id="3d5db-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="3d5db-142">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3d5db-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3d5db-143">JetStopService</span><span class="sxs-lookup"><span data-stu-id="3d5db-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="3d5db-144">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="3d5db-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
