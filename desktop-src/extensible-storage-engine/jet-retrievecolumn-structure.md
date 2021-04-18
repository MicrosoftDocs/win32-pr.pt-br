---
description: 'Saiba mais sobre: estrutura de JET_RETRIEVECOLUMN'
title: Estrutura JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784617"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="5662b-103">Estrutura JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="5662b-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="5662b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5662b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="5662b-105">Estrutura JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="5662b-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="5662b-106">A estrutura de **JET_RETRIEVECOLUMN** contém parâmetros de entrada e saída para [JetRetrieveColumns](./jetretrievecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="5662b-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="5662b-107">Os campos na estrutura descrevem o valor da coluna a ser recuperado, como recuperá-lo e onde salvar os resultados.</span><span class="sxs-lookup"><span data-stu-id="5662b-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="5662b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5662b-108">Members</span></span>

<span data-ttu-id="5662b-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="5662b-109">**columnid**</span></span>

<span data-ttu-id="5662b-110">O identificador de coluna para a coluna a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="5662b-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="5662b-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="5662b-111">**pvData**</span></span>

<span data-ttu-id="5662b-112">Um ponteiro para começar a armazenar dados recuperados do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="5662b-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="5662b-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="5662b-113">**cbData**</span></span>

<span data-ttu-id="5662b-114">O tamanho da alocação que começa em **pvData**, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5662b-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="5662b-115">A operação de recuperação de coluna não armazenará mais dados em **pvData** do que **cbData**.</span><span class="sxs-lookup"><span data-stu-id="5662b-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="5662b-116">**cbActual**</span><span class="sxs-lookup"><span data-stu-id="5662b-116">**cbActual**</span></span>

<span data-ttu-id="5662b-117">O tamanho, em bytes, dos dados recuperados por uma operação de recuperação de coluna.</span><span class="sxs-lookup"><span data-stu-id="5662b-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="5662b-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="5662b-118">**grbit**</span></span>

<span data-ttu-id="5662b-119">Um grupo de bits que contém as opções de recuperação de coluna, que incluem zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5662b-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5662b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5662b-120">Value</span></span></p></th>
<th><p><span data-ttu-id="5662b-121">Significado</span><span class="sxs-lookup"><span data-stu-id="5662b-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5662b-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="5662b-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="5662b-123">Recupera o valor modificado em vez do valor original.</span><span class="sxs-lookup"><span data-stu-id="5662b-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="5662b-124">Se o valor não tiver sido modificado, o valor original será recuperado.</span><span class="sxs-lookup"><span data-stu-id="5662b-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="5662b-125">Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado quando um registro é inserido ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="5662b-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5662b-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="5662b-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="5662b-127">Recupera valores de coluna do índice sem acessar o registro, se possível.</span><span class="sxs-lookup"><span data-stu-id="5662b-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="5662b-128">Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="5662b-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="5662b-129">Nos casos em que o valor da coluna original não puder ser recuperado do índice, devido a transformações irreversíveis ou truncamento de dados, o registro será acessado e os dados serão recuperados como normais.</span><span class="sxs-lookup"><span data-stu-id="5662b-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="5662b-130">Essa é uma opção de desempenho e só deve ser especificada quando for provável que o valor da coluna possa ser recuperado do índice.</span><span class="sxs-lookup"><span data-stu-id="5662b-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="5662b-131">Essa opção não deverá ser especificada se o índice atual for o índice clusterizado, já que as entradas de índice para o índice clusterizado ou primário são os próprios registros.</span><span class="sxs-lookup"><span data-stu-id="5662b-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="5662b-132">Esse bit não poderá ser definido se JET_bitRetrieveFromPrimaryBookmark também for definido.</span><span class="sxs-lookup"><span data-stu-id="5662b-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5662b-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="5662b-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="5662b-134">Recupera valores de coluna do indicador de índice e pode diferir do valor de índice quando uma coluna aparece no índice primário e no índice atual.</span><span class="sxs-lookup"><span data-stu-id="5662b-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="5662b-135">Essa opção não deverá ser especificada se o índice atual for o índice clusterizado ou primário.</span><span class="sxs-lookup"><span data-stu-id="5662b-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="5662b-136">Esse bit não poderá ser definido se JET_bitRetrieveFromIndex também for definido.</span><span class="sxs-lookup"><span data-stu-id="5662b-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5662b-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="5662b-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="5662b-138">Recupera o número de sequência de um valor de coluna com valores múltiplos em pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="5662b-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="5662b-139">O campo itagSequence geralmente é usado como uma entrada para recuperar valores de coluna de vários valores de um registro.</span><span class="sxs-lookup"><span data-stu-id="5662b-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="5662b-140">No entanto, ao recuperar valores de um índice, também é possível associar a entrada de índice a um número de sequência específico e recuperar esse número de sequência também.</span><span class="sxs-lookup"><span data-stu-id="5662b-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="5662b-141">A recuperação do número de sequência pode ser uma operação dispendiosa e só deve ser feita se necessário.</span><span class="sxs-lookup"><span data-stu-id="5662b-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5662b-142">JET_ bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="5662b-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="5662b-143">Recupera valores nulos da coluna de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="5662b-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="5662b-144">Se essa opção não for especificada, os valores nulos da coluna com valores múltiplos serão automaticamente ignorados.</span><span class="sxs-lookup"><span data-stu-id="5662b-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5662b-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="5662b-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="5662b-146">Faz com que um valor nulo seja retornado quando o número de sequência solicitado é 1 e não há valores definidos para a coluna no registro.</span><span class="sxs-lookup"><span data-stu-id="5662b-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="5662b-147">Essa opção afeta apenas as colunas com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="5662b-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5662b-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="5662b-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="5662b-149">Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5662b-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5662b-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="5662b-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="5662b-151">Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5662b-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5662b-152">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="5662b-152">**ibLongValue**</span></span>

<span data-ttu-id="5662b-153">O deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="5662b-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="5662b-154">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="5662b-154">**itagSequence**</span></span>

<span data-ttu-id="5662b-155">O número de sequência dos valores contidos em uma coluna com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="5662b-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="5662b-156">**itagSequence** aqui na **JET_RETRIEVECOLUMN** pode ser 0.</span><span class="sxs-lookup"><span data-stu-id="5662b-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="5662b-157">Se **itagSequence** for 0, o número de instâncias de uma coluna com vários valores será retornado em vez de quaisquer dados de coluna.</span><span class="sxs-lookup"><span data-stu-id="5662b-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="5662b-158">Um valor de **itagSequence** de 0 não pode ser usado em chamadas para [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="5662b-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="5662b-159">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="5662b-159">**columnidNextTagged**</span></span>

<span data-ttu-id="5662b-160">O **columnid** da coluna marcada, com vários valores ou esparsos quando todas as colunas marcadas são recuperadas passando 0 como **columnid** para [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="5662b-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="5662b-161">**erra**</span><span class="sxs-lookup"><span data-stu-id="5662b-161">**err**</span></span>

<span data-ttu-id="5662b-162">Códigos de erro e avisos retornados da recuperação da coluna.</span><span class="sxs-lookup"><span data-stu-id="5662b-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="5662b-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5662b-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5662b-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5662b-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5662b-165">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5662b-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5662b-166"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5662b-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5662b-167">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5662b-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5662b-168"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5662b-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5662b-169">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5662b-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5662b-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5662b-170">See Also</span></span>

[<span data-ttu-id="5662b-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="5662b-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="5662b-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="5662b-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="5662b-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5662b-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5662b-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5662b-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5662b-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="5662b-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="5662b-176">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="5662b-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="5662b-177">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="5662b-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
