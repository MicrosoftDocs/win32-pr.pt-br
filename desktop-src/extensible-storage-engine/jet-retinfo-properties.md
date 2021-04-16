---
description: 'Saiba mais sobre: Propriedades de JET_RETINFO'
title: Propriedades de JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550433"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="486cf-103">Propriedades de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="486cf-103">JET_RETINFO properties</span></span>

<span data-ttu-id="486cf-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="486cf-104">Include protected members</span></span>  
<span data-ttu-id="486cf-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="486cf-105">Include inherited members</span></span>  

<span data-ttu-id="486cf-106">O tipo de [JET_RETINFO](./jet-retinfo-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="486cf-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="486cf-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="486cf-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="486cf-108">Nome</span><span class="sxs-lookup"><span data-stu-id="486cf-108">Name</span></span></th>
<th><span data-ttu-id="486cf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="486cf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="486cf-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="486cf-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="486cf-112">Obtém o columnid da coluna com valor marcado, com vários valores ou esparsos, quando todas as colunas marcadas são recuperadas passando 0 como columnid para JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="486cf-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="486cf-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="486cf-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="486cf-115">Obtém ou define o deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a>ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="486cf-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="486cf-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="486cf-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="486cf-118">Obtém ou define o número de sequência do valor em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="486cf-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="486cf-119">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="486cf-119">The array of values is one-based.</span></span> <span data-ttu-id="486cf-120">O primeiro valor é Sequence 1, e não 0.</span><span class="sxs-lookup"><span data-stu-id="486cf-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="486cf-121">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence.</span><span class="sxs-lookup"><span data-stu-id="486cf-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="486cf-122">Parte superior</span><span class="sxs-lookup"><span data-stu-id="486cf-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="486cf-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="486cf-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="486cf-124">Referência</span><span class="sxs-lookup"><span data-stu-id="486cf-124">Reference</span></span>

[<span data-ttu-id="486cf-125">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="486cf-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="486cf-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="486cf-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
