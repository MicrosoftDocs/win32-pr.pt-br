---
description: 'Saiba mais sobre: estrutura de JET_UNICODEINDEX'
title: Estrutura de JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104371030"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="4bf0f-103">Estrutura de JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="4bf0f-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="4bf0f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4bf0f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="4bf0f-105">Estrutura de JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="4bf0f-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="4bf0f-106">A estrutura de **JET_UNICODEINDEX** personaliza como os dados Unicode são normalizados quando um índice é criado em uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="4bf0f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4bf0f-107">Members</span></span>

<span data-ttu-id="4bf0f-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="4bf0f-108">**lcid**</span></span>

<span data-ttu-id="4bf0f-109">A ID de localidade a ser usada ao normalizar os dados.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="4bf0f-110">Qualquer localidade pode ser usada, desde que o pacote de idiomas apropriado tenha sido instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="4bf0f-111">A única exceção é que a localidade neutra do idioma (LCID de zero) é inválida.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="4bf0f-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="4bf0f-112">**dwMapFlags**</span></span>

<span data-ttu-id="4bf0f-113">Esses sinalizadores são passados para [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) quando os dados Unicode são normalizados para uma chave, o que permite que os sinalizadores definidos pelo usuário substituam o padrão.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="4bf0f-114">**Windows 2000**: os únicos dois valores válidos para **dwFlags** são:</span><span class="sxs-lookup"><span data-stu-id="4bf0f-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="4bf0f-115">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)</span><span class="sxs-lookup"><span data-stu-id="4bf0f-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="4bf0f-116">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)</span><span class="sxs-lookup"><span data-stu-id="4bf0f-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="4bf0f-117">**dwMapFlags** tem as seguintes restrições.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bf0f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4bf0f-118">Value</span></span></p></th>
<th><p><span data-ttu-id="4bf0f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="4bf0f-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bf0f-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="4bf0f-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-121">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf0f-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="4bf0f-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf0f-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="4bf0f-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf0f-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="4bf0f-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf0f-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="4bf0f-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf0f-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="4bf0f-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf0f-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="4bf0f-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf0f-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="4bf0f-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="4bf0f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="4bf0f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bf0f-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bf0f-137"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4bf0f-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf0f-138">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf0f-139"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4bf0f-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf0f-140">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf0f-141"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4bf0f-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf0f-142">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4bf0f-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4bf0f-143">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4bf0f-143">See Also</span></span>

[<span data-ttu-id="4bf0f-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="4bf0f-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="4bf0f-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="4bf0f-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="4bf0f-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="4bf0f-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
