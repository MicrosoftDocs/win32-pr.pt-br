---
description: 'Saiba mais sobre: função JetEnumerateColumns'
title: Função JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170541"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="21474-103">Função JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="21474-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="21474-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="21474-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="21474-105">Função JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="21474-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="21474-106">A função **JetEnumerateColumns** recupera com eficiência um conjunto de colunas e seus valores do registro atual de um cursor ou o buffer de cópia desse cursor.</span><span class="sxs-lookup"><span data-stu-id="21474-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="21474-107">As colunas e os valores recuperados podem ser restringidos por uma lista de IDs de coluna, números de *itagSequence* e outras características.</span><span class="sxs-lookup"><span data-stu-id="21474-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="21474-108">Essa API de recuperação de coluna é exclusiva, pois retorna informações na memória alocada dinamicamente que é obtida usando um retorno de chamada compatível de [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="21474-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="21474-109">Essa nova flexibilidade permite a recuperação eficiente de dados de coluna com características específicas (como tamanho e multiplicidade) que são desconhecidos para o chamador.</span><span class="sxs-lookup"><span data-stu-id="21474-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="21474-110">Isso elimina a necessidade de usar os modos de descoberta de [JetRetrieveColumn](./jetretrievecolumn-function.md) para determinar essas características a fim de configurar uma chamada final para [JetRetrieveColumn](./jetretrievecolumn-function.md) que recuperará com êxito os dados desejados.</span><span class="sxs-lookup"><span data-stu-id="21474-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="21474-111">**Windows XP: o JetEnumerateColumns** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21474-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="21474-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21474-112">Parameters</span></span>

<span data-ttu-id="21474-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="21474-113">*sesid*</span></span>

<span data-ttu-id="21474-114">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="21474-114">The session to use for this call.</span></span>

<span data-ttu-id="21474-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="21474-115">*tableid*</span></span>

<span data-ttu-id="21474-116">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="21474-116">The cursor to use for this call.</span></span>

<span data-ttu-id="21474-117">*cEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="21474-117">*cEnumColumnId*</span></span>

<span data-ttu-id="21474-118">Uma matriz de IDs de coluna, cada uma com uma matriz opcional de números *itagSequence* para enumerar.</span><span class="sxs-lookup"><span data-stu-id="21474-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="21474-119">Se *cEnumColumnId* for 0 (zero), então *rgEnumColumnId* será ignorado e todos os valores de coluna serão enumerados e retornados ao chamador.</span><span class="sxs-lookup"><span data-stu-id="21474-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="21474-120">Se um elemento da matriz de ID de coluna se referir a uma ID de coluna 0 (zero), a enumeração dessa coluna será ignorada e um slot correspondente na saída será gerado com um status de coluna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="21474-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="21474-121">Se *ctagSequence* for 0 (zero) para um determinado elemento da matriz de ID de coluna, *rgtagSequence* será ignorado e todos os valores de coluna para essa ID de coluna serão enumerados e retornados ao chamador.</span><span class="sxs-lookup"><span data-stu-id="21474-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="21474-122">Se um elemento de uma matriz de número *itagSequence* se referir a um número de *itagSequence* de 0 (zero), a enumeração desse número de *itagSequence* será ignorada e um slot correspondente na saída será gerado com um status de valor de coluna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="21474-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="21474-123">*rgEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="21474-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="21474-124">Consulte *cEnumColumnId*.</span><span class="sxs-lookup"><span data-stu-id="21474-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="21474-125">*pcEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="21474-125">*pcEnumColumn*</span></span>

