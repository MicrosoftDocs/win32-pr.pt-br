---
description: 'Saiba mais sobre: função JetStopServiceInstance'
title: Função JetStopServiceInstance
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793701"
---
# <a name="jetstopserviceinstance-function"></a><span data-ttu-id="b69d7-103">Função JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="b69d7-103">JetStopServiceInstance Function</span></span>


<span data-ttu-id="b69d7-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b69d7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopserviceinstance-function"></a><span data-ttu-id="b69d7-105">Função JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="b69d7-105">JetStopServiceInstance Function</span></span>

<span data-ttu-id="b69d7-106">A função **JetStopServiceInstance** prepara uma instância para encerramento.</span><span class="sxs-lookup"><span data-stu-id="b69d7-106">The **JetStopServiceInstance** function prepares an instance for termination.</span></span>

<span data-ttu-id="b69d7-107">**Windows XP:** o **JetStopServiceInstance** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="b69d7-107">**Windows XP:**  **JetStopServiceInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="b69d7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b69d7-108">Parameters</span></span>

<span data-ttu-id="b69d7-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="b69d7-109">*instance*</span></span>

<span data-ttu-id="b69d7-110">A instância em execução a ser usada para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="b69d7-110">The running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="b69d7-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b69d7-111">Return Value</span></span>

<span data-ttu-id="b69d7-112">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="b69d7-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b69d7-113">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b69d7-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b69d7-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b69d7-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="b69d7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b69d7-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b69d7-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b69d7-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b69d7-117">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b69d7-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b69d7-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b69d7-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b69d7-119">O parâmetro de instância especificado tem um valor inválido (não uma instância que está sendo executada no momento).</span><span class="sxs-lookup"><span data-stu-id="b69d7-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="b69d7-120"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b69d7-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b69d7-121">Se essa função for realizada com sucesso, ela se prepara para um encerramento futuro.</span><span class="sxs-lookup"><span data-stu-id="b69d7-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="b69d7-122">As etapas seguidas para se preparar para um encerramento incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b69d7-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="b69d7-123">Pare a desfragmentação online se ela estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="b69d7-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="b69d7-124">Iniciar uma limpeza do repositório de versão.</span><span class="sxs-lookup"><span data-stu-id="b69d7-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="b69d7-125">Reduza a profundidade do ponto de verificação iniciando a liberação de páginas sujas no Gerenciador de buffer.</span><span class="sxs-lookup"><span data-stu-id="b69d7-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="b69d7-126">Impeça chamadas futuras para a maioria das funções para essa instância.</span><span class="sxs-lookup"><span data-stu-id="b69d7-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="b69d7-127">Se essa função falhar, nenhuma das etapas para se preparar para um encerramento da instância será realizada, portanto, nenhuma alteração no estado da instância ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="b69d7-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b69d7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b69d7-128">Remarks</span></span>

<span data-ttu-id="b69d7-129">Essa função reduzirá o trabalho que a instância terá que fazer quando for encerrada, mas não encerrará a instância.</span><span class="sxs-lookup"><span data-stu-id="b69d7-129">This function will reduce the work the instance will have to do when terminated but will not terminate the instance.</span></span> <span data-ttu-id="b69d7-130">Como resultado, essa função é apenas uma otimização e não é obrigatória para uso.</span><span class="sxs-lookup"><span data-stu-id="b69d7-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="b69d7-131">Observe que a quantidade de trabalho realizado na preparação era menor no Windows 2000 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b69d7-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="b69d7-132">Depois que a função for realizada com sucesso, a chamada a funções que não são mais permitidas retornará JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="b69d7-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="b69d7-133">As funções que ainda são permitidas após essa chamada são: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="b69d7-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="b69d7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b69d7-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b69d7-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b69d7-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b69d7-136">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b69d7-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b69d7-137"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b69d7-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b69d7-138">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b69d7-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b69d7-139"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b69d7-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b69d7-140">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b69d7-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b69d7-141"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b69d7-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b69d7-142">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b69d7-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b69d7-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b69d7-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b69d7-144">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b69d7-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b69d7-145">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b69d7-145">See Also</span></span>

[<span data-ttu-id="b69d7-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b69d7-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b69d7-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b69d7-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b69d7-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="b69d7-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="b69d7-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b69d7-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b69d7-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="b69d7-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="b69d7-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="b69d7-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="b69d7-152">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="b69d7-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="b69d7-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b69d7-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b69d7-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="b69d7-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="b69d7-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="b69d7-155">JetTerm2</span></span>](./jetterm2-function.md)
