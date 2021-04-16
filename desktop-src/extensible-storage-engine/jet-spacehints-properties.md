---
description: 'Saiba mais sobre: Propriedades de JET_SPACEHINTS'
title: Propriedades de JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints_properties(v=EXCHG.10)
ms:contentKeyID: 55103923
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f361e0a1fbcf8057ae900e57846cce8457489398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566329"
---
# <a name="jet_spacehints-properties"></a><span data-ttu-id="a74c0-103">Propriedades de JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="a74c0-103">JET_SPACEHINTS properties</span></span>

<span data-ttu-id="a74c0-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="a74c0-104">Include protected members</span></span>  
<span data-ttu-id="a74c0-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="a74c0-105">Include inherited members</span></span>  

<span data-ttu-id="a74c0-106">O tipo de [JET_SPACEHINTS](./jet-spacehints-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a74c0-106">The [JET_SPACEHINTS](./jet-spacehints-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a74c0-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a74c0-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a74c0-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a74c0-108">Name</span></span></th>
<th><span data-ttu-id="a74c0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a74c0-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-111"><a href="dn351103(v=exchg.10).md">cbInitial</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-111"><a href="dn351103(v=exchg.10).md">cbInitial</a></span></span></td>
<td><span data-ttu-id="a74c0-112">Obtém ou define o tamanho inicial (em bytes).</span><span class="sxs-lookup"><span data-stu-id="a74c0-112">Gets or sets the initial size (in bytes).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-114"><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-114"><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></span></span></td>
<td><span data-ttu-id="a74c0-115">Obtém ou define o valor que define o teto de ulGrowth.</span><span class="sxs-lookup"><span data-stu-id="a74c0-115">Gets or sets the value that sets the ceiling of ulGrowth.</span></span> <span data-ttu-id="a74c0-116">Esse valor está em bytes.</span><span class="sxs-lookup"><span data-stu-id="a74c0-116">This value is in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-118"><a href="dn351104(v=exchg.10).md">cbMinExtent</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-118"><a href="dn351104(v=exchg.10).md">cbMinExtent</a></span></span></td>
<td><span data-ttu-id="a74c0-119">Obtém ou define o valor que substitui ulGrowth se for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="a74c0-119">Gets or sets the value that overrides ulGrowth if too small.</span></span> <span data-ttu-id="a74c0-120">Esse valor está em bytes.</span><span class="sxs-lookup"><span data-stu-id="a74c0-120">This value is in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-122"><a href="dn351068(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-122"><a href="dn351068(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="a74c0-123">Obtém ou define as opções de dicas de espaço.</span><span class="sxs-lookup"><span data-stu-id="a74c0-123">Gets or sets the space hints options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-125"><a href="dn351069(v=exchg.10).md">ulGrowth</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-125"><a href="dn351069(v=exchg.10).md">ulGrowth</a></span></span></td>
<td><span data-ttu-id="a74c0-126">Obtém ou define o crescimento percentual do último crescimento ou do tamanho inicial (possivelmente arredondado para o tamanho de alocação mais próximo do JET nativo).</span><span class="sxs-lookup"><span data-stu-id="a74c0-126">Gets or sets the percent growth from last growth or initial size (possibly rounded to nearest native JET allocation size).</span></span> <span data-ttu-id="a74c0-127">Os valores válidos são 0 e [100, 50000).</span><span class="sxs-lookup"><span data-stu-id="a74c0-127">Valid values are 0, and [100, 50000).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-129"><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-129"><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></span></span></td>
<td><span data-ttu-id="a74c0-130">Obtém ou define a densidade no layout (acréscimo).</span><span class="sxs-lookup"><span data-stu-id="a74c0-130">Gets or sets the density at (append) layout.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a74c0-132"><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></span><span class="sxs-lookup"><span data-stu-id="a74c0-132"><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></span></span></td>
<td><span data-ttu-id="a74c0-133">Obtém ou define a densidade na qual manter.</span><span class="sxs-lookup"><span data-stu-id="a74c0-133">Gets or sets the density at which to maintain.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a74c0-134">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a74c0-134">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a74c0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a74c0-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a74c0-136">Referência</span><span class="sxs-lookup"><span data-stu-id="a74c0-136">Reference</span></span>

[<span data-ttu-id="a74c0-137">Classe JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="a74c0-137">JET_SPACEHINTS class</span></span>](./jet-spacehints-class.md)

[<span data-ttu-id="a74c0-138">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a74c0-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
