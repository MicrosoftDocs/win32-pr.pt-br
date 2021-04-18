---
description: 'Saiba mais sobre: função JetSetColumn'
title: Função JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789220"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="b6feb-103">Função JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b6feb-103">JetSetColumn Function</span></span>


<span data-ttu-id="b6feb-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b6feb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="b6feb-105">Função JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b6feb-105">JetSetColumn Function</span></span>

<span data-ttu-id="b6feb-106">A função **JetSetColumn** modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="b6feb-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="b6feb-107">Ele pode substituir um valor existente, adicionar um novo valor a uma sequência de valores em uma coluna com vários valores, remover um valor de uma sequência de valores em uma coluna com vários valores, ou atualizar todo ou parte de um valor longo, uma coluna do tipo [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="b6feb-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="b6feb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6feb-108">Parameters</span></span>

<span data-ttu-id="b6feb-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b6feb-109">*sesid*</span></span>

<span data-ttu-id="b6feb-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-110">The session to use for this call.</span></span>

<span data-ttu-id="b6feb-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b6feb-111">*tableid*</span></span>

<span data-ttu-id="b6feb-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-112">The cursor to use for this call.</span></span>

<span data-ttu-id="b6feb-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="b6feb-113">*columnid*</span></span>

<span data-ttu-id="b6feb-114">A [JET_COLUMNID](./jet-columnid.md) da coluna a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="b6feb-115">Como alternativa, um valor de *columnid* de 0 (zero) pode ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="b6feb-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="b6feb-116">Quando *columnid* 0 (zero) é fornecido, todas as colunas marcadas, as colunas esparsas e de valores múltiplos são tratadas como uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="b6feb-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="b6feb-117">Isso facilita a recuperação de todas as colunas esparsas que estão presentes em um registro.</span><span class="sxs-lookup"><span data-stu-id="b6feb-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="b6feb-118">*pvData*</span><span class="sxs-lookup"><span data-stu-id="b6feb-118">*pvData*</span></span>

<span data-ttu-id="b6feb-119">Buffer de entrada que contém dados a serem usados para o valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="b6feb-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="b6feb-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="b6feb-120">*cbData*</span></span>

<span data-ttu-id="b6feb-121">Tamanho em bytes do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="b6feb-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b6feb-122">*grbit*</span></span>