<span data-ttu-id="21474-126">Retorna a matriz enumerada de colunas e seus valores na memória alocada por meio do retorno de chamada compatível com *itagSequence* fornecido.</span><span class="sxs-lookup"><span data-stu-id="21474-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="21474-127">Se uma matriz de IDs de coluna for solicitada na entrada, a ordem e o tamanho da matriz de saída refletirão a ordem e o tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="21474-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="21474-128">Da mesma forma, se uma matriz de números *itagSequence* for solicitada para uma ID de coluna específica na entrada, a ordem e o tamanho da matriz de saída de valores de coluna para essa coluna refletirão a ordem e o tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="21474-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="21474-129">Os parâmetros de saída são definidos como 0 (zero) e **nulos** em qualquer erro, exceto JET_errBadColumnId e JET_errColumnNotFound.</span><span class="sxs-lookup"><span data-stu-id="21474-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="21474-130">Quando esses erros são retornados, os dados de saída são válidos e concluídos para todas as identificações de coluna afetadas.</span><span class="sxs-lookup"><span data-stu-id="21474-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="21474-131">O código de status de cada uma das IDs de coluna afetadas é definido como um desses erros para que o chamador possa determinar quais IDs de coluna eram ruins e, potencialmente, tomar uma ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="21474-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="21474-132">*prgEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="21474-132">*prgEnumColumn*</span></span>

<span data-ttu-id="21474-133">Consulte *pcEnumColumn*.</span><span class="sxs-lookup"><span data-stu-id="21474-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="21474-134">*pfnRealloc*</span><span class="sxs-lookup"><span data-stu-id="21474-134">*pfnRealloc*</span></span>

<span data-ttu-id="21474-135">Identifica um retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) e um ponteiro de contexto opcional usado para alocar memória para a matriz de saída de colunas e seus valores.</span><span class="sxs-lookup"><span data-stu-id="21474-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="21474-136">*pvReallocContext*</span><span class="sxs-lookup"><span data-stu-id="21474-136">*pvReallocContext*</span></span>

<span data-ttu-id="21474-137">Consulte *pfnRealloc*.</span><span class="sxs-lookup"><span data-stu-id="21474-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="21474-138">*cbDataMost*</span><span class="sxs-lookup"><span data-stu-id="21474-138">*cbDataMost*</span></span>

<span data-ttu-id="21474-139">Define um limite na quantidade de dados a serem retornados de uma coluna longa de texto longo ou binário longo.</span><span class="sxs-lookup"><span data-stu-id="21474-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="21474-140">Esse parâmetro pode ser usado para impedir a enumeração de um valor de coluna muito grande.</span><span class="sxs-lookup"><span data-stu-id="21474-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="21474-141">Normalmente, essa enumeração pode falhar na chamada à API com JET_errOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="21474-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="21474-142">Se um valor de coluna grande for truncado de tal maneira, o status do valor da coluna será JET_wrnColumnTruncated.</span><span class="sxs-lookup"><span data-stu-id="21474-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="21474-143">*grbit*</span><span class="sxs-lookup"><span data-stu-id="21474-143">*grbit*</span></span>

