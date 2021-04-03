---
description: 'Saiba mais sobre: Propriedades de JET_RECSIZE'
title: Propriedades de JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837352"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="af315-103">Propriedades de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="af315-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="af315-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="af315-104">Include protected members</span></span>  
<span data-ttu-id="af315-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="af315-105">Include inherited members</span></span>  

<span data-ttu-id="af315-106">O tipo de [JET_RECSIZE](./jet-recsize-structure2.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="af315-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="af315-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af315-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="af315-108">Nome</span><span class="sxs-lookup"><span data-stu-id="af315-108">Name</span></span></th>
<th><span data-ttu-id="af315-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="af315-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="af315-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="af315-112">Obtém o conjunto de dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="af315-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="af315-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="af315-115">Obtém o tamanho compactado dos dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="af315-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="af315-116">Isso é o mesmo que <a href="hh557581(v=exchg.10).md">cbData</a> se nenhum valor longo intrínseco for compactado).</span><span class="sxs-lookup"><span data-stu-id="af315-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="af315-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="af315-119">Obtém o conjunto de dados do usuário no registro, mas armazenado na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="af315-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="af315-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="af315-122">Obtém o tamanho compactado dos dados do usuário na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="af315-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="af315-123">Isso é o mesmo que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> se nenhum valor longo separado for compactado.</span><span class="sxs-lookup"><span data-stu-id="af315-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="af315-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="af315-126">Obtém a sobrecarga dos dados de valor longo.</span><span class="sxs-lookup"><span data-stu-id="af315-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="af315-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="af315-129">Obtém a sobrecarga da estrutura de registro ESENT para este registro.</span><span class="sxs-lookup"><span data-stu-id="af315-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="af315-130">Isso inclui o tamanho da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="af315-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="af315-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="af315-133">Obtém o número total de colunas no registro que estão compactadas.</span><span class="sxs-lookup"><span data-stu-id="af315-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="af315-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="af315-136">Obtém o número total de valores longos armazenados na árvore de valor longo para esse registro.</span><span class="sxs-lookup"><span data-stu-id="af315-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="af315-137">Isso não inclui valores longos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="af315-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="af315-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="af315-140">Obtém a acumulação do número total de valores além do primeiro para todas as colunas no registro.</span><span class="sxs-lookup"><span data-stu-id="af315-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="af315-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="af315-143">Obtém o número total de colunas fixas e variáveis definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="af315-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="af315-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="af315-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="af315-146">Obtém o número total de colunas marcadas definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="af315-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="af315-147">Parte superior</span><span class="sxs-lookup"><span data-stu-id="af315-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="af315-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="af315-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af315-149">Referência</span><span class="sxs-lookup"><span data-stu-id="af315-149">Reference</span></span>

[<span data-ttu-id="af315-150">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="af315-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="af315-151">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="af315-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