<span data-ttu-id="b6feb-123">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b6feb-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6feb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b6feb-124">Value</span></span></p></th>
<th><p><span data-ttu-id="b6feb-125">Significado</span><span class="sxs-lookup"><span data-stu-id="b6feb-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="b6feb-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="b6feb-127">Essa opção é usada para acrescentar dados a uma coluna do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="b6feb-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="b6feb-128">O mesmo comportamento pode ser obtido determinando o tamanho do valor longo existente e especificando <em>ibLongValue</em> em <em>psetinfo</em>.</span><span class="sxs-lookup"><span data-stu-id="b6feb-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="b6feb-129">No entanto, é mais simples usar esse <em>grbit</em> , já que saber o tamanho do valor da coluna existente não é necessário.</span><span class="sxs-lookup"><span data-stu-id="b6feb-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="b6feb-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="b6feb-131">Essa opção é usada para substituir o valor longo existente pelos dados fornecidos recentemente.</span><span class="sxs-lookup"><span data-stu-id="b6feb-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="b6feb-132">Quando essa opção é usada, é como se o valor longo existente tiver sido definido como 0 (zero) comprimento antes da definição dos novos dados.</span><span class="sxs-lookup"><span data-stu-id="b6feb-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="b6feb-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="b6feb-134">Essa opção só é aplicável a colunas marcadas, esparsas ou com vários valores.</span><span class="sxs-lookup"><span data-stu-id="b6feb-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="b6feb-135">Faz com que a coluna retorne o valor de coluna padrão em operações de recuperação de coluna subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b6feb-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="b6feb-136">Todos os valores de coluna existentes são removidos.</span><span class="sxs-lookup"><span data-stu-id="b6feb-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="b6feb-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="b6feb-138">Essa opção é usada para forçar um valor longo, as colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, a serem armazenadas separadamente do restante dos dados de registro.</span><span class="sxs-lookup"><span data-stu-id="b6feb-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="b6feb-139">Isso ocorre normalmente quando o tamanho do valor longo impede que ele seja armazenado com os dados de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="b6feb-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="b6feb-140">No entanto, essa opção pode ser usada para forçar o valor longo a ser armazenado separadamente.</span><span class="sxs-lookup"><span data-stu-id="b6feb-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="b6feb-141">Observe que valores longos de quatro bytes de tamanho menor não podem ser forçados a serem separados.</span><span class="sxs-lookup"><span data-stu-id="b6feb-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="b6feb-142">Nesses casos, a opção é ignorada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="b6feb-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="b6feb-144">Essa opção é usada para interpretar o buffer de entrada como um número inteiro de bytes a serem definidos como o comprimento do valor longo descrito pelo <em>columnid</em> fornecido e, se fornecido, o número de sequência em psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="b6feb-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="b6feb-145">Se o tamanho fornecido for maior que o valor da coluna existente, a coluna será estendida com 0s.</span><span class="sxs-lookup"><span data-stu-id="b6feb-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="b6feb-146">Se o tamanho for menor do que o valor da coluna existente, o valor será truncado.</span><span class="sxs-lookup"><span data-stu-id="b6feb-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="b6feb-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="b6feb-148">Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos.</span><span class="sxs-lookup"><span data-stu-id="b6feb-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="b6feb-149">Essa opção compara os dados da coluna de origem, sem nenhuma transformação, com outros valores de coluna existentes e um erro será retornado se uma duplicata for encontrada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="b6feb-150">Se essa opção for fornecida, JET_bitSetAppendLV, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não poderão ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b6feb-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="b6feb-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="b6feb-152">Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos.</span><span class="sxs-lookup"><span data-stu-id="b6feb-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="b6feb-153">Essa opção compara a transformação normalizada da chave de dados de coluna com outros valores de coluna existentes transformados de forma semelhante e um erro será retornado se uma duplicata for encontrada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="b6feb-154">Se essa opção for fornecida, JET_bitSetAppendLV, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não poderão ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b6feb-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="b6feb-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="b6feb-156">Essa opção é usada para definir um valor de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="b6feb-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="b6feb-157">Normalmente, um valor de coluna é definido como <strong>NULL</strong> passando um cbMax de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b6feb-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="b6feb-158">No entanto, para alguns tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, um valor de coluna pode ser 0 (zero), em vez de <strong>NULL</strong>, e essa opção é usada para diferenciar entre <strong>NULL</strong> e 0 (zero) comprimento.</span><span class="sxs-lookup"><span data-stu-id="b6feb-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="b6feb-159"><strong>Observação</strong>  Em geral, se a coluna for uma coluna de comprimento fixo, esse bit será ignorado e a coluna será definida como <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6feb-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="b6feb-160">No entanto, se a coluna for uma coluna marcada de comprimento fixo, o comprimento da coluna será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="b6feb-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="b6feb-161">Quando a coluna marcada de comprimento fixo for definida como 0 comprimento, as tentativas de recuperar a coluna com <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> terão sucesso, mas o comprimento real retornado no parâmetro <em>cbActual</em> será 0.</span><span class="sxs-lookup"><span data-stu-id="b6feb-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="b6feb-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="b6feb-163">Essa opção é usada para armazenar o valor longo inteiro no registro.</span><span class="sxs-lookup"><span data-stu-id="b6feb-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="b6feb-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="b6feb-165">Essa opção é usada para tentar a compactação de dados ao armazenar os dados.</span><span class="sxs-lookup"><span data-stu-id="b6feb-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="b6feb-166"><strong>Windows 7:</strong>  JET_bitSetCompressed é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6feb-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="b6feb-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="b6feb-168">Essa opção não é usada para tentar a compactação durante o armazenamento dos dados.</span><span class="sxs-lookup"><span data-stu-id="b6feb-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="b6feb-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6feb-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6feb-170">*psetinfo*</span><span class="sxs-lookup"><span data-stu-id="b6feb-170">*psetinfo*</span></span>