<span data-ttu-id="21474-144">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="21474-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21474-145">Valor</span><span class="sxs-lookup"><span data-stu-id="21474-145">Value</span></span></p></th>
<th><p><span data-ttu-id="21474-146">Significado</span><span class="sxs-lookup"><span data-stu-id="21474-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21474-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="21474-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="21474-148">Ao enumerar valores de coluna, todas as colunas para as quais estamos recuperando todos os valores e que têm apenas um valor de coluna não nula podem ser retornadas em um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="21474-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="21474-149">O status dessas colunas será definido como JET_wrnColumnSingleValue e o tamanho do valor da coluna e a memória que contém o valor da coluna serão retornados diretamente na estrutura de <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="21474-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="21474-150">Não há garantia de que todas as colunas qualificadas sejam compactadas dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="21474-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="21474-151">Consulte <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="21474-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="21474-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="21474-153">Essa opção indica que os valores de coluna modificados do registro devem ser enumerados em vez dos valores de coluna originais.</span><span class="sxs-lookup"><span data-stu-id="21474-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="21474-154">Se um valor de coluna não tiver sido modificado, o valor da coluna original será enumerado.</span><span class="sxs-lookup"><span data-stu-id="21474-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="21474-155">Dessa forma, um valor de coluna que ainda não foi inserido ou atualizado pode ser enumerado ao inserir ou atualizar um registro.</span><span class="sxs-lookup"><span data-stu-id="21474-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="21474-156">Essa opção é idêntica à JET_bitRetrieveCopy quando usada com <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span><span class="sxs-lookup"><span data-stu-id="21474-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="21474-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="21474-158">Se uma determinada coluna não estiver presente no registro, nenhum valor de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="21474-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="21474-159">Normalmente, o valor padrão para a coluna, se houver, seria retornado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="21474-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="21474-160">É garantido que, se a coluna for definida como um valor diferente do valor padrão, esse valor diferente será retornado (ou seja, se uma coluna com um valor padrão for explicitamente definida como <strong>NULL</strong> , um <strong>NULL</strong> será retornado como o valor dessa coluna).</span><span class="sxs-lookup"><span data-stu-id="21474-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="21474-161">Observe que, mesmo que essa opção seja solicitada, ainda é possível ver um valor de coluna que é igual ao valor padrão.</span><span class="sxs-lookup"><span data-stu-id="21474-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="21474-162">Nenhum esforço é feito para remover valores de coluna que correspondam aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="21474-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="21474-163">É importante observar que essa opção afeta a saída de <strong>JetEnumerateColumns</strong> quando usada com JET_bitEnumeratePresenceOnly ou JET_bitEnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="21474-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="21474-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="21474-165">Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="21474-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="21474-166">Essa opção impedirá o retorno de chamada que computa o valor padrão definido pelo usuário para que a coluna seja chamada ao enumerar os valores para essa coluna.</span><span class="sxs-lookup"><span data-stu-id="21474-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="21474-167"><strong>Windows Server 2003 e anterior:  </strong> Para o Windows Server 2003 e versões anteriores, a operação falhará com JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="21474-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="21474-168"><strong>Windows Server 2003 SP1:  </strong> Esse valor possível só está disponível para o Windows Server 2003 SP1 e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="21474-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="21474-169">Se esse valor possível for especificado e a tabela contiver uma coluna que tenha um valor padrão definido pelo usuário, a operação falhará com JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="21474-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="21474-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="21474-171">Se existir um valor não nulo para o valor de coluna ou coluna solicitado, os dados associados não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="21474-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="21474-172">Em vez disso, o status associado para essa coluna ou valor de coluna será definido como JET_wrnColumnPresent.</span><span class="sxs-lookup"><span data-stu-id="21474-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="21474-173">Se o valor da coluna ou coluna for <strong>nulo</strong> , JET_wrnColumnNull será retornado como de costume.</span><span class="sxs-lookup"><span data-stu-id="21474-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="21474-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="21474-175">Ao enumerar todos os valores de coluna no registro (por exemplo, ou seja, quando <em>cEnumColumnId</em> for zero), somente os valores de coluna marcados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="21474-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="21474-176">Essa opção não é permitida ao enumerar uma matriz específica de IDs de coluna.</span><span class="sxs-lookup"><span data-stu-id="21474-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="21474-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="21474-178"><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21474-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="21474-179">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="21474-179">Return Value</span></span>

