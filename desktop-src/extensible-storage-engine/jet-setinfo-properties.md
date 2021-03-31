---
description: 'Saiba mais sobre: Propriedades de JET_SETINFO'
title: Propriedades de JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090120"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="a93d9-103">Propriedades de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="a93d9-103">JET_SETINFO properties</span></span>

<span data-ttu-id="a93d9-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="a93d9-104">Include protected members</span></span>  
<span data-ttu-id="a93d9-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="a93d9-105">Include inherited members</span></span>  

<span data-ttu-id="a93d9-106">O tipo de [JET_SETINFO](./jet-setinfo-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a93d9-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a93d9-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a93d9-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a93d9-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a93d9-108">Name</span></span></th>
<th><span data-ttu-id="a93d9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a93d9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a93d9-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="a93d9-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="a93d9-112">Obtém ou define o deslocamento para o primeiro byte a ser definido em uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="a93d9-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a93d9-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="a93d9-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="a93d9-115">Obtém ou define o número de sequência do valor em uma coluna de valores múltiplos a ser definida.</span><span class="sxs-lookup"><span data-stu-id="a93d9-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="a93d9-116">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="a93d9-116">The array of values is one-based.</span></span> <span data-ttu-id="a93d9-117">O primeiro valor é Sequence 1, não 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a93d9-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="a93d9-118">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence se esse valor estiver sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="a93d9-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="a93d9-119">Um valor de 0 (zero) significa adicionar uma nova instância de valor de coluna ao final da sequência de valores de coluna.</span><span class="sxs-lookup"><span data-stu-id="a93d9-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a93d9-120">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a93d9-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a93d9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a93d9-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a93d9-122">Referência</span><span class="sxs-lookup"><span data-stu-id="a93d9-122">Reference</span></span>

[<span data-ttu-id="a93d9-123">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="a93d9-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="a93d9-124">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a93d9-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
