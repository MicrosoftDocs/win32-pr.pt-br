---
description: 'Saiba mais sobre: função JetRetrieveColumn'
title: Função JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763325"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="9d93f-103">Função JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="9d93f-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="9d93f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9d93f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="9d93f-105">Função JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="9d93f-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="9d93f-106">A função **JetRetrieveColumn** recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="9d93f-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="9d93f-107">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="9d93f-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="9d93f-108">Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor.</span><span class="sxs-lookup"><span data-stu-id="9d93f-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="9d93f-109">Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="9d93f-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="9d93f-110">Além de recuperar o valor real da coluna, **JetRetrieveColumn** também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</span><span class="sxs-lookup"><span data-stu-id="9d93f-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="9d93f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d93f-111">Parameters</span></span>

<span data-ttu-id="9d93f-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9d93f-112">*sesid*</span></span>

<span data-ttu-id="9d93f-113">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="9d93f-113">The session to use for this call.</span></span>

<span data-ttu-id="9d93f-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9d93f-114">*tableid*</span></span>

<span data-ttu-id="9d93f-115">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="9d93f-115">The cursor to use for this call.</span></span>

<span data-ttu-id="9d93f-116">*columnid*</span><span class="sxs-lookup"><span data-stu-id="9d93f-116">*columnid*</span></span>

<span data-ttu-id="9d93f-117">A [JET_COLUMNID](./jet-columnid.md) da coluna a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="9d93f-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="9d93f-118">Um valor de *columnid* de 0 (zero) pode ser fornecido, o que não se refere a nenhuma coluna individual.</span><span class="sxs-lookup"><span data-stu-id="9d93f-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="9d93f-119">Quando *columnid* 0 (zero) é fornecido, todas as colunas marcadas, esparsas e colunas com valores múltiplos são tratadas como uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="9d93f-120">Isso facilita a recuperação de todas as colunas esparsas que estão presentes em um registro.</span><span class="sxs-lookup"><span data-stu-id="9d93f-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="9d93f-121">*pvData*</span><span class="sxs-lookup"><span data-stu-id="9d93f-121">*pvData*</span></span>

<span data-ttu-id="9d93f-122">O buffer de saída que recebe o valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="9d93f-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="9d93f-123">*cbData*</span></span>

<span data-ttu-id="9d93f-124">O tamanho máximo, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="9d93f-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="9d93f-125">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="9d93f-125">*pcbActual*</span></span>

<span data-ttu-id="9d93f-126">Recebe o tamanho real, em bytes, do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="9d93f-127">Se esse parâmetro for **NULL**, o tamanho real do valor da coluna não será retornado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="9d93f-128">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9d93f-128">*grbit*</span></span>

