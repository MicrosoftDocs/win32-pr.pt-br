---
description: 'Saiba mais sobre: método API. RetrieveColumn'
title: Método API. RetrieveColumn
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662981"
---
# <a name="apiretrievecolumn-method"></a><span data-ttu-id="7bf21-103">Método API. RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="7bf21-103">Api.RetrieveColumn method</span></span>

<span data-ttu-id="7bf21-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="7bf21-104">Include protected members</span></span>  
<span data-ttu-id="7bf21-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="7bf21-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="7bf21-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="7bf21-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7bf21-107">Name</span><span class="sxs-lookup"><span data-stu-id="7bf21-107">Name</span></span></th>
<th><span data-ttu-id="7bf21-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bf21-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="7bf21-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span><span class="sxs-lookup"><span data-stu-id="7bf21-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="7bf21-112">Recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="7bf21-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="7bf21-113">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="7bf21-113">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="7bf21-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="7bf21-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="7bf21-117">Recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="7bf21-117">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="7bf21-118">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="7bf21-118">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="7bf21-119">Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor.</span><span class="sxs-lookup"><span data-stu-id="7bf21-119">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="7bf21-120">Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="7bf21-120">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="7bf21-121">Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</span><span class="sxs-lookup"><span data-stu-id="7bf21-121">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bf21-122">Parte superior</span><span class="sxs-lookup"><span data-stu-id="7bf21-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="7bf21-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bf21-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7bf21-124">Referência</span><span class="sxs-lookup"><span data-stu-id="7bf21-124">Reference</span></span>

[<span data-ttu-id="7bf21-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7bf21-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7bf21-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7bf21-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7bf21-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7bf21-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
