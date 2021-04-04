---
description: 'Saiba mais sobre: função JetGotoPosition'
title: Função JetGotoPosition
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646704"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="f98a9-103">Função JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="f98a9-103">JetGotoPosition Function</span></span>


<span data-ttu-id="f98a9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f98a9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="f98a9-105">Função JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="f98a9-105">JetGotoPosition Function</span></span>

<span data-ttu-id="f98a9-106">A função **JetGotoPosition** move um cursor para um novo local que é uma fração do caminho por meio do índice atual.</span><span class="sxs-lookup"><span data-stu-id="f98a9-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="f98a9-107">A fração é aproximadamente igual à seguinte:</span><span class="sxs-lookup"><span data-stu-id="f98a9-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="f98a9-108">precpos- \> centriesLT/precpos- \> centriesTotal</span><span class="sxs-lookup"><span data-stu-id="f98a9-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="f98a9-109">Essa operação é executada em resposta à entrada da caixa de rolagem do usuário que é recebida quando o usuário tenta mostrar dados que iniciam a parte por meio de um conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="f98a9-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="f98a9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f98a9-110">Parameters</span></span>

<span data-ttu-id="f98a9-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f98a9-111">*sesid*</span></span>

<span data-ttu-id="f98a9-112">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="f98a9-112">The session to use for this call.</span></span>

<span data-ttu-id="f98a9-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f98a9-113">*tableid*</span></span>

<span data-ttu-id="f98a9-114">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="f98a9-114">The cursor to use for this call.</span></span>

<span data-ttu-id="f98a9-115">*precpos*</span><span class="sxs-lookup"><span data-stu-id="f98a9-115">*precpos*</span></span>

<span data-ttu-id="f98a9-116">A descrição da fração a ser usada para posicionar o cursor no índice atual.</span><span class="sxs-lookup"><span data-stu-id="f98a9-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="f98a9-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f98a9-117">Return Value</span></span>

<span data-ttu-id="f98a9-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="f98a9-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f98a9-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f98a9-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f98a9-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f98a9-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="f98a9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f98a9-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f98a9-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f98a9-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="f98a9-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98a9-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f98a9-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f98a9-125">A operação não pôde ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f98a9-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f98a9-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f98a9-127">A operação não pôde ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="f98a9-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f98a9-128"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f98a9-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98a9-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f98a9-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f98a9-130">O precpos- &gt; cbStruct fornecido não é um tamanho válido para a estrutura de <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> ou precpos- &gt; centriesLT é maior que precpos- &gt; centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="f98a9-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f98a9-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f98a9-132">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="f98a9-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98a9-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="f98a9-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="f98a9-134">Esse erro será retornado se o índice estiver vazio.</span><span class="sxs-lookup"><span data-stu-id="f98a9-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f98a9-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f98a9-136">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="f98a9-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98a9-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f98a9-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f98a9-138">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="f98a9-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="f98a9-139"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f98a9-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f98a9-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f98a9-141">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="f98a9-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f98a9-142">Se essa função for bem sucedido, o cursor será movido para um registro atual que é uma fração do caminho por meio do índice onde a fração é precpos- \> centriesLT dividida por precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="f98a9-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="f98a9-143">Se essa função falhar, o local do cursor permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="f98a9-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f98a9-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="f98a9-144">Remarks</span></span>

<span data-ttu-id="f98a9-145">Esta operação move o cursor pela tabela para uma posição no seguinte ponto aproximado: precpos- \> centriesLT dividido por precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="f98a9-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="f98a9-146">Quando as atualizações estão ocorrendo continuamente na tabela, as chamadas subsequentes com o mesmo [JET_RECPOS](./jet-recpos-structure.md) podem mover o cursor para posições diferentes no índice, antes e depois da posição anterior.</span><span class="sxs-lookup"><span data-stu-id="f98a9-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="f98a9-147">O isolamento transacional não se aplica ao posicionamento por meio de [JET_RECPOS](./jet-recpos-structure.md) , pois depende das propriedades físicas do índice que não são isoladas da transação.</span><span class="sxs-lookup"><span data-stu-id="f98a9-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="f98a9-148">[JET_RECPOS](./jet-recpos-structure.md) não deve ser usado para descrever um registro em uma tabela ou para reposicionar um registro próximo a um registro existente.</span><span class="sxs-lookup"><span data-stu-id="f98a9-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="f98a9-149">Em vez disso, os indicadores para um registro existente devem ser recuperados após um **JetGotoPosition** inicial e, em seguida, usados para reposicionar o mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="f98a9-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f98a9-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f98a9-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-151"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f98a9-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f98a9-152">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f98a9-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98a9-153"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f98a9-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f98a9-154">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f98a9-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-155"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="f98a9-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f98a9-156">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f98a9-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98a9-157"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="f98a9-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f98a9-158">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f98a9-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98a9-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f98a9-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f98a9-160">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f98a9-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f98a9-161">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f98a9-161">See Also</span></span>

[<span data-ttu-id="f98a9-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f98a9-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f98a9-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f98a9-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f98a9-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f98a9-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f98a9-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f98a9-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f98a9-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="f98a9-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="f98a9-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="f98a9-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)