<span data-ttu-id="9d93f-129">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="9d93f-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d93f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9d93f-130">Value</span></span></p></th>
<th><p><span data-ttu-id="9d93f-131">Significado</span><span class="sxs-lookup"><span data-stu-id="9d93f-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="9d93f-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="9d93f-133">Esse sinalizador faz com que a coluna de recuperação recupere o valor modificado em vez do valor original.</span><span class="sxs-lookup"><span data-stu-id="9d93f-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="9d93f-134">Se o valor não tiver sido modificado, o valor original será recuperado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="9d93f-135">Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado durante a operação de inserção ou atualização de um registro.</span><span class="sxs-lookup"><span data-stu-id="9d93f-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="9d93f-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="9d93f-137">Essa opção é usada para recuperar valores de coluna do índice, se possível, sem acessar o registro.</span><span class="sxs-lookup"><span data-stu-id="9d93f-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="9d93f-138">Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="9d93f-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="9d93f-139">Nos casos em que o valor da coluna original não puder ser recuperado do índice, devido a transformações irreversíveis ou truncamento de dados, o registro será acessado e os dados serão recuperados como normais.</span><span class="sxs-lookup"><span data-stu-id="9d93f-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="9d93f-140">Essa é uma opção de desempenho e só deve ser especificada quando for provável que o valor da coluna possa ser recuperado do índice.</span><span class="sxs-lookup"><span data-stu-id="9d93f-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="9d93f-141">Essa opção não deverá ser especificada se o índice atual for o índice clusterizado, já que as entradas de índice para o índice clusterizado ou primário são os próprios registros.</span><span class="sxs-lookup"><span data-stu-id="9d93f-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="9d93f-142">Esse bit não poderá ser definido se JET_bitRetrieveFromPrimaryBookmark também for definido.</span><span class="sxs-lookup"><span data-stu-id="9d93f-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="9d93f-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="9d93f-144">Essa opção é usada para recuperar valores de coluna do indicador de índice e pode ser diferente do valor de índice quando uma coluna aparece no índice primário e no índice atual.</span><span class="sxs-lookup"><span data-stu-id="9d93f-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="9d93f-145">Essa opção não deverá ser especificada se o índice atual for o índice clusterizado ou primário.</span><span class="sxs-lookup"><span data-stu-id="9d93f-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="9d93f-146">Esse bit não poderá ser definido se JET_bitRetrieveFromIndex também for definido.</span><span class="sxs-lookup"><span data-stu-id="9d93f-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="9d93f-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="9d93f-148">Essa opção é usada para recuperar o número de sequência de um valor de coluna com valores múltiplos em pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="9d93f-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="9d93f-149">Normalmente, o campo itagSequence é uma entrada para recuperar valores de coluna de vários valores de um registro.</span><span class="sxs-lookup"><span data-stu-id="9d93f-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="9d93f-150">No entanto, ao recuperar valores de um índice, também é possível associar a entrada de índice a um número de sequência específico e recuperar esse número de sequência também.</span><span class="sxs-lookup"><span data-stu-id="9d93f-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="9d93f-151">A recuperação do número de sequência pode ser uma operação dispendiosa e só deve ser feita se necessário.</span><span class="sxs-lookup"><span data-stu-id="9d93f-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="9d93f-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="9d93f-153">Essa opção é usada para recuperar valores <strong>nulos</strong> de coluna de vários valores.</span><span class="sxs-lookup"><span data-stu-id="9d93f-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="9d93f-154">Se essa opção não for especificada, os valores <strong>nulos</strong> da coluna com valores múltiplos serão automaticamente ignorados.</span><span class="sxs-lookup"><span data-stu-id="9d93f-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="9d93f-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="9d93f-156">Essa opção afeta apenas as colunas com valores múltiplos e faz com que um valor <strong>nulo</strong> seja retornado quando o número de sequência solicitado é 1 e não há valores definidos para a coluna no registro.</span><span class="sxs-lookup"><span data-stu-id="9d93f-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="9d93f-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="9d93f-158">Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9d93f-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="9d93f-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="9d93f-160">Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9d93f-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="9d93f-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="9d93f-162">Esse sinalizador permitirá a recuperação de um segmento de tupla do índice.</span><span class="sxs-lookup"><span data-stu-id="9d93f-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="9d93f-163">Esse bit deve ser especificado com JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="9d93f-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d93f-164">*pretinfo*</span><span class="sxs-lookup"><span data-stu-id="9d93f-164">*pretinfo*</span></span>

<span data-ttu-id="9d93f-165">Se *pretinfo* for atribuído como **NULL** , a função se comporta como se um *ItagSequence* de 1 e um *ibLongValue* de 0 (zero) fossem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9d93f-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="9d93f-166">Isso faz com que a recuperação de coluna recupere o primeiro valor de uma coluna com vários valores e recupere dados longos no deslocamento 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9d93f-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="9d93f-167">Esse parâmetro é usado para fornecer um ou mais dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="9d93f-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d93f-168">Valor</span><span class="sxs-lookup"><span data-stu-id="9d93f-168">Value</span></span></p></th>
<th><p><span data-ttu-id="9d93f-169">Significado</span><span class="sxs-lookup"><span data-stu-id="9d93f-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-170">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="9d93f-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="9d93f-171">Fornece um deslocamento binário em um valor de coluna longo ao recuperar uma parte de um valor de coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-172">itagSequence</span><span class="sxs-lookup"><span data-stu-id="9d93f-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="9d93f-173">Fornece o número de sequência do valor de coluna com valores múltiplos desejado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="9d93f-174">Observe que esse campo só será definido se o JET_bitRetrieveTag for especificado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="9d93f-175">Caso contrário, ele não será modificado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-176">columnidNextTagged</span><span class="sxs-lookup"><span data-stu-id="9d93f-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="9d93f-177">Retorna a ID de coluna do valor de coluna retornado ao recuperar todas as colunas marcadas, esparsas e com valores múltiplos usando a passagem de <em>columnid</em> de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9d93f-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9d93f-178">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9d93f-178">Return Value</span></span>

