---
description: 'Saiba mais sobre: função JetRetrieveColumns'
title: Função JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171617"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="db588-103">Função JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="db588-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="db588-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="db588-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="db588-105">Função JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="db588-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="db588-106">A função **JetRetrieveColumns** recupera vários valores de coluna do registro atual em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="db588-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="db588-107">Uma matriz de estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) é usada para descrever o conjunto de valores de coluna a serem recuperados e para descrever os buffers de saída para cada valor de coluna a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="db588-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="db588-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db588-108">Parameters</span></span>

<span data-ttu-id="db588-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="db588-109">*sesid*</span></span>

<span data-ttu-id="db588-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="db588-110">The session to use for this call.</span></span>

<span data-ttu-id="db588-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="db588-111">*tableid*</span></span>

<span data-ttu-id="db588-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="db588-112">The cursor to use for this call.</span></span>

<span data-ttu-id="db588-113">*pretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="db588-113">*pretrievecolumn*</span></span>

<span data-ttu-id="db588-114">Um ponteiro para uma matriz de uma ou mais estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="db588-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="db588-115">Cada estrutura inclui descrições de qual valor de coluna recuperar e onde armazenar dados retornados.</span><span class="sxs-lookup"><span data-stu-id="db588-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="db588-116">*cretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="db588-116">*cretrievecolumn*</span></span>

<span data-ttu-id="db588-117">O número de estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) na matriz fornecida por *pretrievecolumn*.</span><span class="sxs-lookup"><span data-stu-id="db588-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="db588-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="db588-118">Return Value</span></span>

<span data-ttu-id="db588-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="db588-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="db588-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="db588-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db588-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="db588-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="db588-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="db588-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db588-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="db588-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="db588-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="db588-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="db588-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="db588-126">Um valor de número de sequência de coluna com valores múltiplos inválido foi passado em pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="db588-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="db588-127">Os valores válidos para os números de sequência de valor de coluna com valores múltiplos são 1 ou mais.</span><span class="sxs-lookup"><span data-stu-id="db588-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="db588-128">Um valor de 0 (zero) é válido para essa função, mas é inválido para <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="db588-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="db588-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="db588-130">A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="db588-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="db588-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="db588-132">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="db588-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="db588-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="db588-134">A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="db588-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="db588-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="db588-136">As colunas indexadas como subcadeias de caracteres não podem ser recuperadas do índice, já que apenas uma pequena parte da coluna está normalmente presente em cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="db588-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="db588-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="db588-138">Em alguns casos, o buffer fornecido para a coluna de recuperação deve ser suficientemente dimensionado para retornar qualquer valor do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="db588-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="db588-139">Por exemplo, colunas atualizáveis de caução são ajustadas para serem consistentes para o contexto transacional da sessão de chamada e esse ajuste requer o buffer fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="db588-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="db588-140">Se espaço de buffer insuficiente for fornecido, JET_errInvalidBufferSize será retornado e nenhum dado de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="db588-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="db588-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="db588-142">As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</span><span class="sxs-lookup"><span data-stu-id="db588-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="db588-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="db588-144">Um ou mais dos parâmetros fornecidos estão incorretos.</span><span class="sxs-lookup"><span data-stu-id="db588-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="db588-145">Isso pode acontecer se o retinfo. cbStruct for menor que o tamanho de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="db588-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="db588-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="db588-147">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="db588-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="db588-148"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="db588-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="db588-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="db588-150">O cursor não está posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="db588-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="db588-151">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="db588-151">This can happen for many different reasons.</span></span> <span data-ttu-id="db588-152">Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</span><span class="sxs-lookup"><span data-stu-id="db588-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="db588-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="db588-154">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="db588-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="db588-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="db588-156">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="db588-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="db588-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="db588-158">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="db588-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="db588-159"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="db588-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="db588-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="db588-161">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="db588-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="db588-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="db588-163">O valor da coluna inteira não pôde ser recuperado porque o buffer fornecido é menor do que o tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="db588-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db588-164">Em caso de sucesso, os dados de colunas e o tamanho da coluna são retornados nos buffers fornecidos descritos na matriz de estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="db588-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="db588-165">Se um *itagSequence* foi definido como 0 (zero) para indicar que o número de instâncias de um campo com valores múltiplos foi desejado em vez dos dados da coluna, o número de instâncias de uma coluna com vários valores será retornado no próprio campo *itagSequence* .</span><span class="sxs-lookup"><span data-stu-id="db588-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="db588-166">Cada estrutura de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) tem um campo de erro que contém avisos para a coluna recuperada.</span><span class="sxs-lookup"><span data-stu-id="db588-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="db588-167">Se a coluna fosse um valor **nulo** , o código de erro será definido como JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="db588-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="db588-168">Em caso de falha, o local do cursor permanece inalterado e nenhum dado é copiado no buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="db588-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="db588-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="db588-169">Remarks</span></span>

<span data-ttu-id="db588-170">O **JetRetrieveColumns** dá suporte a um recurso que o [JetRetrieveColumn](./jetretrievecolumn-function.md) não faz.</span><span class="sxs-lookup"><span data-stu-id="db588-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="db588-171">Essa é a capacidade de recuperar o número de instâncias de uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="db588-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="db588-172">A finalidade desse recurso é permitir que um aplicativo Recupere todos os valores de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="db588-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="db588-173">Isso pode ser feito determinando primeiro o número de valores que uma coluna tem.</span><span class="sxs-lookup"><span data-stu-id="db588-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="db588-174">Em seguida, seus comprimentos podem ser determinados chamando **JetRetrieveColumns** novamente com uma estrutura de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) alocada para cada valor para determinar o comprimento dos dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="db588-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="db588-175">Isso pode ser feito passando ponteiros _PvData_ **nulos** com *cbMax* de 0 (zero) e recuperando o comprimento da coluna em *cbActual*.</span><span class="sxs-lookup"><span data-stu-id="db588-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="db588-176">A terceira e última chamada podem ser feitas com memória alocada para os dados de valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="db588-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="db588-177">Se qualquer coluna recuperada for truncada devido a um buffer de comprimento insuficiente, a API retornará JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="db588-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="db588-178">No entanto, outros erros JET_wrnColumnNull são retornados somente no campo de erro em [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="db588-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="db588-179">A razão para isso é que os aplicativos muitas vezes desejam garantir que todos os dados foram recuperados e retornar esse erro do **JetRetrieveColumns** facilite essa compreensão.</span><span class="sxs-lookup"><span data-stu-id="db588-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="db588-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db588-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db588-181"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="db588-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="db588-182">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="db588-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-183"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="db588-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="db588-184">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="db588-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-185"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="db588-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="db588-186">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="db588-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db588-187"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="db588-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="db588-188">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="db588-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db588-189"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="db588-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="db588-190">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="db588-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="db588-191">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="db588-191">See Also</span></span>

[<span data-ttu-id="db588-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="db588-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="db588-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="db588-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="db588-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="db588-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="db588-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="db588-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="db588-196">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="db588-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="db588-197">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="db588-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="db588-198">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="db588-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