<span data-ttu-id="21474-180">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="21474-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="21474-181">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="21474-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21474-182">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="21474-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="21474-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="21474-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21474-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="21474-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="21474-185">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="21474-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="21474-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="21474-187">A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="21474-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="21474-188">Esse erro será retornado por <strong>JetEnumerateColumns</strong> se forem solicitadas IDs de coluna específicas, uma dessas IDs de coluna era inválida e a primeira ID de coluna inválida falhou com esse erro para seu código de status de coluna.</span><span class="sxs-lookup"><span data-stu-id="21474-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="21474-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="21474-190">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="21474-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="21474-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="21474-192">A coluna descrita pela ID de coluna fornecida não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="21474-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="21474-193">Esse erro será retornado por <strong>JetEnumerateColumns</strong> se forem solicitadas IDs de coluna específicas, uma dessas IDs de coluna era inválida e a primeira ID de coluna inválida falhou com esse erro para seu código de status de coluna.</span><span class="sxs-lookup"><span data-stu-id="21474-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="21474-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="21474-195">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="21474-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="21474-196"><strong>Windows XP:  </strong> Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="21474-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="21474-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="21474-198">Uma das opções solicitadas era inválida ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="21474-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="21474-199">Esse erro será retornado por <strong>JetEnumerateColumns</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="21474-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="21474-200">JET_bitEnumerateLocal está especificado.</span><span class="sxs-lookup"><span data-stu-id="21474-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="21474-201">Um <em>grbit</em> inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="21474-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="21474-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="21474-203">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="21474-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="21474-204">Esse erro será retornado por <strong>JetEnumerateColumns</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="21474-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="21474-205"><em>pcEnumColumn</em> é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="21474-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="21474-206"><em>prgEnumColumn</em> é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="21474-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="21474-207"><em>pfnRealloc</em> é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="21474-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="21474-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="21474-209">O cursor não está posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="21474-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="21474-210">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="21474-210">This can happen for many different reasons.</span></span> <span data-ttu-id="21474-211">Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</span><span class="sxs-lookup"><span data-stu-id="21474-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="21474-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="21474-213">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="21474-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="21474-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="21474-215">O cursor está posicionado em um registro que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="21474-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="21474-216">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="21474-216">This can happen for many different reasons.</span></span> <span data-ttu-id="21474-217">O motivo mais comum é que a sessão não está em uma transação, o cursor foi posicionado em um registro, esse registro foi excluído e, em seguida, o cursor tentou fazer referência a esse registro.</span><span class="sxs-lookup"><span data-stu-id="21474-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="21474-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="21474-219">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="21474-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="21474-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="21474-221">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="21474-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="21474-222"><strong>Windows XP:  </strong> Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="21474-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="21474-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="21474-224">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="21474-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="21474-225">Em caso de sucesso, os dados solicitados serão retornados nos buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="21474-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="21474-226">É responsabilidade do chamador liberar qualquer memória alocada por esse retorno de chamada e retornada nos buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="21474-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="21474-227">Essa memória deve ser liberada por meio do retorno de chamada compatível de [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecida.</span><span class="sxs-lookup"><span data-stu-id="21474-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="21474-228">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="21474-228">No change to the database state will occur.</span></span>

<span data-ttu-id="21474-229">Em caso de falha, nenhum dos dados solicitados será retornado.</span><span class="sxs-lookup"><span data-stu-id="21474-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="21474-230">Qualquer memória que foi alocada durante a chamada será liberada automaticamente usando o retorno de chamada compatível de [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido.</span><span class="sxs-lookup"><span data-stu-id="21474-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="21474-231">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="21474-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="21474-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="21474-232">Remarks</span></span>

<span data-ttu-id="21474-233">Se você estiver enumerando todos os valores de coluna no registro e não tiver especificado JET_bitEnumerateIgnoreDefaults, não será possível pressupor que você nunca verá um valor de coluna ou coluna com um código de status de JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="21474-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="21474-234">Você poderá ver esse código de status se uma coluna tiver um valor padrão e tiver sido explicitamente definida como **nula** ou se a coluna for uma coluna não esparsa (por exemplo, uma coluna fixa ou variável).</span><span class="sxs-lookup"><span data-stu-id="21474-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="21474-235">O parâmetro *cbDataMost* não se aplica a todos os valores de coluna.</span><span class="sxs-lookup"><span data-stu-id="21474-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="21474-236">Esse parâmetro truncará apenas os valores de texto longo e de coluna binária longa que são tão grandes que foram armazenados separadamente do registro.</span><span class="sxs-lookup"><span data-stu-id="21474-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="21474-237">Se **JetEnumerateColumns** retornar dados em seus parâmetros de saída, o chamador será responsável por liberar a memória na matriz, bem como qualquer memória referenciada por ponteiros inseridos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="21474-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="21474-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21474-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21474-239"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="21474-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="21474-240">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21474-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-241"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="21474-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="21474-242">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="21474-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-243"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="21474-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="21474-244">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="21474-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21474-245"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="21474-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="21474-246">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="21474-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21474-247"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="21474-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="21474-248">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="21474-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="21474-249">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="21474-249">See Also</span></span>

[<span data-ttu-id="21474-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="21474-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="21474-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="21474-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="21474-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="21474-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="21474-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="21474-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="21474-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="21474-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="21474-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="21474-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="21474-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="21474-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="21474-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="21474-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="21474-258">realloc</span><span class="sxs-lookup"><span data-stu-id="21474-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="21474-259">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="21474-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="21474-260">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="21474-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
