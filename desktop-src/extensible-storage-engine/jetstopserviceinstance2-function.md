---
description: 'Saiba mais sobre: função JetStopServiceInstance2'
title: Função JetStopServiceInstance2
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647344"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="3b321-103">Função JetStopServiceInstance2</span><span class="sxs-lookup"><span data-stu-id="3b321-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="3b321-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b321-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="3b321-105">A função **JetStopServiceInstance2** prepara uma instância antes da suspensão e prepara uma instância após a retomada.</span><span class="sxs-lookup"><span data-stu-id="3b321-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="3b321-106">Suspender e retomar são Estados de execução do modelo de ciclo de vida do aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3b321-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="3b321-107">A função **JetStopServiceInstance2** foi introduzida no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3b321-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="3b321-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b321-108">Parameters</span></span>

<span data-ttu-id="3b321-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="3b321-109">*instance*</span></span>

<span data-ttu-id="3b321-110">A instância de destino.</span><span class="sxs-lookup"><span data-stu-id="3b321-110">The target instance.</span></span> <span data-ttu-id="3b321-111">O tipo de dados **JET_INSTANCE** é um identificador para a instância do banco de dado a ser usado para uma chamada para a API do Jet.</span><span class="sxs-lookup"><span data-stu-id="3b321-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="3b321-112">Esse identificador é obtido quando você cria uma instância do banco de dados chamando as funções [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3b321-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="3b321-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3b321-113">*grbit*</span></span>

<span data-ttu-id="3b321-114">Um grupo de bits que especifica um ou mais dos valores listados e definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b321-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b321-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3b321-115">Value</span></span></p></th>
<th><p><span data-ttu-id="3b321-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b321-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b321-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="3b321-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="3b321-118">Interrompe todos os serviços ESE (mecanismo de armazenamento extensível) para a instância especificada.</span><span class="sxs-lookup"><span data-stu-id="3b321-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b321-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="3b321-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="3b321-120">Interrompe tarefas de manutenção em segundo plano especificadas pelo cliente reiniciáveis (desfragmentação da árvore B +, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="3b321-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b321-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="3b321-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="3b321-122">Quiesces todos os caches sujos em disco.</span><span class="sxs-lookup"><span data-stu-id="3b321-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="3b321-123">Esse valor é assíncrono e pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="3b321-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b321-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="3b321-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="3b321-125">Retoma as operações StopService emitidas anteriormente; ou seja, ele reinicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="3b321-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="3b321-126">Esse valor pode ser combinado com o parâmetro <em>grbits</em> para retomar serviços específicos ou com JET_bitStopServiceAll para retomar todos os serviços interrompidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3b321-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="3b321-127">Esse bit só pode ser usado para retomar StopServiceBackgroundUserTasks e JET_bitStopServiceQuiesceCaches.</span><span class="sxs-lookup"><span data-stu-id="3b321-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="3b321-128">Se você tiver chamado anteriormente com JET_bitStopServiceAll, uma tentativa de usar JET_bitStopServiceResume falhará.</span><span class="sxs-lookup"><span data-stu-id="3b321-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="3b321-129">Se a segunda etapa de retomada não for chamada, o aplicativo causará degradação do desempenho.</span><span class="sxs-lookup"><span data-stu-id="3b321-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="3b321-130">Nessa situação, o ponto de verificação é mantido em zero.</span><span class="sxs-lookup"><span data-stu-id="3b321-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3b321-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b321-131">Return value</span></span>

<span data-ttu-id="3b321-132">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b321-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="3b321-133">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b321-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b321-134">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b321-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b321-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b321-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b321-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b321-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b321-137">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3b321-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="3b321-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b321-138">Remarks</span></span>

<span data-ttu-id="3b321-139">Essa função permite que um aplicativo JET mova o cache do banco de dados para um estado limpo ou quase limpo (com o sistema operacional ocioso de e/s), de modo que, se o aplicativo fosse encerrado, a recuperação seria rápida.</span><span class="sxs-lookup"><span data-stu-id="3b321-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="3b321-140">Essa abordagem é preferida sobre o JET de terminação chamando as funções [JetTerm](./jetterm-function.md) ou [JetDetachDatabase](./jetdetachdatabase-function.md) , de modo que, no cenário mais comum, o aplicativo seja simplesmente dessuspenso e, posteriormente, o aplicativo tenha todo o cache e esteja pronto para ser o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="3b321-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="3b321-141">Se essa função for realizada com sucesso, ela prepara o cache do banco de dados para uma suspensão iminente.</span><span class="sxs-lookup"><span data-stu-id="3b321-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="3b321-142">Essa função enfileira trabalhos em um thread de trabalho em segundo plano e retorna ao chamador imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3b321-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="3b321-143">A função deve ser chamada com base no VisibilityNotice de PLM em vez de chamar do manipulador de eventos de suspensão do aplicativo para garantir que o JET tenha tempo para liberar buffers sujos antes de o PLM suspender/encerrar o processo.</span><span class="sxs-lookup"><span data-stu-id="3b321-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="3b321-144">Internamente, o JET dispara um despacho imediato da manutenção do ponto de verificação após a alteração da configuração (ou seja, a atualização do ponto de verificação ou esse novo bit de cache).</span><span class="sxs-lookup"><span data-stu-id="3b321-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="3b321-145">Para obter mais informações sobre eventos VisibilityNotice, consulte [classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span><span class="sxs-lookup"><span data-stu-id="3b321-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="3b321-146">Essa função deve ser chamada duas vezes.</span><span class="sxs-lookup"><span data-stu-id="3b321-146">This function must be called twice.</span></span> <span data-ttu-id="3b321-147">Ele é chamado depois que o aplicativo recebe o aviso de suspensão do sistema operacional, mas antes de o aplicativo ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="3b321-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="3b321-148">Em seguida, ele é chamado novamente depois que o sistema operacional retoma o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b321-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="3b321-149">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3b321-149">For example:</span></span>

<span data-ttu-id="3b321-150">Quando chamado para suspender: JET_ERR JET_API JetStopServiceInstance2 (instância, JET_bitStopServiceQuiesceCaches);</span><span class="sxs-lookup"><span data-stu-id="3b321-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="3b321-151">Quando retomado: JET_ERR JET_API JetStopServiceInstance2 (instância, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);</span><span class="sxs-lookup"><span data-stu-id="3b321-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b321-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b321-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b321-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3b321-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b321-154">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3b321-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b321-155"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3b321-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b321-156">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3b321-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b321-157"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3b321-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b321-158">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3b321-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b321-159"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3b321-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b321-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b321-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b321-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b321-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b321-162">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b321-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b321-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b321-163">See also</span></span>

[<span data-ttu-id="3b321-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b321-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b321-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3b321-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="3b321-166">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="3b321-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="3b321-167">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="3b321-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="3b321-168">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="3b321-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="3b321-169">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="3b321-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="3b321-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="3b321-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="3b321-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="3b321-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="3b321-172">JetTerm</span><span class="sxs-lookup"><span data-stu-id="3b321-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="3b321-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="3b321-173">JetTerm2</span></span>](./jetterm2-function.md)
