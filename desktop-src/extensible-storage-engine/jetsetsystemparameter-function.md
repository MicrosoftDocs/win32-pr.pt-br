---
description: 'Saiba mais sobre: função JetSetSystemParameter'
title: Função JetSetSystemParameter
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164631"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="a4eee-103">Função JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a4eee-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="a4eee-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a4eee-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="a4eee-105">Função JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a4eee-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="a4eee-106">A função **JetSetSystemParameter** é usada para definir as várias definições de configuração do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a4eee-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="a4eee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4eee-107">Parameters</span></span>

<span data-ttu-id="a4eee-108">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="a4eee-108">*pinstance*</span></span>

<span data-ttu-id="a4eee-109">Especifica a instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="a4eee-110">**Windows 2000:**  Para o Windows 2000, esse parâmetro é ignorado e sempre deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a4eee-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="a4eee-111">**Windows XP:**  Para o Windows XP e versões posteriores, esse parâmetro é um pouco sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="a4eee-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="a4eee-112">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="a4eee-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="a4eee-113">Em qualquer um dos casos, todas as configurações de parâmetro do sistema são lidas a partir dessa instância.</span><span class="sxs-lookup"><span data-stu-id="a4eee-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="a4eee-114">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro poderá ser **nulo** ou um ponteiro para uma instância criada usando [JetInit](./jetinit-function.md) ou [JetCreateIndex](./jetcreateindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="a4eee-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="a4eee-115">Quando esse parâmetro for **nulo** , a configuração do parâmetro do sistema global (ou padrão) será lida.</span><span class="sxs-lookup"><span data-stu-id="a4eee-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="a4eee-116">Quando esse parâmetro for uma instância, a configuração de parâmetro do sistema para essa instância será lida.</span><span class="sxs-lookup"><span data-stu-id="a4eee-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="a4eee-117">Embora esse seja tecnicamente um parâmetro out, essa API nunca modifica o conteúdo do buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="a4eee-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="a4eee-118">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a4eee-118">*sesid*</span></span>

<span data-ttu-id="a4eee-119">Especifica a sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="a4eee-120">Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="a4eee-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="a4eee-121">*paramid*</span></span>

<span data-ttu-id="a4eee-122">A ID do parâmetro do sistema que será definido.</span><span class="sxs-lookup"><span data-stu-id="a4eee-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="a4eee-123">Consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter uma lista completa de parâmetros do sistema e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a4eee-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="a4eee-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4eee-124">*lParam*</span></span>

<span data-ttu-id="a4eee-125">Fornece o valor a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="a4eee-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="a4eee-126">*szParam*</span><span class="sxs-lookup"><span data-stu-id="a4eee-126">*szParam*</span></span>

<span data-ttu-id="a4eee-127">Fornece o valor para o parâmetro de sistema selecionado se esse parâmetro de sistema for de um tipo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a4eee-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="a4eee-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a4eee-128">Return Value</span></span>