<span data-ttu-id="b6feb-171">Ponteiro para parâmetros de entrada opcionais que podem ser definidos para essa função usando a estrutura de [JET_SETINFO](./jet-setinfo-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="b6feb-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="b6feb-172">Se *psetinfo* for atribuído como **NULL** , a função se comporta como se um *ItagSequence* de 1 e um *ibLongValue* de 0 (zero) fossem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b6feb-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="b6feb-173">Isso faz com que o conjunto de colunas defina o primeiro valor de uma coluna com valores múltiplos e defina dados longos começando no deslocamento 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b6feb-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="b6feb-174">As seguintes opções podem ser definidas para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="b6feb-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6feb-175">Valor</span><span class="sxs-lookup"><span data-stu-id="b6feb-175">Value</span></span></p></th>
<th><p><span data-ttu-id="b6feb-176">Significado</span><span class="sxs-lookup"><span data-stu-id="b6feb-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-177">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="b6feb-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="b6feb-178">Deslocamento binário em um valor de coluna longo em que os dados definidos devem começar.</span><span class="sxs-lookup"><span data-stu-id="b6feb-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-179">itagSequence</span><span class="sxs-lookup"><span data-stu-id="b6feb-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="b6feb-180">Número de sequência do valor de coluna de valores múltiplos desejado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="b6feb-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="b6feb-181">Se <em>itagSequence</em> for definido como 0 (zero), o valor fornecido deverá ser acrescentado ao final da sequência de valores com vários valors.</span><span class="sxs-lookup"><span data-stu-id="b6feb-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="b6feb-182">Se o número de sequência fornecido for maior do que o último valor de valores múltiplos, o valor especificado será acrescentado ao final da sequência.</span><span class="sxs-lookup"><span data-stu-id="b6feb-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="b6feb-183">Se o número de sequência corresponder a um valor existente, esse valor será substituído pelo valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b6feb-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b6feb-184">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b6feb-184">Return Value</span></span>

<span data-ttu-id="b6feb-185">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6feb-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b6feb-186">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b6feb-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6feb-187">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b6feb-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="b6feb-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6feb-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b6feb-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b6feb-190">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b6feb-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="b6feb-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="b6feb-192">A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="b6feb-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b6feb-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b6feb-194">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b6feb-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="b6feb-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="b6feb-196">A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="b6feb-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="b6feb-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="b6feb-198">Foi feita uma tentativa ilegal de atualizar um valor longo durante uma operação de exclusão de atualização original de cópia de inserção.</span><span class="sxs-lookup"><span data-stu-id="b6feb-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="b6feb-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="b6feb-200">Os dados de valor de coluna fornecidos no buffer de entrada excedem a limitação de tamanho natural para uma coluna de comprimento fixo ou configurados para texto de comprimento fixo ou colunas binárias.</span><span class="sxs-lookup"><span data-stu-id="b6feb-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="b6feb-201">Esse erro também é retornado ao passar mais de 1024 bytes de dados para uma coluna longa e definir o sinalizador de JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="b6feb-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b6feb-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b6feb-203">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="b6feb-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b6feb-204"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="b6feb-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="b6feb-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="b6feb-206">O tamanho de dados do valor da coluna fornecido não corresponde ao que é natural para o tipo de dados de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="b6feb-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="b6feb-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="b6feb-208">Foi feita uma tentativa ilegal de atualizar uma coluna de incremento automático durante uma operação de inserção ou atualização, ou para atualizar uma coluna de versão durante uma operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="b6feb-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="b6feb-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="b6feb-210">As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</span><span class="sxs-lookup"><span data-stu-id="b6feb-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b6feb-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b6feb-212">O psetinfo- &gt; cbStruct fornecido não é um tamanho válido para a estrutura de <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="b6feb-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="b6feb-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b6feb-214">A operação definir coluna tentou criar um valor duplicado e especificou JET_bitSetUniqueMultiValues ou JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="b6feb-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b6feb-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b6feb-216">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="b6feb-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="b6feb-218">Foi feita uma tentativa ilegal de atualizar um valor de coluna longo quando a sessão de chamada não estava em uma transação.</span><span class="sxs-lookup"><span data-stu-id="b6feb-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="b6feb-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="b6feb-220">Foi feita uma tentativa ilegal de definir uma coluna não<strong>nula</strong> como <strong>nula</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6feb-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="b6feb-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="b6feb-222">O mesmo que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="b6feb-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="b6feb-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="b6feb-224">O valor da coluna não pôde ser definido como o valor no buffer de entrada porque ele teria feito com que o registro excedesse sua limitação de tamanho relacionada ao tamanho da página.</span><span class="sxs-lookup"><span data-stu-id="b6feb-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="b6feb-225">As colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> podem ser armazenadas separadamente dos dados de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="b6feb-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="b6feb-226">No entanto, outras colunas devem ser armazenadas com o registro e podem fazer com que a limitação do tamanho do registro seja excedida.</span><span class="sxs-lookup"><span data-stu-id="b6feb-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="b6feb-227">Colunas longas exigem 5 bytes de espaço dentro do registro como uma ligação e isso também pode levar a JET_errRecordTooBig retornando.</span><span class="sxs-lookup"><span data-stu-id="b6feb-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b6feb-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b6feb-229">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="b6feb-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b6feb-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b6feb-231">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b6feb-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b6feb-232"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="b6feb-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b6feb-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b6feb-234">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="b6feb-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="b6feb-236">O cursor não está atualmente no processo de inserir um novo registro ou atualizar um registro existente.</span><span class="sxs-lookup"><span data-stu-id="b6feb-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b6feb-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b6feb-238">Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</span><span class="sxs-lookup"><span data-stu-id="b6feb-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="b6feb-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="b6feb-240">O valor da coluna no buffer de entrada excedeu o comprimento máximo configurado para uma coluna de comprimento variável e foi truncado.</span><span class="sxs-lookup"><span data-stu-id="b6feb-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6feb-241">Em caso de sucesso, a parte desejada de um valor de coluna para a coluna especificada é definida com os dados copiados do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="b6feb-242">O conjunto de dados pode ter sido truncado se ele excedeu o comprimento máximo especificado para uma coluna de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="b6feb-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="b6feb-243">Em caso de falha, o local do cursor permanece inalterado e nenhum dado do valor da coluna é atualizado no buffer de cópia.</span><span class="sxs-lookup"><span data-stu-id="b6feb-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b6feb-244">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6feb-244">Remarks</span></span>

<span data-ttu-id="b6feb-245">Definir valores longos, valores para colunas [JET_coltypLongBinary](./jet-coltyp.md) do tipo [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md), deve ser feito somente quando a sessão de chamada estiver em uma transação.</span><span class="sxs-lookup"><span data-stu-id="b6feb-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="b6feb-246">Se a sessão de chamada não estiver em uma transação, as modificações a valores longos armazenados separadamente poderão ser confirmadas completamente mesmo quando a operação de atualização for cancelada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b6feb-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="b6feb-247">Se a sessão de chamada estiver em uma transação, os efeitos da atualização poderão ser totalmente revertidos cancelando a atualização e revertendo a transação da sessão.</span><span class="sxs-lookup"><span data-stu-id="b6feb-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="b6feb-248">As atualizações de índice não são executadas como resultado de operações de **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="b6feb-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="b6feb-249">Em vez disso, os índices são atualizados somente depois que todas as modificações de coluna são concluídas e [JetUpdate](./jetupdate-function.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="b6feb-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="b6feb-250">Isso permite a atualização mais eficiente de índices quando os índices envolvem mais de uma coluna que está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="b6feb-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="b6feb-251">Um registro é limitado em tamanho com base no tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b6feb-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="b6feb-252">Todos os valores longos no registro com mais de cinco bytes serão armazenados separados do registro se os dados no registro excederem seu limite como resultado de uma operação **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="b6feb-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="b6feb-253">O erro JET_errRecordTooBig será retornado somente depois que todos os dados da coluna de registro separáveis tiverem sido armazenados separadamente do registro e o registro ainda exceder o limite de tamanho do registro.</span><span class="sxs-lookup"><span data-stu-id="b6feb-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b6feb-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6feb-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-255"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b6feb-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b6feb-256">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b6feb-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-257"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b6feb-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b6feb-258">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b6feb-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-259"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b6feb-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b6feb-260">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b6feb-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6feb-261"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b6feb-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b6feb-262">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b6feb-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6feb-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b6feb-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b6feb-264">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b6feb-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b6feb-265">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b6feb-265">See Also</span></span>

[<span data-ttu-id="b6feb-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="b6feb-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="b6feb-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b6feb-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b6feb-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b6feb-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b6feb-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b6feb-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b6feb-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="b6feb-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="b6feb-271">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b6feb-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="b6feb-272">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b6feb-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
