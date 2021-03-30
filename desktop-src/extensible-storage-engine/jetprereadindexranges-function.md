---
description: 'Saiba mais sobre: função JetPrereadIndexRanges'
title: Função JetPrereadIndexRanges
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089878"
---
# <a name="jetprereadindexranges-function"></a><span data-ttu-id="77598-103">Função JetPrereadIndexRanges</span><span class="sxs-lookup"><span data-stu-id="77598-103">JetPrereadIndexRanges Function</span></span>


<span data-ttu-id="77598-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77598-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="77598-105">A função **JetPrereadIndexRanges** lê índices para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="77598-105">The **JetPrereadIndexRanges** function prereads indexes to improve the performance.</span></span>

<span data-ttu-id="77598-106">A função **JetPrereadIndexRanges** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77598-106">The **JetPrereadIndexRanges** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="77598-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77598-107">Parameters</span></span>

<span data-ttu-id="77598-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="77598-108">*sesid*</span></span>

<span data-ttu-id="77598-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="77598-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="77598-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="77598-110">*tableid*</span></span>

<span data-ttu-id="77598-111">A tabela na qual os itens são relidos.</span><span class="sxs-lookup"><span data-stu-id="77598-111">The table to issue the prereads against.</span></span>

<span data-ttu-id="77598-112">*rgIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="77598-112">*rgIndexRanges*</span></span>

<span data-ttu-id="77598-113">Os intervalos de chave a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="77598-113">The key ranges to preread.</span></span>

<span data-ttu-id="77598-114">*cIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="77598-114">*cIndexRanges*</span></span>

<span data-ttu-id="77598-115">O número de intervalos de chave a serem lidos, determinados pelo número de elementos em *rgIndexRanges*.</span><span class="sxs-lookup"><span data-stu-id="77598-115">The number of key ranges to preread, determined by the number of elements in *rgIndexRanges*.</span></span>

<span data-ttu-id="77598-116">*pcRangesPreread*</span><span class="sxs-lookup"><span data-stu-id="77598-116">*pcRangesPreread*</span></span>

<span data-ttu-id="77598-117">O número de intervalos de chave que foram realmente lidos.</span><span class="sxs-lookup"><span data-stu-id="77598-117">The number of key ranges that were actually preread.</span></span>

<span data-ttu-id="77598-118">*rgcolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="77598-118">*rgcolumnidPreread*</span></span>

<span data-ttu-id="77598-119">Lista de IDs de coluna para colunas de valor longo a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="77598-119">List of column IDs for long value columns to preread.</span></span> <span data-ttu-id="77598-120">Por padrão, somente o registro na página é de leitura.</span><span class="sxs-lookup"><span data-stu-id="77598-120">By default, only the on-page record is preread.</span></span> <span data-ttu-id="77598-121">Se colunas de valor longo fora da página precisarem ser lidas, suas IDs de coluna precisarão ser passadas por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="77598-121">If Off-page long value columns need to be preread, their column IDs need to be passed via this parameter.</span></span>

<span data-ttu-id="77598-122">*ccolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="77598-122">*ccolumnidPreread*</span></span>

<span data-ttu-id="77598-123">O número de IDs de coluna para colunas de valor longo a serem lidas, determinado pelo número de elementos em *rgcolumnidPreread*.</span><span class="sxs-lookup"><span data-stu-id="77598-123">The number of column IDs for long value columns to preread, determined by the number of elements in *rgcolumnidPreread*.</span></span>

<span data-ttu-id="77598-124">*grbit*</span><span class="sxs-lookup"><span data-stu-id="77598-124">*grbit*</span></span>

<span data-ttu-id="77598-125">Um grupo de bits que especifica zero ou mais valores de direção de preread listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77598-125">A group of bits that specifies zero or more of the preread direction values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77598-126">Valor</span><span class="sxs-lookup"><span data-stu-id="77598-126">Value</span></span></p></th>
<th><p><span data-ttu-id="77598-127">Significado</span><span class="sxs-lookup"><span data-stu-id="77598-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77598-128">Encaminhar</span><span class="sxs-lookup"><span data-stu-id="77598-128">Forward</span></span></p></td>
<td><p><span data-ttu-id="77598-129">Leitura antecipada.</span><span class="sxs-lookup"><span data-stu-id="77598-129">Preread forward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77598-130">Compatibilidade</span><span class="sxs-lookup"><span data-stu-id="77598-130">Backwards</span></span></p></td>
<td><p><span data-ttu-id="77598-131">Leia o retrocesso.</span><span class="sxs-lookup"><span data-stu-id="77598-131">Preread backward.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77598-132">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="77598-132">FirstPageOnly</span></span></p></td>
<td><p><span data-ttu-id="77598-133">Somente Leia a primeira página de qualquer coluna longa.</span><span class="sxs-lookup"><span data-stu-id="77598-133">Preread only the first page of any long column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77598-134">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="77598-134">NormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="77598-135">Chave/indicador normalizado fornecido em vez do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="77598-135">Normalized key/bookmark provided instead of column value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="77598-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77598-136">Return value</span></span>

<span data-ttu-id="77598-137">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77598-137">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="77598-138">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77598-138">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77598-139">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="77598-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="77598-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="77598-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77598-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="77598-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="77598-142">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="77598-142">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="77598-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="77598-143">Remarks</span></span>

<span data-ttu-id="77598-144">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, você deverá iniciar as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="77598-144">If the records with the specified key ranges are not in the buffer cache, you should start asynchronous reads to bring the records into the database buffer cache.</span></span>

#### <a name="requirements"></a><span data-ttu-id="77598-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77598-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77598-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="77598-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77598-147">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77598-147">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77598-148"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="77598-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77598-149">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="77598-149">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77598-150"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="77598-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77598-151">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="77598-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77598-152"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="77598-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="77598-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="77598-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77598-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="77598-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="77598-155">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="77598-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="77598-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="77598-156">See also</span></span>

[<span data-ttu-id="77598-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="77598-157">JET_ERR</span></span>](./jet-err.md)
