---
description: 'Saiba mais sobre: função JetSetTableSequential'
title: Função JetSetTableSequential
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808334"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="0abde-103">Função JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="0abde-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="0abde-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0abde-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="0abde-105">Função JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="0abde-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="0abde-106">A função **JetSetTableSequential** notifica o mecanismo de banco de dados de que o aplicativo está verificando todo o índice atual que contém um determinado cursor.</span><span class="sxs-lookup"><span data-stu-id="0abde-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="0abde-107">Consequentemente, os métodos usados para acessar os dados do índice serão ajustados para tornar esse cenário o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="0abde-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="0abde-108">**Windows XP:** o **JetSetTableSequential** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="0abde-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="0abde-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0abde-109">Parameters</span></span>

<span data-ttu-id="0abde-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0abde-110">*sesid*</span></span>

<span data-ttu-id="0abde-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="0abde-111">The session to use for this call.</span></span>

<span data-ttu-id="0abde-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0abde-112">*tableid*</span></span>

<span data-ttu-id="0abde-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="0abde-113">The cursor to use for this call.</span></span>

<span data-ttu-id="0abde-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0abde-114">*grbit*</span></span>

<span data-ttu-id="0abde-115">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0abde-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0abde-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0abde-116">Value</span></span></p></th>
<th><p><span data-ttu-id="0abde-117">Significado</span><span class="sxs-lookup"><span data-stu-id="0abde-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0abde-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="0abde-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="0abde-119">Essa opção é usada para indexar na direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="0abde-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="0abde-120"><strong>Windows 7:</strong>o<strong>JET_bitPrereadForward</strong> é introduzido no Windows 7.  </span><span class="sxs-lookup"><span data-stu-id="0abde-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0abde-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="0abde-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="0abde-122">Essa opção é usada para indexar na direção de retrocesso.</span><span class="sxs-lookup"><span data-stu-id="0abde-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="0abde-123"><strong>Windows 7:</strong>o<strong>JET_bitPrereadBackward</strong> é introduzido no Windows 7.  </span><span class="sxs-lookup"><span data-stu-id="0abde-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0abde-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0abde-124">Return Value</span></span>

<span data-ttu-id="0abde-125">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="0abde-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0abde-126">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0abde-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0abde-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0abde-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="0abde-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="0abde-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0abde-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0abde-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0abde-130">A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram desativadas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="0abde-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0abde-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0abde-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0abde-132">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="0abde-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="0abde-133"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0abde-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0abde-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0abde-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0abde-135">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="0abde-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0abde-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0abde-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0abde-137">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="0abde-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0abde-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0abde-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0abde-139">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="0abde-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0abde-140">Se essa função for realizada com sucesso, o índice atual do cursor será otimizado para uma verificação sequencial de todo o índice.</span><span class="sxs-lookup"><span data-stu-id="0abde-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="0abde-141">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="0abde-141">No change to the database state will occur.</span></span>

<span data-ttu-id="0abde-142">Se essa função falhar, nenhuma alteração na configuração do cursor ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="0abde-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="0abde-143">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="0abde-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0abde-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="0abde-144">Remarks</span></span>

<span data-ttu-id="0abde-145">Se o aplicativo precisar examinar com eficiência um subconjunto conhecido de um índice, uma otimização semelhante também será executada sempre que um intervalo de índice for estabelecido usando [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="0abde-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="0abde-146">Essa otimização só está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="0abde-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="0abde-147">Se o aplicativo precisar examinar com eficiência um subconjunto desconhecido de um índice, nenhuma ação deverá ser executada.</span><span class="sxs-lookup"><span data-stu-id="0abde-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="0abde-148">O mecanismo pode detectar automaticamente o comportamento da verificação e buscará os dados antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="0abde-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="0abde-149">No entanto, esse comportamento não é tão agressivo.</span><span class="sxs-lookup"><span data-stu-id="0abde-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="0abde-150">Essa otimização tornará a verificação do índice primário eficiente e fará com que a verificação apenas dos dados de entrada de índice em um índice secundário seja eficiente.</span><span class="sxs-lookup"><span data-stu-id="0abde-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="0abde-151">Ele não fará a verificação de um índice secundário enquanto recupera dados de registro eficientes.</span><span class="sxs-lookup"><span data-stu-id="0abde-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="0abde-152">Isso ocorre porque o mecanismo não executa uma leitura antecipada nos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="0abde-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0abde-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0abde-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0abde-154"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0abde-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0abde-155">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0abde-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0abde-156"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="0abde-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0abde-157">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0abde-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0abde-158"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="0abde-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0abde-159">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0abde-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0abde-160"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="0abde-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0abde-161">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0abde-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0abde-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0abde-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0abde-163">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0abde-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0abde-164">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0abde-164">See Also</span></span>

[<span data-ttu-id="0abde-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0abde-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0abde-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0abde-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0abde-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0abde-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0abde-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0abde-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0abde-169">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="0abde-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="0abde-170">JetStopService</span><span class="sxs-lookup"><span data-stu-id="0abde-170">JetStopService</span></span>](./jetstopservice-function.md)
