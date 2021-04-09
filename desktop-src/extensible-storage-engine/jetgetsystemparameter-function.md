---
description: 'Saiba mais sobre: função JetGetSystemParameter'
title: Função JetGetSystemParameter
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171340"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="35992-103">Função JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="35992-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="35992-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="35992-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="35992-105">Função JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="35992-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="35992-106">A função **JetGetSystemParameter** lê as várias definições de configuração do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35992-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="35992-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35992-107">Parameters</span></span>

<span data-ttu-id="35992-108">*cópia*</span><span class="sxs-lookup"><span data-stu-id="35992-108">*instance*</span></span>

<span data-ttu-id="35992-109">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="35992-109">The instance to use for this call.</span></span>

<span data-ttu-id="35992-110">Para o Windows 2000, esse parâmetro é ignorado e sempre deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="35992-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="35992-111">Para o Windows XP e versões posteriores, esse parâmetro é um pouco sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="35992-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="35992-112">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="35992-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="35992-113">Em qualquer um dos casos, todas as configurações de parâmetro do sistema são lidas a partir dessa instância.</span><span class="sxs-lookup"><span data-stu-id="35992-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="35992-114">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro poderá ser **nulo** ou um ponteiro para uma instância criada usando [JetInit](./jetinit-function.md) ou [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="35992-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="35992-115">Quando esse parâmetro for **nulo** , a configuração do parâmetro do sistema global (ou padrão) será lida.</span><span class="sxs-lookup"><span data-stu-id="35992-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="35992-116">Quando esse parâmetro for uma instância, a configuração de parâmetro do sistema para essa instância será lida.</span><span class="sxs-lookup"><span data-stu-id="35992-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="35992-117">*sesid*</span><span class="sxs-lookup"><span data-stu-id="35992-117">*sesid*</span></span>

<span data-ttu-id="35992-118">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="35992-118">The session to use for this call.</span></span>

<span data-ttu-id="35992-119">Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.</span><span class="sxs-lookup"><span data-stu-id="35992-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="35992-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="35992-120">*paramid*</span></span>

<span data-ttu-id="35992-121">A ID do parâmetro do sistema que será lido.</span><span class="sxs-lookup"><span data-stu-id="35992-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="35992-122">Consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter uma lista completa de parâmetros do sistema e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="35992-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="35992-123">*plParam*</span><span class="sxs-lookup"><span data-stu-id="35992-123">*plParam*</span></span>

<span data-ttu-id="35992-124">O buffer de saída que recebe o valor do parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="35992-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="35992-125">*szParam*</span><span class="sxs-lookup"><span data-stu-id="35992-125">*szParam*</span></span>

<span data-ttu-id="35992-126">O buffer de saída que recebe o valor do parâmetro do sistema selecionado se o parâmetro do sistema for de um tipo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35992-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="35992-127">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="35992-127">*cbMax*</span></span>

<span data-ttu-id="35992-128">O tamanho máximo em bytes do buffer de saída da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35992-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="35992-129">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="35992-129">Return Value</span></span>

<span data-ttu-id="35992-130">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="35992-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="35992-131">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35992-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35992-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="35992-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="35992-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="35992-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35992-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="35992-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="35992-135">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="35992-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="35992-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="35992-137">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="35992-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="35992-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="35992-139">Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="35992-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="35992-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="35992-141">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="35992-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="35992-142">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="35992-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="35992-144">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="35992-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="35992-145">Isso pode ocorrer para <strong>JetGetSystemParameter</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="35992-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="35992-146">A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="35992-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="35992-147">O parâmetro do sistema especificado requer que o buffer de saída inteiro seja fornecido e o ponteiro do buffer de saída era <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="35992-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="35992-148">O parâmetro do sistema especificado requer que um buffer de saída de cadeia de caracteres seja fornecido e o ponteiro do buffer de saída era <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="35992-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="35992-149"><strong>Windows Vista:  </strong> Isso só pode acontecer no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="35992-150">O parâmetro do sistema especificado requer que um buffer de saída de cadeia de caracteres seja fornecido e o tamanho desse buffer de saída seja muito pequeno para aceitar uma cadeia de caracteres terminada em NULL.</span><span class="sxs-lookup"><span data-stu-id="35992-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="35992-151"><strong>Windows Vista:  </strong> Isso só pode acontecer no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="35992-152">O parâmetro do sistema especificado não pode ser lido porque é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="35992-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="35992-153">O parâmetro do sistema especificado é global somente e foi feita uma tentativa de ler um valor específico de instância para esse parâmetro de sistema.</span><span class="sxs-lookup"><span data-stu-id="35992-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="35992-154">Isso só pode acontecer no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="35992-155">O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de ler o valor global para esse parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="35992-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="35992-156">Isso só pode acontecer no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="35992-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="35992-158">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="35992-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="35992-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="35992-160">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="35992-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="35992-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="35992-162">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="35992-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="35992-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="35992-164">O identificador de sessão é inválido ou se refere a uma sessão fechada.</span><span class="sxs-lookup"><span data-stu-id="35992-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="35992-165">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="35992-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="35992-166">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="35992-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="35992-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="35992-168">O identificador de instância é inválido ou se refere a uma instância que foi desligada.</span><span class="sxs-lookup"><span data-stu-id="35992-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="35992-169">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="35992-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="35992-170">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="35992-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="35992-171"><strong>Windows Vista:  </strong> Esse erro só será retornado pelo Windows Vista e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="35992-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="35992-173">A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber a configuração de parâmetro do sistema inteira.</span><span class="sxs-lookup"><span data-stu-id="35992-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="35992-174">O buffer de saída foi preenchido com a maior parte da configuração de parâmetro do sistema que se ajustaria.</span><span class="sxs-lookup"><span data-stu-id="35992-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="35992-175">Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres nesse buffer de saída será terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="35992-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="35992-176"><strong>Observação  </strong> Esse erro não é retornado por todas as versões.</span><span class="sxs-lookup"><span data-stu-id="35992-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="35992-177">Consulte a seção comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="35992-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="35992-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="35992-179">A operação falhou porque o buffer de saída era muito pequeno para receber a configuração do parâmetro do sistema inteiro.</span><span class="sxs-lookup"><span data-stu-id="35992-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="35992-180"><strong>Observação  </strong> Esse erro não é retornado em alguns casos para preservar a compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="35992-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="35992-181">Consulte a seção comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="35992-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="35992-182"><strong>Windows Vista:  </strong> Esse erro só será retornado pelo Windows Vista e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="35992-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35992-183">Em caso de sucesso, o buffer de saída apropriado para o parâmetro do sistema solicitado será definido como o valor desse parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="35992-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="35992-184">Em caso de falha, o estado dos buffers de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="35992-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="35992-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="35992-185">Remarks</span></span>

<span data-ttu-id="35992-186">Há um problema importante nessa API que está presente em todas as versões.</span><span class="sxs-lookup"><span data-stu-id="35992-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="35992-187">Se um parâmetro do sistema com um valor de cadeia de caracteres for solicitado e o buffer de saída for muito pequeno para receber a configuração inteira de parâmetro do sistema, JET_wrnBufferTruncated não será retornado.</span><span class="sxs-lookup"><span data-stu-id="35992-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="35992-188">JET_errSuccess é retornado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="35992-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="35992-189">Se o comprimento da cadeia de caracteres retornada for igual ao tamanho do buffer de saída menos o terminador **NULL** , o chamador deverá reagir como se JET_wrnBufferTruncated fossem retornadas.</span><span class="sxs-lookup"><span data-stu-id="35992-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="35992-190">Se um buffer de saída de cadeia de caracteres de tamanho zero for especificado, o chamador deverá reagir como se JET_errInvalidParameter fosse retornado.</span><span class="sxs-lookup"><span data-stu-id="35992-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="35992-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35992-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35992-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="35992-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35992-193">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="35992-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-194"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="35992-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35992-195">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="35992-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-196"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="35992-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35992-197">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="35992-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-198"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="35992-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="35992-199">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="35992-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35992-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="35992-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="35992-201">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="35992-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35992-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="35992-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="35992-203">Implementado como <strong>JetGetSystemParameterW</strong> (Unicode) e <strong>JetGetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="35992-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="35992-204">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="35992-204">See Also</span></span>

[<span data-ttu-id="35992-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="35992-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="35992-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35992-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="35992-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="35992-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="35992-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="35992-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="35992-209">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="35992-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="35992-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="35992-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="35992-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="35992-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="35992-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="35992-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="35992-213">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="35992-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