<span data-ttu-id="9d93f-179">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d93f-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9d93f-180">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d93f-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d93f-181">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9d93f-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="9d93f-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d93f-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9d93f-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9d93f-184">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9d93f-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="9d93f-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="9d93f-186">A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="9d93f-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="9d93f-188">Um valor de número de sequência de coluna com valores múltiplos inválido foi passado em pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="9d93f-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="9d93f-189">Os valores válidos para os números de sequência de valor de coluna com valores múltiplos são 1 ou mais.</span><span class="sxs-lookup"><span data-stu-id="9d93f-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="9d93f-190">Um valor de 0 (zero) é inválido para esta função.</span><span class="sxs-lookup"><span data-stu-id="9d93f-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9d93f-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9d93f-192">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9d93f-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="9d93f-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="9d93f-194">A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="9d93f-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="9d93f-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="9d93f-196">As colunas indexadas como subcadeias de caracteres não podem ser recuperadas do índice, já que apenas uma pequena parte da coluna está normalmente presente em cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="9d93f-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9d93f-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9d93f-198">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="9d93f-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9d93f-199">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9d93f-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="9d93f-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="9d93f-201">Em alguns casos, o buffer fornecido para a coluna de recuperação deve ser suficientemente dimensionado para retornar qualquer valor do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="9d93f-202">Por exemplo, colunas atualizáveis de caução são ajustadas para serem consistentes para o contexto transacional da sessão de chamada e esse ajuste requer o buffer fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9d93f-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="9d93f-203">Se espaço de buffer insuficiente for fornecido, JET_errInvalidBufferSize será retornado e nenhum dado de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9d93f-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9d93f-205">Um ou mais dos parâmetros fornecidos estão incorretos.</span><span class="sxs-lookup"><span data-stu-id="9d93f-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="9d93f-206">Isso pode acontecer se o retinfo. cbStruct for menor que o tamanho de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="9d93f-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9d93f-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9d93f-208">As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</span><span class="sxs-lookup"><span data-stu-id="9d93f-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9d93f-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9d93f-210">O cursor não está posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="9d93f-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="9d93f-211">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9d93f-211">This can happen for many different reasons.</span></span> <span data-ttu-id="9d93f-212">Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</span><span class="sxs-lookup"><span data-stu-id="9d93f-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9d93f-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9d93f-214">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="9d93f-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9d93f-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d93f-216">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="9d93f-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9d93f-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9d93f-218">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9d93f-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9d93f-219"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9d93f-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9d93f-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d93f-221">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="9d93f-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="9d93f-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="9d93f-223">O valor da coluna inteira não pôde ser recuperado porque o buffer fornecido é menor do que o tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="9d93f-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="9d93f-225">O valor da coluna recuperado é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d93f-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d93f-226">Em caso de sucesso, o valor da coluna para a coluna especificada é copiado para o buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="9d93f-227">Menor que todo o valor da coluna é copiado com o aviso JET_wrnBufferTruncated é retornado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="9d93f-228">Se o *pcbActual* foi fornecido, o tamanho real do valor da coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="9d93f-229">Observe que os valores **nulos** têm comprimento 0 (zero) e, portanto, definirão o tamanho retornado como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9d93f-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="9d93f-230">Se a coluna recuperada tiver sido uma coluna com vários valores e *pretinfo* tiver sido definida, e JET_bitReturnTag for definido como uma opção, o número de sequência do valor da coluna será retornado em pretinfo- \> itagSequence.</span><span class="sxs-lookup"><span data-stu-id="9d93f-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="9d93f-231">Em caso de falha, o local do cursor permanece inalterado e nenhum dado é copiado no buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="9d93f-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9d93f-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d93f-232">Remarks</span></span>

