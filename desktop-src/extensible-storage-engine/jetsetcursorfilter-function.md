---
description: 'Saiba mais sobre: função JetSetCursorFilter'
title: Função JetSetCursorFilter
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090113"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="d8675-103">Função JetSetCursorFilter</span><span class="sxs-lookup"><span data-stu-id="d8675-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="d8675-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d8675-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="d8675-105">A função **JetSetCursorFilter** define uma matriz de filtros simples para a função [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d8675-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="d8675-106">A função **JetSetCursorFilter** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8675-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="d8675-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8675-107">Parameters</span></span>

<span data-ttu-id="d8675-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d8675-108">*sesid*</span></span>

<span data-ttu-id="d8675-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d8675-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="d8675-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d8675-110">*tableid*</span></span>

<span data-ttu-id="d8675-111">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="d8675-111">The cursor to position.</span></span>

<span data-ttu-id="d8675-112">*rgFilters*</span><span class="sxs-lookup"><span data-stu-id="d8675-112">*rgFilters*</span></span>

<span data-ttu-id="d8675-113">Os filtros de registro simples.</span><span class="sxs-lookup"><span data-stu-id="d8675-113">The simple record filters.</span></span>

<span data-ttu-id="d8675-114">*cFilters*</span><span class="sxs-lookup"><span data-stu-id="d8675-114">*cFilters*</span></span>

<span data-ttu-id="d8675-115">O número de filtros.</span><span class="sxs-lookup"><span data-stu-id="d8675-115">The number of filters.</span></span>

<span data-ttu-id="d8675-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d8675-116">*grbit*</span></span>

<span data-ttu-id="d8675-117">Um grupo de bits que especifica zero ou mais das opções de movimentação listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8675-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8675-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d8675-118">Value</span></span></p></th>
<th><p><span data-ttu-id="d8675-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d8675-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8675-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d8675-120">None</span></span></p></td>
<td><p><span data-ttu-id="d8675-121">Opção padrão.</span><span class="sxs-lookup"><span data-stu-id="d8675-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d8675-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8675-122">Return value</span></span>

<span data-ttu-id="d8675-123">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8675-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="d8675-124">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d8675-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8675-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8675-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="d8675-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8675-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8675-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d8675-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d8675-128">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d8675-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="d8675-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8675-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8675-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d8675-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d8675-131">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8675-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8675-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d8675-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d8675-133">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="d8675-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8675-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d8675-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d8675-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d8675-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8675-136"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d8675-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d8675-137">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d8675-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8675-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d8675-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d8675-139">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d8675-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d8675-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8675-140">See also</span></span>

[<span data-ttu-id="d8675-141">JetMove</span><span class="sxs-lookup"><span data-stu-id="d8675-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="d8675-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d8675-142">JET_ERR</span></span>](./jet-err.md)
