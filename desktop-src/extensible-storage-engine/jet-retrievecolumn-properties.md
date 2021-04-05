---
description: 'Saiba mais sobre: Propriedades de JET_RETRIEVECOLUMN'
title: Propriedades de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662824"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="a2319-103">Propriedades de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="a2319-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="a2319-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="a2319-104">Include protected members</span></span>  
<span data-ttu-id="a2319-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="a2319-105">Include inherited members</span></span>  

<span data-ttu-id="a2319-106">O tipo de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a2319-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a2319-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2319-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a2319-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a2319-108">Name</span></span></th>
<th><span data-ttu-id="a2319-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2319-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="a2319-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="a2319-112">Obtém o tamanho, em bytes, dos dados recuperados por uma operação de recuperação de coluna.</span><span class="sxs-lookup"><span data-stu-id="a2319-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="a2319-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="a2319-115">Obtém ou define o tamanho do buffer <a href="dn351040(v=exchg.10).md">pvData</a> , em bytes.</span><span class="sxs-lookup"><span data-stu-id="a2319-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="a2319-116">A operação de recuperação de coluna não armazenará mais dados em pvData do que cbData.</span><span class="sxs-lookup"><span data-stu-id="a2319-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-118"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="a2319-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="a2319-119">Obtém ou define o identificador de coluna da coluna a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="a2319-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="a2319-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="a2319-122">Obtém o columnid da coluna marcada, com vários valores ou esparsos quando todas as colunas marcadas são recuperadas passando 0 como columnid.</span><span class="sxs-lookup"><span data-stu-id="a2319-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-124"><a href="dn335231(v=exchg.10).md">erra</a></span><span class="sxs-lookup"><span data-stu-id="a2319-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="a2319-125">Obtém o aviso retornado da recuperação da coluna.</span><span class="sxs-lookup"><span data-stu-id="a2319-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-127"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="a2319-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="a2319-128">Obtém ou define as opções de recuperação de coluna.</span><span class="sxs-lookup"><span data-stu-id="a2319-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-130"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="a2319-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="a2319-131">Obtém ou define o deslocamento no buffer no qual os dados serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="a2319-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="a2319-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="a2319-134">Obtém ou define o deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="a2319-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="a2319-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="a2319-137">Obtém ou define o número de sequência dos valores contidos em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="a2319-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="a2319-138">Se itagSequence for 0, o número de instâncias de uma coluna com vários valores será retornado em vez de quaisquer dados de coluna.</span><span class="sxs-lookup"><span data-stu-id="a2319-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a2319-140"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="a2319-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="a2319-141">Obtém ou define o buffer que armazenará os dados que serão recuperados da coluna.</span><span class="sxs-lookup"><span data-stu-id="a2319-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a2319-142">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a2319-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a2319-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2319-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2319-144">Referência</span><span class="sxs-lookup"><span data-stu-id="a2319-144">Reference</span></span>

[<span data-ttu-id="a2319-145">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="a2319-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="a2319-146">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a2319-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