<span data-ttu-id="9d93f-233">Essa chamada é usada apenas uma vez para recuperar dados de tamanho fixo ou conhecido para colunas sem vários valores.</span><span class="sxs-lookup"><span data-stu-id="9d93f-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="9d93f-234">No entanto, quando os dados da coluna são de tamanho desconhecido, essa chamada normalmente é usada duas vezes.</span><span class="sxs-lookup"><span data-stu-id="9d93f-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="9d93f-235">Ele é chamado primeiro para determinar o tamanho dos dados para que ele possa alocar o espaço de armazenamento necessário.</span><span class="sxs-lookup"><span data-stu-id="9d93f-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="9d93f-236">Em seguida, a mesma chamada é feita novamente para recuperar os dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="9d93f-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="9d93f-237">Quando o número real de valores é desconhecido, como uma coluna tem vários valores, a chamada normalmente é usada três vezes.</span><span class="sxs-lookup"><span data-stu-id="9d93f-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="9d93f-238">Primeiro, para obter o número de valores e duas vezes mais para alocar o armazenamento e recuperar os dados reais.</span><span class="sxs-lookup"><span data-stu-id="9d93f-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="9d93f-239">A recuperação de todos os valores de uma coluna com vários valores pode ser feita chamando repetidamente essa função com um valor de pretinfo- \> itagSequence começando em 1 e aumentando em cada chamada subsequente.</span><span class="sxs-lookup"><span data-stu-id="9d93f-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="9d93f-240">O último valor de coluna é conhecido por ser recuperado quando um JET_wrnColumnNull é retornado da função.</span><span class="sxs-lookup"><span data-stu-id="9d93f-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="9d93f-241">Observe que esse método não poderá ser feito se a coluna de vários valores tiver valores **nulos** explícitos definidos em sua sequência de valores, pois esses valores seriam ignorados.</span><span class="sxs-lookup"><span data-stu-id="9d93f-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="9d93f-242">Se um aplicativo desejar recuperar todos os valores de coluna com vários valores, incluindo aqueles explicitamente definidos como **NULL**, [JetRetrieveColumns](./jetretrievecolumns-function.md) deverá ser usado em vez de **JetRetrieveColumn**.</span><span class="sxs-lookup"><span data-stu-id="9d93f-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="9d93f-243">Observe que essa função não retorna o número de valores para uma função com valores múltiplos quando um valor de *itagSequence* de 0 (zero) é fornecido.</span><span class="sxs-lookup"><span data-stu-id="9d93f-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="9d93f-244">Somente [JetRetrieveColumns](./jetretrievecolumns-function.md) retornará o número de valores de um valor de coluna quando um valor de *itagSequence* de 0 (zero) for passado.</span><span class="sxs-lookup"><span data-stu-id="9d93f-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="9d93f-245">Se essa função for chamada no nível de transação 0 (zero), por exemplo, a sessão de chamada não está em uma transação, então uma transação é aberta e fechada dentro da função.</span><span class="sxs-lookup"><span data-stu-id="9d93f-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="9d93f-246">A finalidade disso é retornar resultados consistentes no caso de um valor longo abranger páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9d93f-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="9d93f-247">Observe que a transação é liberada entre chamadas de função e uma série de chamadas para essa função quando a sessão não está em uma transação pode retornar dados atualizados após a primeira chamada para essa função.</span><span class="sxs-lookup"><span data-stu-id="9d93f-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="9d93f-248">O valor padrão da coluna será recuperado quando a coluna não tiver sido definida explicitamente para outro valor, a menos que a opção JET_bitRetrieveIgnoreDefault esteja definida.</span><span class="sxs-lookup"><span data-stu-id="9d93f-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="9d93f-249">Recuperar o valor da coluna AutoIncrement do buffer de cópia antes da inserção é um meio comum de identificar um registro exclusivamente para vinculação ao inserir dados normalizados em várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="9d93f-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="9d93f-250">O valor de incremento automático é alocado quando a operação de inserção é iniciada e pode ser recuperada do buffer de cópia a qualquer momento até que a atualização seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9d93f-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="9d93f-251">Ao recuperar todas as colunas marcadas, com valores múltiplos e esparsos, ao definir *columnid* como 0 (zero), as colunas são recuperadas na ordem *columnid* do menor *columnid* para a *columnid* mais alta.</span><span class="sxs-lookup"><span data-stu-id="9d93f-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="9d93f-252">A mesma ordem dos valores de coluna é retornada cada vez que os valores de coluna são recuperados.</span><span class="sxs-lookup"><span data-stu-id="9d93f-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="9d93f-253">A ordem é determinística.</span><span class="sxs-lookup"><span data-stu-id="9d93f-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9d93f-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d93f-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-255"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9d93f-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9d93f-256">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9d93f-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-257"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9d93f-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9d93f-258">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9d93f-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-259"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9d93f-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9d93f-260">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9d93f-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d93f-261"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="9d93f-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9d93f-262">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9d93f-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d93f-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9d93f-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9d93f-264">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9d93f-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9d93f-265">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9d93f-265">See Also</span></span>

[<span data-ttu-id="9d93f-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9d93f-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9d93f-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9d93f-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9d93f-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9d93f-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9d93f-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9d93f-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9d93f-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="9d93f-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="9d93f-271">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="9d93f-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="9d93f-272">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="9d93f-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
