---
description: 'Saiba mais sobre: função JetEnableMultiInstance'
title: Função JetEnableMultiInstance
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783676"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="f82bd-103">Função JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="f82bd-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="f82bd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f82bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="f82bd-105">Função JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="f82bd-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="f82bd-106">A função **JetEnableMultiInstance** configura o mecanismo de banco de dados para uso com várias instâncias no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="f82bd-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="f82bd-107">Uma matriz opcional de parâmetros globais do sistema está disponível para o primeiro chamador que permite a alteração no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="f82bd-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="f82bd-108">**Windows XP: o JetEnableMultiInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f82bd-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="f82bd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f82bd-109">Parameters</span></span>

<span data-ttu-id="f82bd-110">*psetsysparam*</span><span class="sxs-lookup"><span data-stu-id="f82bd-110">*psetsysparam*</span></span>

<span data-ttu-id="f82bd-111">Uma matriz de parâmetros de sistema global para definir se e somente se o mecanismo entrar no modo de várias instâncias como resultado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="f82bd-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="f82bd-112">Se *csetsysparam* for zero, *psetsysparam* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f82bd-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="f82bd-113">*csetsysparam*</span><span class="sxs-lookup"><span data-stu-id="f82bd-113">*csetsysparam*</span></span>

<span data-ttu-id="f82bd-114">A contagem de elementos para a matriz de parâmetros globais a definir se e somente se o mecanismo entrar no modo de várias instâncias como resultado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="f82bd-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="f82bd-115">Se *csetsysparam* for zero, *psetsysparam* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f82bd-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="f82bd-116">*pcsetsucceed*</span><span class="sxs-lookup"><span data-stu-id="f82bd-116">*pcsetsucceed*</span></span>

<span data-ttu-id="f82bd-117">Um ponteiro para a contagem de parâmetros globais do sistema que foram configurados com êxito como resultado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="f82bd-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="f82bd-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f82bd-118">Return Value</span></span>

<span data-ttu-id="f82bd-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="f82bd-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f82bd-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f82bd-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f82bd-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f82bd-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="f82bd-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="f82bd-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f82bd-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f82bd-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f82bd-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="f82bd-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82bd-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="f82bd-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="f82bd-126">Os parâmetros de índice de tupla especificados não foram permitidos.</span><span class="sxs-lookup"><span data-stu-id="f82bd-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="f82bd-127">Esse erro pode ser retornado por <strong>JetEnableMultiInstance</strong> somente ao definir <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> como um valor ilegal.</span><span class="sxs-lookup"><span data-stu-id="f82bd-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="f82bd-128"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f82bd-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82bd-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="f82bd-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="f82bd-130">O caminho do sistema de arquivos especificado era inválido.</span><span class="sxs-lookup"><span data-stu-id="f82bd-130">The specified file system path was invalid.</span></span> <span data-ttu-id="f82bd-131">Esse erro pode ser retornado por <strong>JetEnableMultiInstance</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f82bd-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="f82bd-132">Por exemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pode retornar esse erro.</span><span class="sxs-lookup"><span data-stu-id="f82bd-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82bd-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f82bd-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f82bd-134">A operação falhou porque ela é inválida quando o mecanismo de banco de dados está operando em modo de instância única (modo de compatibilidade do Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="f82bd-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82bd-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="f82bd-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="f82bd-136"><strong>JetEnableMultiInstance</strong> falhou porque o mecanismo já está no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="f82bd-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="f82bd-137"><strong>Observação  </strong> Isso ocorrerá mesmo que nenhum parâmetro do sistema seja especificado.</span><span class="sxs-lookup"><span data-stu-id="f82bd-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f82bd-138">Se essa função for realizada com sucesso, o mecanismo de banco de dados será configurado para ser executado no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="f82bd-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="f82bd-139">O mecanismo também foi configurado com êxito com a lista opcional de parâmetros globais do sistema.</span><span class="sxs-lookup"><span data-stu-id="f82bd-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="f82bd-140">Se essa função falhar, o mecanismo de banco de dados permanecerá no modo atual.</span><span class="sxs-lookup"><span data-stu-id="f82bd-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="f82bd-141">Se *pcsetsucceed* for diferente de zero, esse número de parâmetros do sistema permanecerá definido.</span><span class="sxs-lookup"><span data-stu-id="f82bd-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f82bd-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="f82bd-142">Remarks</span></span>

<span data-ttu-id="f82bd-143">Essa função só deve ser usada se o aplicativo precisar configurar um determinado conjunto de parâmetros do sistema atomicamente ao configurar o mecanismo de banco de dados para uso em um cenário de vários usuários no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="f82bd-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="f82bd-144">Se outro método de sincronização estiver disponível, é preferível chamar [JetCreateInstance](./jetcreateinstance-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) separadamente.</span><span class="sxs-lookup"><span data-stu-id="f82bd-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f82bd-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f82bd-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f82bd-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f82bd-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f82bd-147">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f82bd-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82bd-148"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f82bd-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f82bd-149">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f82bd-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82bd-150"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="f82bd-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f82bd-151">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f82bd-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82bd-152"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="f82bd-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f82bd-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f82bd-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82bd-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f82bd-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f82bd-155">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f82bd-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82bd-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f82bd-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f82bd-157">Implementado como <strong>JetEnableMultiInstanceW</strong> (Unicode) e <strong>JetEnableMultiInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f82bd-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f82bd-158">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f82bd-158">See Also</span></span>

[<span data-ttu-id="f82bd-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f82bd-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f82bd-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="f82bd-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="f82bd-161">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f82bd-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f82bd-162">JetInit</span><span class="sxs-lookup"><span data-stu-id="f82bd-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="f82bd-163">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="f82bd-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
