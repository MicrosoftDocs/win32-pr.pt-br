---
description: 'Saiba mais sobre: função JetPrereadKeys'
title: Função JetPrereadKeys
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461098"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="b9c0a-103">Função JetPrereadKeys</span><span class="sxs-lookup"><span data-stu-id="b9c0a-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="b9c0a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b9c0a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="b9c0a-105">Função JetPrereadKeys</span><span class="sxs-lookup"><span data-stu-id="b9c0a-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="b9c0a-106">A função **JetPrereadKeys** lê os valores de chave para melhorar o desempenho da limpeza do repositório de versão.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="b9c0a-107">**Windows 7:** a função PrereadKeys é introduzida no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="b9c0a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9c0a-108">Parameters</span></span>

<span data-ttu-id="b9c0a-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-109">*sesid*</span></span>

<span data-ttu-id="b9c0a-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="b9c0a-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-111">*tableid*</span></span>

<span data-ttu-id="b9c0a-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-112">The cursor to use for this call.</span></span>

<span data-ttu-id="b9c0a-113">*rgpvKeys*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-113">*rgpvKeys*</span></span>

<span data-ttu-id="b9c0a-114">Uma matriz de ponteiros para chaves.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-114">An array of pointers to keys.</span></span> <span data-ttu-id="b9c0a-115">As chaves podem ser feitas com [JetMakeKey](./jetmakekey-function.md) ou recuperadas com [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="b9c0a-116">As chaves devem ser classificadas em ordem crescente ou decrescente, dependendo do grbit passado.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="b9c0a-117">As chaves podem ser classificadas com memcmp.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="b9c0a-118">*rgcbKeys*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-118">*rgcbKeys*</span></span>

<span data-ttu-id="b9c0a-119">Uma matriz de comprimentos de chave.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-119">An array of key lengths.</span></span> <span data-ttu-id="b9c0a-120">rgpvKeys \[ n \] deve apontar para uma chave de comprimento rgcbKeys \[ n\]</span><span class="sxs-lookup"><span data-stu-id="b9c0a-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="b9c0a-121">*ckeys*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-121">*ckeys*</span></span>

<span data-ttu-id="b9c0a-122">O número de chaves.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-122">The number of keys.</span></span> <span data-ttu-id="b9c0a-123">rgpvKeys e rgcbKeys devem cada ponto para uma matriz com pelo menos elementos ckeys.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="b9c0a-124">*pckeysPreread*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-124">*pckeysPreread*</span></span>

<span data-ttu-id="b9c0a-125">Retorna o número de chaves para as quais as subleituras foram realmente emitidas.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="b9c0a-126">Este parâmetro pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-126">This parameter can be NULL.</span></span>

<span data-ttu-id="b9c0a-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b9c0a-127">*grbit*</span></span>

<span data-ttu-id="b9c0a-128">Deve ser JET_bitPrereadForward ou JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="b9c0a-129">Se grbit for JET_bitPrereadForward, as chaves deverão ser classificadas em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="b9c0a-130">Se grbit for JET_bitPrereadBackward, as chaves deverão ser classificadas em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="b9c0a-131">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b9c0a-131">Return Value</span></span>

<span data-ttu-id="b9c0a-132">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b9c0a-133">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="b9c0a-134">Vários erros de e/s podem ser retornados junto com esses erros de uso de API:</span><span class="sxs-lookup"><span data-stu-id="b9c0a-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9c0a-135">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b9c0a-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="b9c0a-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9c0a-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9c0a-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="b9c0a-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="b9c0a-138">Grbit não foi JET_bitPrereadForward nem JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9c0a-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="b9c0a-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="b9c0a-140">Um tamanho de chave incorreto foi passado.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="b9c0a-141">As chaves não podem ser 0 nem maiores que o comprimento máximo da chave para a tabela.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9c0a-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b9c0a-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b9c0a-143">Um parâmetro inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="b9c0a-144">Isso pode ser causado por um valor nulo para um parâmetro necessário ou pode indicar que a matriz de chave não está classificada corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9c0a-145">**JetPrereadKeys** percorre as páginas internas da árvore b para determinar quais páginas de folha contêm as chaves especificadas por RgpvKeys/rgcbKeys.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="b9c0a-146">A lista de páginas de folha é classificada e, em seguida, as conleituras são emitidas para os intervalos de páginas.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="b9c0a-147">O número de páginas que podem ser conlidas é limitado, portanto, é possível que nem todas as chaves possam ser conlidas.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="b9c0a-148">Nesse caso, o número de chaves realmente lidas é retornado em pckeysPreread.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b9c0a-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9c0a-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9c0a-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b9c0a-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b9c0a-151">Requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9c0a-152"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b9c0a-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b9c0a-153">Requer o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9c0a-154"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b9c0a-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b9c0a-155">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9c0a-156"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b9c0a-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b9c0a-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9c0a-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b9c0a-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b9c0a-159">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