<span data-ttu-id="a4eee-129">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4eee-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a4eee-130">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a4eee-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4eee-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a4eee-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="a4eee-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4eee-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a4eee-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a4eee-134">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a4eee-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="a4eee-135"><strong>Windows Vista:</strong>  No Windows Vista e versões posteriores, o sucesso pode ser retornado sem uma alteração no valor do parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4eee-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="a4eee-136">Consulte o parâmetro sistema JET_paramEnableAdvanced no tópico <a href="gg269346(v=exchg.10).md">Metaparâmetros</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a4eee-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="a4eee-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="a4eee-138">A instância foi inicializada usando uma chamada para <a href="gg294068(v=exchg.10).md">JetInit</a> e essa operação não pode ser executada como resultado.</span><span class="sxs-lookup"><span data-stu-id="a4eee-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="a4eee-139">Isso pode ocorrer para <strong>JetSetSystemParameter</strong> quando for feita uma tentativa de configurar um parâmetro do sistema depois que uma alteração no seu valor não puder afetar o estado do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a4eee-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a4eee-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a4eee-141">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a4eee-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="a4eee-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="a4eee-143">Os parâmetros de índice de tupla especificados eram ilegais.</span><span class="sxs-lookup"><span data-stu-id="a4eee-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="a4eee-144">Esse erro pode ser retornado por <strong>JetSetSystemParameter</strong> somente ao definir <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> como um valor ilegal.</span><span class="sxs-lookup"><span data-stu-id="a4eee-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="a4eee-145"><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a4eee-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="a4eee-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4eee-147">Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a4eee-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a4eee-149">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="a4eee-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a4eee-150"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a4eee-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a4eee-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a4eee-152">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a4eee-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a4eee-153">Isso pode ocorrer para <strong>JetSetSystemParameter</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="a4eee-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a4eee-154">A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="a4eee-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-155">Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com uma cadeia de caracteres cujo comprimento estava fora do intervalo legal para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a4eee-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-156">Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com um caminho de arquivo em que o comprimento de sua representação de caminho absoluto estava fora do intervalo legal para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a4eee-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="a4eee-157"><strong>Windows Vista:</strong>  Isso só pode acontecer no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a4eee-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-158">Foi feita uma tentativa de definir um parâmetro de sistema com valor inteiro com um inteiro que estava fora do intervalo legal para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a4eee-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-159">Foi feita uma tentativa de definir JET_paramUnicodeIndexDefault com um ponteiro de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> <strong>nulo</strong> , um LCID inválido ou um conjunto sem suporte de sinalizadores LCMapString.</span><span class="sxs-lookup"><span data-stu-id="a4eee-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="a4eee-160"><strong>Windows Vista:</strong>  Isso só pode acontecer no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a4eee-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-161">O parâmetro de sistema especificado não pode ser definido porque é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a4eee-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-162">Foi feita uma tentativa de definir um parâmetro do sistema depois que <a href="gg294068(v=exchg.10).md">JetInit</a> foi chamado, o mecanismo de banco de dados está no modo de instância única e uma sessão não foi especificada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="a4eee-163"><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a4eee-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-164">O parâmetro do sistema especificado é global somente e foi feita uma tentativa de definir um valor específico de instância para esse parâmetro de sistema.</span><span class="sxs-lookup"><span data-stu-id="a4eee-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="a4eee-165"><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a4eee-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="a4eee-166">O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de definir o valor global para esse parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4eee-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="a4eee-167"><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a4eee-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a4eee-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="a4eee-169">O caminho do sistema de arquivos especificado era inválido.</span><span class="sxs-lookup"><span data-stu-id="a4eee-169">The specified file system path was invalid.</span></span> <span data-ttu-id="a4eee-170">Esse erro pode ser retornado por <strong>JetSetSystemParameter</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a4eee-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="a4eee-171">Por exemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pode retornar esse erro.</span><span class="sxs-lookup"><span data-stu-id="a4eee-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a4eee-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a4eee-173">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a4eee-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4eee-175">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="a4eee-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a4eee-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4eee-177">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a4eee-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a4eee-179">O identificador de sessão é inválido ou se refere a uma sessão fechada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="a4eee-180">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="a4eee-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a4eee-181">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="a4eee-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="a4eee-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="a4eee-183">O identificador de instância é inválido ou se refere a uma instância que foi desligada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="a4eee-184">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="a4eee-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a4eee-185">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="a4eee-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="a4eee-186"><strong>Windows Vista:</strong>  Esse erro só será retornado pelo Windows Vista e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a4eee-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4eee-187">Em caso de sucesso, a configuração do parâmetro System será definida como o valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="a4eee-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="a4eee-188">Em caso de falha, a configuração para o parâmetro do sistema permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="a4eee-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a4eee-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4eee-189">Remarks</span></span>

<span data-ttu-id="a4eee-190">O **JetSetSystemParameter** faz um trabalho insatisfatório de validar a configuração escolhida para cada parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4eee-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="a4eee-191">Deve-se ter cuidado para não confiar nessa validação para impor configurações boas.</span><span class="sxs-lookup"><span data-stu-id="a4eee-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="a4eee-192">Preste muita atenção à descrição de cada parâmetro do sistema e siga essas diretrizes para obter uma boa configuração de parâmetro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4eee-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="a4eee-193">Há um conjunto de parâmetros do sistema que devem ser sempre definidos para garantir que o mecanismo de banco de dados funcione conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="a4eee-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="a4eee-194">Especificamente, todos os parâmetros do sistema que afetam o layout físico dos arquivos usados pelo mecanismo de banco de dados sempre devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a4eee-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="a4eee-195">Para obter mais informações, consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a4eee-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="a4eee-196">Cada parâmetro do sistema tem um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="a4eee-196">Every system parameter has a default value.</span></span> <span data-ttu-id="a4eee-197">Esses valores padrão evoluíram ao longo do tempo e são bastante arbitrários.</span><span class="sxs-lookup"><span data-stu-id="a4eee-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="a4eee-198">É altamente recomendável que um aplicativo avalie todos os valores padrão para garantir que eles sejam apropriados.</span><span class="sxs-lookup"><span data-stu-id="a4eee-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="a4eee-199">Se eles não forem apropriados, eles deverão ser configurados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4eee-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="a4eee-200">Isso é importante, pois muitos desses parâmetros podem afetar significativamente a confiabilidade, o desempenho e a utilização de recursos do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a4eee-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a4eee-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4eee-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a4eee-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a4eee-203">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a4eee-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-204"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a4eee-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a4eee-205">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a4eee-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-206"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a4eee-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a4eee-207">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a4eee-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-208"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a4eee-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a4eee-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a4eee-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4eee-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a4eee-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a4eee-211">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a4eee-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4eee-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a4eee-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a4eee-213">Implementado como <strong>JetSetSystemParameterW</strong> (Unicode) e <strong>JetSetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a4eee-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a4eee-214">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a4eee-214">See Also</span></span>

[<span data-ttu-id="a4eee-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="a4eee-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="a4eee-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a4eee-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a4eee-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a4eee-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a4eee-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a4eee-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a4eee-219">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a4eee-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a4eee-220">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a4eee-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="a4eee-221">JetInit</span><span class="sxs-lookup"><span data-stu-id="a4eee-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="a4eee-222">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="a4eee-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
