---
description: 'Saiba mais sobre: função JetIntersectIndexes'
title: Função JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761206"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="233d5-103">Função JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="233d5-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="233d5-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="233d5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="233d5-105">Função JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="233d5-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="233d5-106">A função **JetIntersectIndexes** computa a interseção entre vários conjuntos de entradas de índice de índices secundários diferentes na mesma tabela.</span><span class="sxs-lookup"><span data-stu-id="233d5-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="233d5-107">Essa operação é útil para localizar o conjunto de registros em uma tabela que corresponde a dois ou mais critérios que podem ser expressos usando intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="233d5-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="233d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="233d5-108">Parameters</span></span>

<span data-ttu-id="233d5-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="233d5-109">*sesid*</span></span>

<span data-ttu-id="233d5-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="233d5-110">The session to use for this call.</span></span>

<span data-ttu-id="233d5-111">*rgindexrange*</span><span class="sxs-lookup"><span data-stu-id="233d5-111">*rgindexrange*</span></span>

<span data-ttu-id="233d5-112">Um ponteiro para uma matriz de estruturas de [JET_IndexRange](./jet-indexrange-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="233d5-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="233d5-113">Cada estrutura inclui um [JET_TABLEID](./jet-tableid.md) que foi configurado para conter um dos intervalos de índice a serem interseccionados.</span><span class="sxs-lookup"><span data-stu-id="233d5-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="233d5-114">Para obter mais informações, consulte [JET_IndexRange](./jet-indexrange-structure.md).</span><span class="sxs-lookup"><span data-stu-id="233d5-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="233d5-115">*cindexrange*</span><span class="sxs-lookup"><span data-stu-id="233d5-115">*cindexrange*</span></span>

<span data-ttu-id="233d5-116">O número de estruturas de [JET_IndexRange](./jet-indexrange-structure.md) na matriz contida no parâmetro *rgindexrange* .</span><span class="sxs-lookup"><span data-stu-id="233d5-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="233d5-117">*precabolist*</span><span class="sxs-lookup"><span data-stu-id="233d5-117">*precordlist*</span></span>

<span data-ttu-id="233d5-118">Ponteiro para uma estrutura de [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="233d5-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="233d5-119">Essa estrutura será preenchida com informações suficientes para atravessar a tabela temporária com os resultados de **JetIntersectIndexes**.</span><span class="sxs-lookup"><span data-stu-id="233d5-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="233d5-120">O buffer de saída que recebe uma estrutura de [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="233d5-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="233d5-121">A estrutura contém uma descrição do conjunto de resultados da interseção.</span><span class="sxs-lookup"><span data-stu-id="233d5-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="233d5-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="233d5-122">*grbit*</span></span>

<span data-ttu-id="233d5-123">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="233d5-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="233d5-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="233d5-124">Return Value</span></span>

<span data-ttu-id="233d5-125">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="233d5-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="233d5-126">Para obter mais informações sobre erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="233d5-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="233d5-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="233d5-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="233d5-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="233d5-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="233d5-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="233d5-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="233d5-130">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="233d5-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="233d5-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="233d5-132">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="233d5-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="233d5-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="233d5-134">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="233d5-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="233d5-135"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="233d5-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="233d5-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="233d5-137">Uma das opções solicitadas era inválida, foi usada incorretamente ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="233d5-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="233d5-138">Esse erro é retornado por <strong>JetIntersectIndexes</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="233d5-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="233d5-139">O <em>grbit</em> contido na estrutura de <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> apontada por qualquer elemento na matriz <em>rgindexrange</em> não é igual a JET_bitRecordInIndex.</span><span class="sxs-lookup"><span data-stu-id="233d5-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="233d5-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="233d5-141">Um dos parâmetros fornecidos contém um valor inesperado ou um valor que é inconsistente quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="233d5-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="233d5-142">Esse erro é retornado por <strong>JetIntersectIndexes</strong> pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="233d5-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="233d5-143">O parâmetro <em>precabolist</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="233d5-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="233d5-144">O membro <strong>cbStruct</strong> da estrutura de <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> especificada no parâmetro <em>precabolist</em> não é igual ao tamanho da estrutura de <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="233d5-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="233d5-145">O parâmetro <em>cindexrange</em> é zero.</span><span class="sxs-lookup"><span data-stu-id="233d5-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="233d5-146">O parâmetro <em>cindexrange</em> é maior que 64.</span><span class="sxs-lookup"><span data-stu-id="233d5-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="233d5-147">O membro <strong>cbStruct</strong> para qualquer elemento na matriz especificado pelo parâmetro <em>rgindexrange</em> não é igual ao tamanho da estrutura de <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="233d5-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="233d5-148">Os elementos na matriz <em>rgindexrange</em> contêm <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s de tabelas diferentes.</span><span class="sxs-lookup"><span data-stu-id="233d5-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="233d5-149">Um elemento na matriz <em>rgindexrange</em> contém um <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> que não está posicionado em um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="233d5-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="233d5-150">Um ou mais dos elementos na matriz <em>rgindexrange</em> contêm <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s posicionados no mesmo índice secundário.</span><span class="sxs-lookup"><span data-stu-id="233d5-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="233d5-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="233d5-152">O identificador de sessão é inválido ou se refere a uma sessão fechada.</span><span class="sxs-lookup"><span data-stu-id="233d5-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="233d5-153">Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="233d5-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="233d5-154">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="233d5-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="233d5-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="233d5-156">Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="233d5-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="233d5-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="233d5-158">A operação falhou porque o mecanismo não pôde alocar os recursos necessários para abrir um novo cursor.</span><span class="sxs-lookup"><span data-stu-id="233d5-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="233d5-159">Os recursos de cursor são configurados chamando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <em>JET_paramMaxCursors</em> especificado no parâmetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="233d5-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="233d5-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="233d5-161">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="233d5-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="233d5-162"><strong>JetIntersectIndexes</strong> pode retornar JET_errOutOfMemory se o espaço de endereço do processo do host se tornar muito fragmentado.</span><span class="sxs-lookup"><span data-stu-id="233d5-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="233d5-163">O Gerenciador de tabela temporária sempre alocará um bloco de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="233d5-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="233d5-164"><strong>JetIntersectIndexes</strong> criará uma tabela temporária para cada <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> especificado no parâmetro <em>rgindexrange</em> e uma tabela temporária para a saída em <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="233d5-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="233d5-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="233d5-166">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="233d5-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="233d5-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="233d5-168">É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="233d5-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="233d5-169"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="233d5-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="233d5-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="233d5-171">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="233d5-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="233d5-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="233d5-173">A operação falhou porque o mecanismo não pôde alocar os recursos necessários para armazenar em cache os índices da tabela.</span><span class="sxs-lookup"><span data-stu-id="233d5-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="233d5-174">O número de índices cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <em>JET_paramMaxOpenTables</em> especificado no parâmetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="233d5-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="233d5-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="233d5-176">A operação falhou porque o mecanismo não pôde alocar os recursos necessários para armazenar em cache o esquema da tabela.</span><span class="sxs-lookup"><span data-stu-id="233d5-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="233d5-177">O número de tabelas cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <em>JET_paramMaxOpenTables</em> especificado no parâmetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="233d5-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="233d5-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="233d5-179">A operação falhou porque o mecanismo não pôde alocar os recursos necessários para criar uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="233d5-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="233d5-180">Os recursos de tabela temporária são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com JET_paramMaxTemporaryTables especificado no parâmetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="233d5-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="233d5-181">Em caso de sucesso, uma nova tabela temporária é retornada contendo os indicadores dos registros que correspondem aos critérios representados por cada uma das descrições de intervalo de índice de entrada.</span><span class="sxs-lookup"><span data-stu-id="233d5-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="233d5-182">Em caso de falha, a tabela temporária que contém os resultados não será criada.</span><span class="sxs-lookup"><span data-stu-id="233d5-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="233d5-183">O estado do banco de dados temporário pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="233d5-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="233d5-184">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="233d5-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="233d5-185">A posição atual das [JET_TABLEID](./jet-tableid.md)s fornecidas para essa função pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="233d5-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="233d5-186">Comentários</span><span class="sxs-lookup"><span data-stu-id="233d5-186">Remarks</span></span>

<span data-ttu-id="233d5-187">**JetIntersectIndexes** pode ser usado para filtrar com eficiência os registros em uma tabela por vários critérios se esses critérios puderem ser expressos em termos dos índices secundários nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="233d5-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="233d5-188">Por exemplo, considere que você tem uma tabela muito grande que contém pessoas.</span><span class="sxs-lookup"><span data-stu-id="233d5-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="233d5-189">A tabela pode ter colunas para sua ID de usuário, nome, sobrenome e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="233d5-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="233d5-190">Suponha que cada uma dessas colunas seja indexada separadamente e que o índice principal da tabela esteja acima da ID de usuário. Se você quisesse encontrar todos cujo primeiro nome começa com um e cujo sobrenome começa com G, você executaria as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="233d5-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="233d5-191">Abra um novo cursor na tabela e defina esse cursor para usar o índice na coluna "First Name".</span><span class="sxs-lookup"><span data-stu-id="233d5-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="233d5-192">Em seguida, configure um intervalo de índice para todas as pessoas cujo "primeiro nome" seja iniciado com ' A ' e crie um [JET_IndexRange](./jet-indexrange-structure.md) struct que contenha esse cursor.</span><span class="sxs-lookup"><span data-stu-id="233d5-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="233d5-193">Repita a etapa 1 com um novo cursor no índice "Last Name" para todas as pessoas cujo "Last Name" começou com "G".</span><span class="sxs-lookup"><span data-stu-id="233d5-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="233d5-194">Passe esses critérios para **JetIntersectIndexes** para computar o resultado em uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="233d5-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="233d5-195">Percorra a tabela temporária e recupere cada um dos registros que passam os critérios por indicador.</span><span class="sxs-lookup"><span data-stu-id="233d5-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="233d5-196">A tabela temporária que contém o conjunto de resultados é uma tabela simples com uma coluna que contém o indicador de cada registro que passou todos os critérios usados para calcular a interseção.</span><span class="sxs-lookup"><span data-stu-id="233d5-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="233d5-197">O conjunto de resultados é classificado na mesma ordem que o índice primário e não contém entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="233d5-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="233d5-198">O aplicativo pode enumerar os resultados da interseção enumerando as linhas na tabela temporária, recuperando o indicador para cada resultado usando [JetRetrieveColumn](./jetretrievecolumn-function.md)e, em seguida, visitando o registro no banco de dados chamando [JetGotoBookmark](./jetgotobookmark-function.md) com esse indicador em um cursor posicionado no índice primário.</span><span class="sxs-lookup"><span data-stu-id="233d5-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="233d5-199">A tabela temporária retornada por **JetIntersectIndexes** só pode ser verificada em uma direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="233d5-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="233d5-200">Ele também deve ser fechado por meio de [JetCloseTable](./jetclosetable-function.md) quando a verificação for concluída.</span><span class="sxs-lookup"><span data-stu-id="233d5-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="233d5-201">Para obter mais informações sobre tabelas temporárias e como elas funcionam, consulte [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="233d5-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="233d5-202">O **JetIntersectIndexes** geralmente é uma maneira eficiente e conveniente de filtrar registros com base em vários critérios indexados.</span><span class="sxs-lookup"><span data-stu-id="233d5-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="233d5-203">No entanto, há algumas dicas importantes que devem ser seguidas para maximizar a utilidade desse recurso.</span><span class="sxs-lookup"><span data-stu-id="233d5-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="233d5-204">Se você souber que um dos critérios é tão restritivo que o intervalo de índice resultante tem poucos registros, é provável que seja melhor simplesmente percorrer esse intervalo de índice e filtrar os registros no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="233d5-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="233d5-205">Além disso, se você souber que tem critérios muito menos restritivos do que outros critérios em sua interseção, você pode considerar descartar os critérios muito menos restritivos da interseção.</span><span class="sxs-lookup"><span data-stu-id="233d5-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="233d5-206">Por fim, se você souber que um dos critérios não é tão restritivo, de modo que o intervalo de índice resultante seja quase tão grande quanto o índice primário, é improvável que a interseção com esse intervalo de índice se beneficiará (reduza o tamanho do) do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="233d5-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="233d5-207">Em todos os casos, você deve estar selecionando critérios de uma maneira que utilizará o menor número possível de entradas de índice na entrada e gerará o conjunto mais específico de indicadores na saída para o desempenho máximo.</span><span class="sxs-lookup"><span data-stu-id="233d5-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="233d5-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="233d5-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="233d5-209"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="233d5-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="233d5-210">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="233d5-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-211"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="233d5-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="233d5-212">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="233d5-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-213"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="233d5-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="233d5-214">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="233d5-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233d5-215"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="233d5-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="233d5-216">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="233d5-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233d5-217"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="233d5-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="233d5-218">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="233d5-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="233d5-219">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="233d5-219">See Also</span></span>

[<span data-ttu-id="233d5-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="233d5-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="233d5-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="233d5-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="233d5-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="233d5-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="233d5-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="233d5-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="233d5-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="233d5-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="233d5-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="233d5-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="233d5-226">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="233d5-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="233d5-227">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="233d5-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="233d5-228">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="233d5-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
