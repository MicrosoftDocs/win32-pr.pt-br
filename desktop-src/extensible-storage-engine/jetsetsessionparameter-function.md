---
description: 'Saiba mais sobre: função JetSetSessionParameter'
title: Função JetSetSessionParameter
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920774"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="01e2b-103">Função JetSetSessionParameter</span><span class="sxs-lookup"><span data-stu-id="01e2b-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="01e2b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="01e2b-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="01e2b-105">A função **JetSetSessionParameter** configura o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="01e2b-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="01e2b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01e2b-106">Parameters</span></span>

<span data-ttu-id="01e2b-107">*sesid*</span><span class="sxs-lookup"><span data-stu-id="01e2b-107">*sesid*</span></span>

<span data-ttu-id="01e2b-108">Especifica a sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="01e2b-109">Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="01e2b-110">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="01e2b-110">*sesparamid*</span></span>

<span data-ttu-id="01e2b-111">A ID do parâmetro de sessão a ser definido.</span><span class="sxs-lookup"><span data-stu-id="01e2b-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="01e2b-112">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="01e2b-112">*pvParam*</span></span>

<span data-ttu-id="01e2b-113">Os dados a serem definidos neste parâmetro de sessão.</span><span class="sxs-lookup"><span data-stu-id="01e2b-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="01e2b-114">*cbParam*</span><span class="sxs-lookup"><span data-stu-id="01e2b-114">*cbParam*</span></span>

<span data-ttu-id="01e2b-115">O tamanho dos dados fornecidos.</span><span class="sxs-lookup"><span data-stu-id="01e2b-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="01e2b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01e2b-116">Return value</span></span>

<span data-ttu-id="01e2b-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01e2b-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="01e2b-118">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="01e2b-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01e2b-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01e2b-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="01e2b-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="01e2b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="01e2b-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="01e2b-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="01e2b-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="01e2b-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="01e2b-124">A instância foi inicializada usando uma chamada para a função <a href="gg294068(v=exchg.10).md">JetInit</a> e essa operação não pode ser executada como resultado.</span><span class="sxs-lookup"><span data-stu-id="01e2b-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="01e2b-125">Isso pode acontecer quando é feita uma tentativa de configurar um parâmetro do sistema depois que uma alteração no valor do parâmetro não pode mais afetar o estado do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="01e2b-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="01e2b-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="01e2b-127">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="01e2b-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="01e2b-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="01e2b-129">Os parâmetros de índice de tupla especificados eram ilegais.</span><span class="sxs-lookup"><span data-stu-id="01e2b-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="01e2b-130">Esse erro é retornado somente quando o parâmetro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>ou <em>JET_paramIndexTuplesToIndexMax</em> é definido como um valor ilegal.</span><span class="sxs-lookup"><span data-stu-id="01e2b-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="01e2b-131">Para obter informações sobre esses parâmetros, consulte <a href="gg294119(v=exchg.10).md">parâmetros de índice</a>.</span><span class="sxs-lookup"><span data-stu-id="01e2b-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="01e2b-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="01e2b-133">Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="01e2b-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="01e2b-135">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="01e2b-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="01e2b-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="01e2b-137">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01e2b-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="01e2b-138">Isso pode acontecer quando ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="01e2b-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="01e2b-139">A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="01e2b-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-140">Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com uma cadeia de caracteres cujo comprimento estava fora do intervalo legal para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01e2b-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-141">Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com um caminho de arquivo em que o comprimento de sua representação de caminho absoluto estava fora do intervalo legal para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01e2b-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-142">Foi feita uma tentativa de definir um parâmetro de sistema com valor inteiro com um inteiro que estava fora do intervalo legal para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01e2b-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-143">Foi feita uma tentativa de definir JET_paramUnicodeIndexDefault com um ponteiro de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> nulo, um LCID inválido ou um conjunto sem suporte de sinalizadores <strong>LCMapString</strong> .</span><span class="sxs-lookup"><span data-stu-id="01e2b-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-144">O parâmetro de sistema especificado não pode ser definido porque é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01e2b-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-145">Foi feita uma tentativa de definir um parâmetro do sistema após a chamada da função <a href="gg294068(v=exchg.10).md">JetInit</a> , o mecanismo de banco de dados está no modo de instância única e não foi especificada uma sessão.</span><span class="sxs-lookup"><span data-stu-id="01e2b-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-146">O parâmetro do sistema especificado é global somente e foi feita uma tentativa de definir um valor específico da instância para esse parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="01e2b-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="01e2b-147">O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de definir o valor global para esse parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="01e2b-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="01e2b-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="01e2b-149">O caminho do sistema de arquivos especificado era inválido.</span><span class="sxs-lookup"><span data-stu-id="01e2b-149">The specified file system path was invalid.</span></span> <span data-ttu-id="01e2b-150">Esse erro pode ser retornado por <strong>JetSetSessionParameter</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="01e2b-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="01e2b-151">Por exemplo, o parâmetro <em>JET_paramSystemPath</em> pode retornar esse erro.</span><span class="sxs-lookup"><span data-stu-id="01e2b-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="01e2b-152">Para obter informações sobre esse parâmetro, consulte <a href="gg269235(v=exchg.10).md">parâmetros do log de transações</a>.</span><span class="sxs-lookup"><span data-stu-id="01e2b-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="01e2b-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="01e2b-154">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="01e2b-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="01e2b-156">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="01e2b-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="01e2b-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="01e2b-158">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="01e2b-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="01e2b-160">O identificador de sessão é inválido ou se refere a uma sessão fechada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="01e2b-161">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="01e2b-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="01e2b-162">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="01e2b-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="01e2b-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="01e2b-164">O identificador de instância é inválido ou se refere a uma instância que foi desligada.</span><span class="sxs-lookup"><span data-stu-id="01e2b-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="01e2b-165">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="01e2b-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="01e2b-166">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="01e2b-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01e2b-167">Em caso de sucesso, o parâmetro do sistema será definido para o valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="01e2b-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="01e2b-168">Se houver falha, o valor do parâmetro do sistema permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="01e2b-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="01e2b-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01e2b-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-170"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="01e2b-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="01e2b-171">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01e2b-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-172"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="01e2b-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="01e2b-173">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="01e2b-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-174"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="01e2b-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="01e2b-175">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="01e2b-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e2b-176"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="01e2b-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="01e2b-177">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="01e2b-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e2b-178"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="01e2b-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="01e2b-179">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="01e2b-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="01e2b-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="01e2b-180">See also</span></span>

[<span data-ttu-id="01e2b-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="01e2b-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="01e2b-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="01e2b-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="01e2b-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="01e2b-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="01e2b-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="01e2b-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="01e2b-185">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="01e2b-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="01e2b-186">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="01e2b-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="01e2b-187">JetInit</span><span class="sxs-lookup"><span data-stu-id="01e2b-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="01e2b-188">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="01e2b-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
