---
description: 'Saiba mais sobre: função JetGetRecordSize'
title: Função JetGetRecordSize
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 255ca71f3b57c0d1f1bc8440a9a6d4697c09c670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922277"
---
# <a name="jetgetrecordsize-function"></a><span data-ttu-id="d8cc1-103">Função JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="d8cc1-103">JetGetRecordSize Function</span></span>


<span data-ttu-id="d8cc1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d8cc1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize-function"></a><span data-ttu-id="d8cc1-105">Função JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="d8cc1-105">JetGetRecordSize Function</span></span>

<span data-ttu-id="d8cc1-106">A função **JetGetRecordSize** recupera informações de tamanho de registro do local desejado.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-106">The **JetGetRecordSize** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="d8cc1-107">**Windows Vista: o JetGetRecordSize** é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-107">**Windows Vista:  JetGetRecordSize** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d8cc1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8cc1-108">Parameters</span></span>

<span data-ttu-id="d8cc1-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d8cc1-109">*sesid*</span></span>

<span data-ttu-id="d8cc1-110">Identifica o contexto de sessão de banco de dados que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="d8cc1-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d8cc1-111">*tableid*</span></span>

<span data-ttu-id="d8cc1-112">Identifica a tabela ou o cursor que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="d8cc1-113">O cursor deve ser posicionado em um registro ou ter uma atualização preparada.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="d8cc1-114">*precsize*</span><span class="sxs-lookup"><span data-stu-id="d8cc1-114">*precsize*</span></span>

<span data-ttu-id="d8cc1-115">Um ponteiro para um buffer de saída para a estrutura de [JET_RECSIZE](./jet-recsize-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d8cc1-115">A pointer to an output buffer for the [JET_RECSIZE](./jet-recsize-structure.md) structure.</span></span>

<span data-ttu-id="d8cc1-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d8cc1-116">*grbit*</span></span>

<span data-ttu-id="d8cc1-117">Este é um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8cc1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d8cc1-118">Value</span></span></p></th>
<th><p><span data-ttu-id="d8cc1-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d8cc1-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="d8cc1-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-121">Isso recupera o tamanho do registro que está no buffer de cópia preparado para atualização.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="d8cc1-122">Caso contrário, o <em>TableName</em> ou o cursor deve ser posicionado em um registro e esse registro será usado.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="d8cc1-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-124">Quando esse bit é especificado, o <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> não é zerado antes de preencher o conteúdo, agindo efetivamente como um acúmulo das estatísticas de vários registros visitados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-124">When this bit is specified, the <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="d8cc1-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-126">Isso faz com que a API ignore valores longos não intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="d8cc1-127">Por exemplo, somente o registro local na página será usado.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d8cc1-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d8cc1-128">Return Value</span></span>

<span data-ttu-id="d8cc1-129">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d8cc1-130">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d8cc1-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8cc1-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8cc1-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="d8cc1-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8cc1-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d8cc1-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-134">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="d8cc1-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-136">Uma das opções solicitadas era inválida ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="d8cc1-137">Esse erro será retornado pela função <strong>JetGetRecordSize</strong> quando um <em>grbit</em> ilegal for especificado.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-137">This error will be returned by the <strong>JetGetRecordSize</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d8cc1-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-139">Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d8cc1-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-141">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d8cc1-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-143">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d8cc1-144"><strong>Windows XP:</strong>  JET_errInstanceUnavailable será retornado somente pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-144"><strong>Windows XP:</strong>  JET_errInstanceUnavailable will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d8cc1-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-146">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d8cc1-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-148">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d8cc1-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-150">É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-150">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d8cc1-151"><strong>Windows XP:</strong>  JET_errInstanceUnavailable será retornado somente pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-151"><strong>Windows XP:</strong>  JET_errInstanceUnavailable will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d8cc1-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-153">Isso pode acontecer se o cursor foi posicionado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="d8cc1-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-155">Se o cursor não tiver sido posicionado em uma transação, isso poderá acontecer se outro thread excluir o registro de fora desta sessão.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d8cc1-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d8cc1-157">Isso pode ser retornado se um <strong></strong><em>precsize</em> nulo foi passado.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d8cc1-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8cc1-158">Remarks</span></span>

<span data-ttu-id="d8cc1-159">O tamanho da chave acumulada no campo **cbOverhead** de [JET_RECSIZE](./jet-recsize-structure.md), é afetado pelo JET_bitRecordSizeInCopyBuffer.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE](./jet-recsize-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="d8cc1-160">Se esse bit for especificado, o tamanho da chave acumulado no campo **cbOverhead** será o tamanho de chave completo.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="d8cc1-161">Se esse bit não for usado, o tamanho da chave acumulado não incluirá nenhum tamanho salvo devido à compactação de prefixo de chave.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-161">If this bit is not used, then the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d8cc1-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8cc1-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d8cc1-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d8cc1-164">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-165"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d8cc1-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d8cc1-166">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-167"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d8cc1-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d8cc1-168">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8cc1-169"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d8cc1-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d8cc1-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8cc1-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d8cc1-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d8cc1-172">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d8cc1-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d8cc1-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d8cc1-173">See Also</span></span>

[<span data-ttu-id="d8cc1-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d8cc1-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d8cc1-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d8cc1-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d8cc1-176">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d8cc1-176">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d8cc1-177">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="d8cc1-177">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="d8cc1-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d8cc1-178">JET_TABLEID</span></span>](./jet-tableid.md)
