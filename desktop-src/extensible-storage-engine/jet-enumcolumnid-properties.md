---
description: 'Saiba mais sobre: Propriedades de JET_ENUMCOLUMNID'
title: Propriedades de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501314"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="9d1c5-103">Propriedades de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="9d1c5-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="9d1c5-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="9d1c5-104">Include protected members</span></span>  
<span data-ttu-id="9d1c5-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="9d1c5-105">Include inherited members</span></span>  

<span data-ttu-id="9d1c5-106">O tipo de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="9d1c5-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d1c5-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9d1c5-108">Nome</span><span class="sxs-lookup"><span data-stu-id="9d1c5-108">Name</span></span></th>
<th><span data-ttu-id="9d1c5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d1c5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="9d1c5-111"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="9d1c5-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="9d1c5-112">Obtém ou define a ID de columnid a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="9d1c5-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="9d1c5-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="9d1c5-115">Obtém ou define a contagem de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="9d1c5-116">Se ctagSequence for 0 (zero), rgtagSequence será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="9d1c5-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="9d1c5-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="9d1c5-119">Obtém ou define a matriz de índices com base em um na matriz de valores de coluna para uma determinada coluna.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="9d1c5-120">Um único elemento é um itagSequence que é definido em JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="9d1c5-121">Um itagSequence de 0 (zero) significa &quot; ignorar &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d1c5-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="9d1c5-122">Um itagSequence de 1 significa retornar o primeiro valor de coluna da coluna, 2 significa o segundo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9d1c5-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d1c5-123">Parte superior</span><span class="sxs-lookup"><span data-stu-id="9d1c5-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9d1c5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d1c5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d1c5-125">Referência</span><span class="sxs-lookup"><span data-stu-id="9d1c5-125">Reference</span></span>

[<span data-ttu-id="9d1c5-126">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="9d1c5-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="9d1c5-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9d1c5-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
