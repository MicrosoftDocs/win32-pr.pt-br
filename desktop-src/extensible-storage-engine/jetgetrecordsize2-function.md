---
description: 'Saiba mais sobre: função JetGetRecordSize2'
title: Função JetGetRecordSize2
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787668"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="d9e81-103">Função JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="d9e81-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="d9e81-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d9e81-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="d9e81-105">Função JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="d9e81-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="d9e81-106">A função **JetGetRecordSize2** recupera informações de tamanho de registro do local desejado.</span><span class="sxs-lookup"><span data-stu-id="d9e81-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="d9e81-107">**Windows 7: o JetGetRecordSize2** é introduzido no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d9e81-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d9e81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9e81-108">Parameters</span></span>

<span data-ttu-id="d9e81-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d9e81-109">*sesid*</span></span>

<span data-ttu-id="d9e81-110">Identifica o contexto de sessão de banco de dados que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d9e81-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="d9e81-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d9e81-111">*tableid*</span></span>

<span data-ttu-id="d9e81-112">Identifica a tabela ou o cursor que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d9e81-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="d9e81-113">O cursor deve ser posicionado em um registro ou ter uma atualização preparada.</span><span class="sxs-lookup"><span data-stu-id="d9e81-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="d9e81-114">*precsize*</span><span class="sxs-lookup"><span data-stu-id="d9e81-114">*precsize*</span></span>

<span data-ttu-id="d9e81-115">Um ponteiro para um buffer de saída para a estrutura de [JET_RECSIZE2](./jet-recsize2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e81-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="d9e81-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d9e81-116">*grbit*</span></span>

<span data-ttu-id="d9e81-117">Este é um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9e81-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9e81-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e81-118">Value</span></span></p></th>
<th><p><span data-ttu-id="d9e81-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d9e81-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="d9e81-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="d9e81-121">Isso recupera o tamanho do registro que está no buffer de cópia preparado para atualização.</span><span class="sxs-lookup"><span data-stu-id="d9e81-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="d9e81-122">Caso contrário, o <em>TableName</em> ou o cursor deve ser posicionado em um registro e esse registro será usado.</span><span class="sxs-lookup"><span data-stu-id="d9e81-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="d9e81-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="d9e81-124">Quando esse bit é especificado, o <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> não é zerado antes de preencher o conteúdo, agindo efetivamente como um acúmulo das estatísticas de vários registros visitados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="d9e81-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="d9e81-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="d9e81-126">Isso faz com que a API ignore valores longos não intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="d9e81-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="d9e81-127">Por exemplo, somente o registro local na página será usado.</span><span class="sxs-lookup"><span data-stu-id="d9e81-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d9e81-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d9e81-128">Return Value</span></span>

<span data-ttu-id="d9e81-129">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9e81-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d9e81-130">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d9e81-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9e81-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d9e81-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="d9e81-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9e81-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d9e81-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d9e81-134">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d9e81-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="d9e81-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="d9e81-136">Uma das opções solicitadas era inválida ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="d9e81-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="d9e81-137">Esse erro será retornado pela função <strong>JetGetRecordSize2</strong> quando um <em>grbit</em> ilegal for especificado.</span><span class="sxs-lookup"><span data-stu-id="d9e81-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d9e81-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d9e81-139">Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="d9e81-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d9e81-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d9e81-141">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d9e81-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d9e81-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d9e81-143">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="d9e81-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d9e81-144"><strong>Windows XP:  </strong> JET_errInstanceUnavailable só será retornada pelo sistema operacional Windows XP e pelas versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d9e81-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d9e81-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d9e81-146">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="d9e81-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d9e81-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d9e81-148">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="d9e81-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d9e81-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d9e81-150">É ilegal usar a mesma sessão para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d9e81-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d9e81-151"><strong>Windows XP:  </strong> JET_errInstanceUnavailable será retornado somente pelo Windows XP e por versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d9e81-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d9e81-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d9e81-153">Isso pode acontecer se o cursor foi posicionado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="d9e81-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="d9e81-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="d9e81-155">Se o cursor não tiver sido posicionado em uma transação, isso poderá acontecer se outro thread excluir o registro de fora desta sessão.</span><span class="sxs-lookup"><span data-stu-id="d9e81-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d9e81-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d9e81-157">Isso pode ser retornado se um <strong></strong><em>precsize</em> nulo foi passado.</span><span class="sxs-lookup"><span data-stu-id="d9e81-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d9e81-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9e81-158">Remarks</span></span>

<span data-ttu-id="d9e81-159">O tamanho da chave acumulada no campo **cbOverhead** de [JET_RECSIZE2](./jet-recsize2-structure.md), é afetado pelo JET_bitRecordSizeInCopyBuffer.</span><span class="sxs-lookup"><span data-stu-id="d9e81-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="d9e81-160">Se esse bit for especificado, o tamanho da chave acumulado no campo **cbOverhead** será o tamanho de chave completo.</span><span class="sxs-lookup"><span data-stu-id="d9e81-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="d9e81-161">Se esse bit não for usado, o tamanho da chave acumulado não incluirá nenhum tamanho salvo devido à compactação de prefixo de chave.</span><span class="sxs-lookup"><span data-stu-id="d9e81-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d9e81-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9e81-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d9e81-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d9e81-164">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d9e81-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-165"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d9e81-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d9e81-166">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d9e81-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-167"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d9e81-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d9e81-168">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d9e81-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9e81-169"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d9e81-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d9e81-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d9e81-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9e81-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d9e81-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d9e81-172">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d9e81-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d9e81-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d9e81-173">See Also</span></span>

[<span data-ttu-id="d9e81-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d9e81-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d9e81-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d9e81-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d9e81-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="d9e81-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="d9e81-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d9e81-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d9e81-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d9e81-178">JET_TABLEID</span></span>](./jet-tableid.md)
