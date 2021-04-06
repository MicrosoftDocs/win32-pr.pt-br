---
description: 'Saiba mais sobre: estrutura de JET_SETCOLUMN'
title: Estrutura de JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646904"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="52238-103">Estrutura de JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="52238-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="52238-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52238-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="52238-105">Estrutura de JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="52238-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="52238-106">A estrutura de **JET_SETCOLUMN** contém parâmetros de entrada e saída para [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="52238-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="52238-107">Os campos na estrutura descrevem o valor da coluna a ser definido, como defini-lo e onde obter os dados do conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="52238-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="52238-108">Membros</span><span class="sxs-lookup"><span data-stu-id="52238-108">Members</span></span>

<span data-ttu-id="52238-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="52238-109">**columnid**</span></span>

<span data-ttu-id="52238-110">O identificador de coluna para uma coluna a ser definida.</span><span class="sxs-lookup"><span data-stu-id="52238-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="52238-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="52238-111">**pvData**</span></span>

<span data-ttu-id="52238-112">Um ponteiro para os dados a serem definidos em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="52238-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="52238-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="52238-113">**cbData**</span></span>

<span data-ttu-id="52238-114">O tamanho da alocação, em bytes, começando em **pvData** em bytes.</span><span class="sxs-lookup"><span data-stu-id="52238-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="52238-115">**grbit**</span><span class="sxs-lookup"><span data-stu-id="52238-115">**grbit**</span></span>

<span data-ttu-id="52238-116">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="52238-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52238-117">Valor</span><span class="sxs-lookup"><span data-stu-id="52238-117">Value</span></span></p></th>
<th><p><span data-ttu-id="52238-118">Significado</span><span class="sxs-lookup"><span data-stu-id="52238-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52238-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="52238-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="52238-120">Anexa dados a uma coluna do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="52238-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="52238-121">O mesmo comportamento pode ser obtido determinando o tamanho do valor longo existente e especificando <strong>ibLongValue</strong> em <strong>psetinfo</strong>.</span><span class="sxs-lookup"><span data-stu-id="52238-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="52238-122">No entanto, é mais simples usar esse <em>grbit</em>, já que saber o tamanho do valor da coluna existente não é necessário.</span><span class="sxs-lookup"><span data-stu-id="52238-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52238-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="52238-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="52238-124">Substitui o valor longo existente pelos novos dados.</span><span class="sxs-lookup"><span data-stu-id="52238-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="52238-125">Quando essa opção é usada, é como se o valor longo existente tiver sido definido como 0 (zero) comprimento antes da definição dos novos dados.</span><span class="sxs-lookup"><span data-stu-id="52238-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52238-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="52238-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="52238-127">Interpreta o buffer de entrada como um número inteiro de bytes a serem definidos como o comprimento do valor longo descrito pelo columnid fornecido e, se fornecido, o número de sequência em psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="52238-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="52238-128">Se o tamanho fornecido for maior que o valor da coluna existente, a coluna será estendida com 0s.</span><span class="sxs-lookup"><span data-stu-id="52238-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="52238-129">Se o tamanho for menor do que o valor da coluna existente, o valor será truncado.</span><span class="sxs-lookup"><span data-stu-id="52238-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52238-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="52238-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="52238-131">Define um valor como comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="52238-131">Sets a value to zero length.</span></span> <span data-ttu-id="52238-132">Normalmente, um valor de coluna é definido como NULL passando um cbMax de 0.</span><span class="sxs-lookup"><span data-stu-id="52238-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="52238-133">No entanto, para alguns tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, um valor de coluna pode ter 0 comprimento em vez de NULL, e essa opção é usada para diferenciar entre NULL e 0 comprimento.</span><span class="sxs-lookup"><span data-stu-id="52238-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52238-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="52238-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="52238-135">Força um valor longo, as colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, a serem armazenadas separadamente do restante dos dados de registro.</span><span class="sxs-lookup"><span data-stu-id="52238-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="52238-136">Isso ocorre normalmente quando o tamanho do valor longo impede que ele seja armazenado com os dados de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="52238-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="52238-137">No entanto, essa opção pode ser usada para forçar o valor longo a ser armazenado separadamente.</span><span class="sxs-lookup"><span data-stu-id="52238-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="52238-138">Observe que valores longos de quatro bytes de tamanho ou menores não podem ser forçados a serem separados.</span><span class="sxs-lookup"><span data-stu-id="52238-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="52238-139">Nesses casos, a opção é ignorada.</span><span class="sxs-lookup"><span data-stu-id="52238-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52238-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="52238-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="52238-141">Impõe valores distintos em uma coluna com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="52238-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="52238-142">Essa opção compara os dados da coluna de origem, sem nenhuma transformação, com outros valores de coluna existentes e um erro será retornado se uma duplicata for encontrada.</span><span class="sxs-lookup"><span data-stu-id="52238-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="52238-143">Se essa opção for fornecida, JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não puderem ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="52238-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52238-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="52238-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="52238-145">Impõe valores distintos em uma coluna com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="52238-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="52238-146">Essa opção compara a transformação normalizada da chave de dados de coluna com outros valores de coluna existentes transformados de forma semelhante e um erro será retornado se uma duplicata for encontrada.</span><span class="sxs-lookup"><span data-stu-id="52238-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="52238-147">Se essa opção for fornecida, JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não puderem ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="52238-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52238-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="52238-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="52238-149">Faz com que a coluna retorne o valor de coluna padrão em operações de recuperação de coluna subsequentes.</span><span class="sxs-lookup"><span data-stu-id="52238-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="52238-150">Todos os valores de coluna existentes são removidos.</span><span class="sxs-lookup"><span data-stu-id="52238-150">All existing column values are removed.</span></span> <span data-ttu-id="52238-151">Essa opção só é aplicável a colunas marcadas, esparsas ou com vários valores.</span><span class="sxs-lookup"><span data-stu-id="52238-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52238-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="52238-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="52238-153">Mantém o valor longo, colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou JET_coltypeLongBinary, armazenados com os dados de registro restantes, se possível.</span><span class="sxs-lookup"><span data-stu-id="52238-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="52238-154">Normalmente, as colunas longas são armazenadas separadamente quando seu comprimento excede 1024 bytes ou faria com que o tamanho do registro exceda o limite de tamanho relacionado à página.</span><span class="sxs-lookup"><span data-stu-id="52238-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="52238-155">No entanto, se essa opção for definida, a operação definir coluna falhará com o erro JET_errColumnTooBig em vez de armazenar esse valor de coluna separado dos dados de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="52238-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52238-156">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="52238-156">**ibLongValue**</span></span>

<span data-ttu-id="52238-157">O deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="52238-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="52238-158">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="52238-158">**itagSequence**</span></span>

<span data-ttu-id="52238-159">Descreve o número de sequência do valor em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="52238-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="52238-160">Um **itagSequence** de 0 indica que o valor da coluna definido deve ser adicionado como uma nova instância de uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="52238-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="52238-161">**erra**</span><span class="sxs-lookup"><span data-stu-id="52238-161">**err**</span></span>

<span data-ttu-id="52238-162">Códigos de erro e avisos retornados da operação definir coluna.</span><span class="sxs-lookup"><span data-stu-id="52238-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="52238-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52238-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52238-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="52238-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="52238-165">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="52238-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52238-166"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="52238-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="52238-167">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="52238-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52238-168"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="52238-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="52238-169">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="52238-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="52238-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="52238-170">See Also</span></span>

[<span data-ttu-id="52238-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="52238-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="52238-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="52238-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="52238-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="52238-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="52238-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="52238-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="52238-175">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="52238-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
