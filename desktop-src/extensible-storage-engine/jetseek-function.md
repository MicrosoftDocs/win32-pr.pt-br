---
description: 'Saiba mais sobre: função JetSeek'
title: Função JetSeek
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764144"
---
# <a name="jetseek-function"></a><span data-ttu-id="3d1c6-103">Função JetSeek</span><span class="sxs-lookup"><span data-stu-id="3d1c6-103">JetSeek Function</span></span>


<span data-ttu-id="3d1c6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3d1c6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="3d1c6-105">Função JetSeek</span><span class="sxs-lookup"><span data-stu-id="3d1c6-105">JetSeek Function</span></span>

<span data-ttu-id="3d1c6-106">A função **JetSeek** posiciona com eficiência um cursor para uma entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e à desigualdade especificada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="3d1c6-107">Uma chave de pesquisa deve ter sido construída anteriormente usando [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d1c6-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="3d1c6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d1c6-108">Parameters</span></span>

<span data-ttu-id="3d1c6-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3d1c6-109">*sesid*</span></span>

<span data-ttu-id="3d1c6-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-110">The session to use for this call.</span></span>

<span data-ttu-id="3d1c6-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3d1c6-111">*tableid*</span></span>

<span data-ttu-id="3d1c6-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-112">The cursor to use for this call.</span></span>

<span data-ttu-id="3d1c6-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3d1c6-113">*grbit*</span></span>

<span data-ttu-id="3d1c6-114">Um grupo de bits que contém as opções a serem usadas para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="3d1c6-115">*Grbit* deve ser diferente de zero e deve incluir um ou mais dos valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d1c6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3d1c6-116">Value</span></span></p></th>
<th><p><span data-ttu-id="3d1c6-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3d1c6-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="3d1c6-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-119">Um código de erro especial, JET_wrnUniqueKey, será retornado se puder ser determinado de forma barata que há exatamente uma entrada de índice que corresponde à chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="3d1c6-120">Essa opção é ignorada a menos que JET_bitSeekEQ também seja especificado.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="3d1c6-121">Essa opção só está disponível no Windows Server 2003 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="3d1c6-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-123">O cursor será posicionado na entrada de índice mais próxima do início do índice que corresponde exatamente à chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="3d1c6-124">O início do índice é a entrada de índice que é encontrada ao mover para o primeiro registro nesse índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="3d1c6-125">O início do índice não é o mesmo que o low end do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="3d1c6-126">Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="3d1c6-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-128">O cursor será posicionado na entrada de índice mais próxima do início do índice que seja maior ou igual a uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="3d1c6-129">O início do índice é a entrada de índice que é encontrada ao mover para o primeiro registro nesse índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="3d1c6-130">O início do índice não é o mesmo que o low end do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="3d1c6-131">Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga para localizar entradas de índice mais próximas ao final do índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="3d1c6-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-133">O cursor será posicionado na entrada de índice mais próxima do início do índice que é maior que uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="3d1c6-134">O início do índice é a entrada de índice que é encontrada ao mover para o primeiro registro nesse índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="3d1c6-135">O início do índice não é o mesmo que o low end do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="3d1c6-136">Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga para localizar entradas de índice mais próximas ao início do índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="3d1c6-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-138">O cursor será posicionado na entrada de índice mais próxima do final do índice que for menor ou igual a uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="3d1c6-139">O final do índice é a entrada de índice que é encontrada ao mover para o último registro nesse índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="3d1c6-140">O final do índice não é o mesmo que o alto fim do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="3d1c6-141">Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga para localizar entradas de índice mais próximas ao início do índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="3d1c6-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-143">O cursor será posicionado na entrada de índice mais próxima do final do índice que for menor que uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="3d1c6-144">O final do índice é a entrada de índice que é encontrada ao mover para o último registro nesse índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="3d1c6-145">O final do índice não é o mesmo que o alto fim do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="3d1c6-146">Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga para localizar entradas de índice mais próximas ao final do índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="3d1c6-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-148">Um intervalo de índice será automaticamente configurado para todas as chaves que correspondem exatamente à chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="3d1c6-149">O intervalo de índice resultante é idêntico a um que, de outra forma, teria sido criado por uma chamada para <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> com as opções JET_bitRangeInclusive e JET_bitRangeUpperLimit.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="3d1c6-150">Consulte <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="3d1c6-151">Esse é um método conveniente para descobrir todas as entradas de índice que correspondem aos mesmos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="3d1c6-152">Essa opção é ignorada a menos que JET_bitSeekEQ também seja especificado.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3d1c6-153">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3d1c6-153">Return Value</span></span>

<span data-ttu-id="3d1c6-154">Essa função permite o retorno de qualquer [JET_ERRs](./jet-err.md) definido nesta API.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="3d1c6-155">Para obter mais informações sobre erros do Jet, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3d1c6-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d1c6-156">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3d1c6-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="3d1c6-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d1c6-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3d1c6-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-159">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="3d1c6-160">Para <strong>JetSeek</strong>, isso significa que foi encontrada uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3d1c6-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-162">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3d1c6-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-164">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3d1c6-165">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="3d1c6-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-167">Não há uma chave de pesquisa atual para o cursor.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="3d1c6-168"><strong>JetSeek</strong> exige que o cursor tenha uma chave de pesquisa válida porque usará isso para os critérios de pesquisa usados para localizar entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3d1c6-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-170">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="3d1c6-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-172">Nenhuma entrada de índice correspondente aos critérios de pesquisa foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3d1c6-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-174">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="3d1c6-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-176">Foi encontrada uma entrada de índice que correspondeu aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="3d1c6-177">No entanto, essa entrada de índice não era uma correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3d1c6-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-179">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="3d1c6-180">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3d1c6-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-182">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3d1c6-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="3d1c6-184">Foi encontrada exatamente uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="3d1c6-185">Esse erro só será retornado se JET_bitSeekCheckUniqueness tiver sido especificado e for barato determinar que a entrada de índice correspondente era a única entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="3d1c6-186">Esse erro só será retornado pelo Windows Server 2003 e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d1c6-187">Em caso de sucesso, o cursor será posicionado em uma entrada de índice que corresponda aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="3d1c6-188">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="3d1c6-189">Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="3d1c6-190">Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="3d1c6-191">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-191">No change to the database state will occur.</span></span> <span data-ttu-id="3d1c6-192">Quando várias entradas de índice têm o mesmo valor, a entrada mais próxima ao início do índice é sempre selecionada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="3d1c6-193">Em caso de falha, a posição do cursor permanecerá inalterada, a menos que JET_errRecordNotFound tenha sido retornado.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="3d1c6-194">Nesse caso, o cursor será posicionado onde a entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e a desigualdade especificada teria sido.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="3d1c6-195">O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="3d1c6-196">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="3d1c6-197">Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="3d1c6-198">Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="3d1c6-199">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3d1c6-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1c6-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3d1c6-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1c6-202">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-203"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3d1c6-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1c6-204">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-205"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3d1c6-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1c6-206">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d1c6-207"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3d1c6-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1c6-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d1c6-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3d1c6-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3d1c6-210">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3d1c6-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3d1c6-211">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3d1c6-211">See Also</span></span>

[<span data-ttu-id="3d1c6-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3d1c6-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3d1c6-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3d1c6-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3d1c6-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3d1c6-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3d1c6-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3d1c6-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3d1c6-216">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="3d1c6-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="3d1c6-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="3d1c6-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="3d1c6-218">JetStopService</span><span class="sxs-lookup"><span data-stu-id="3d1c6-218">JetStopService</span></span>](./jetstopservice-function.md)
