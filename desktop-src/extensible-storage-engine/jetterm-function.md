---
description: 'Saiba mais sobre: função JetTerm'
title: Função JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764054"
---
# <a name="jetterm-function"></a><span data-ttu-id="c53e4-103">Função JetTerm</span><span class="sxs-lookup"><span data-stu-id="c53e4-103">JetTerm Function</span></span>


<span data-ttu-id="c53e4-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c53e4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="c53e4-105">Função JetTerm</span><span class="sxs-lookup"><span data-stu-id="c53e4-105">JetTerm Function</span></span>

<span data-ttu-id="c53e4-106">A função **JetTerm** inicia o desligamento de uma instância que foi inicializada pelo [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c53e4-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="c53e4-107">**JetTerm** também pode ser usado para destruir uma instância não inicializada que foi criada pelo [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="c53e4-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="c53e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c53e4-108">Parameters</span></span>

<span data-ttu-id="c53e4-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="c53e4-109">*instance*</span></span>

<span data-ttu-id="c53e4-110">Especifica a instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c53e4-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="c53e4-111">**Windows 2000:**  Esse parâmetro é ignorado e sempre deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c53e4-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="c53e4-112">**Windows XP e versões posteriores:**  Este parâmetro está sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="c53e4-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="c53e4-113">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c53e4-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="c53e4-114">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser um ponteiro para uma instância que foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="c53e4-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="c53e4-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c53e4-115">Return Value</span></span>

<span data-ttu-id="c53e4-116">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="c53e4-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c53e4-117">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c53e4-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c53e4-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c53e4-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c53e4-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c53e4-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c53e4-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c53e4-121">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c53e4-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53e4-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c53e4-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c53e4-123">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="c53e4-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="c53e4-124">Esse erro será retornado por <strong>JetTerm</strong> quando o mecanismo estiver no modo de várias instâncias e quando <em>pinstance</em> se referir a uma instância inválida.</span><span class="sxs-lookup"><span data-stu-id="c53e4-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="c53e4-125"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c53e4-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c53e4-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c53e4-127">A operação não pode ser concluída porque a instância ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="c53e4-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53e4-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c53e4-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c53e4-129">A operação não pode ser concluída porque a instância está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="c53e4-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c53e4-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c53e4-131">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância.</span><span class="sxs-lookup"><span data-stu-id="c53e4-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53e4-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="c53e4-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="c53e4-133">A operação não pode ser concluída porque uma operação de backup está em andamento na instância.</span><span class="sxs-lookup"><span data-stu-id="c53e4-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="c53e4-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="c53e4-135">A instância não pode ser desligada porque existem sessões com transações ativas para a instância especificada.</span><span class="sxs-lookup"><span data-stu-id="c53e4-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="c53e4-136">Esse erro ocorrerá somente se o JET_bitTermComplete for usado.</span><span class="sxs-lookup"><span data-stu-id="c53e4-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c53e4-137">Se essa função for realizada com sucesso, a instância especificada será desligada.</span><span class="sxs-lookup"><span data-stu-id="c53e4-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="c53e4-138">O identificador de instância também será fechado e ficará indisponível para qualquer API que usa um identificador de instância.</span><span class="sxs-lookup"><span data-stu-id="c53e4-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="c53e4-139">Todos os outros objetos associados à instância, como sessões, também serão fechados.</span><span class="sxs-lookup"><span data-stu-id="c53e4-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="c53e4-140">O estado do arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância serão modificados durante o processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="c53e4-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="c53e4-141">Se essa função falhar como resultado de um erro de uso, a instância permanecerá em um estado inicializado e nada será alterado.</span><span class="sxs-lookup"><span data-stu-id="c53e4-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="c53e4-142">Caso contrário, a instância ainda será desligada de acordo com o caso de êxito.</span><span class="sxs-lookup"><span data-stu-id="c53e4-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="c53e4-143">A diferença é que a instância precisará passar pela recuperação de pane quando for inicializada na próxima vez.</span><span class="sxs-lookup"><span data-stu-id="c53e4-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="c53e4-144">O mecanismo tentará liberar o máximo de dados possível para minimizar a quantidade de recuperação necessária.</span><span class="sxs-lookup"><span data-stu-id="c53e4-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="c53e4-145">Conceitualmente, essa falha de **JetTerm** não é diferente de uma falha de processo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c53e4-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="c53e4-146">Remarks</span></span>

<span data-ttu-id="c53e4-147">Se o processo de host de uma instância for encerrado por qualquer motivo antes que **JetTerm** seja chamado com êxito nessa instância, a instância será considerada em um estado de falha.</span><span class="sxs-lookup"><span data-stu-id="c53e4-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="c53e4-148">A recuperação de falha ocorrerá na próxima tentativa de inicializar essa instância.</span><span class="sxs-lookup"><span data-stu-id="c53e4-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c53e4-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c53e4-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c53e4-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c53e4-151">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c53e4-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53e4-152"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c53e4-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c53e4-153">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c53e4-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-154"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c53e4-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c53e4-155">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c53e4-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53e4-156"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="c53e4-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c53e4-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c53e4-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53e4-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c53e4-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c53e4-159">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c53e4-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c53e4-160">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c53e4-160">See Also</span></span>

[<span data-ttu-id="c53e4-161">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="c53e4-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="c53e4-162">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c53e4-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c53e4-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c53e4-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c53e4-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c53e4-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c53e4-165">JetInit</span><span class="sxs-lookup"><span data-stu-id="c53e4-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c53e4-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c53e4-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c53e4-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="c53e4-167">JetTerm2</span></span>](./jetterm2-function.md)
