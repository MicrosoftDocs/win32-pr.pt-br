---
description: 'Saiba mais sobre: método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810774"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="68a35-103">Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="68a35-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="68a35-104">Recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="68a35-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="68a35-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="68a35-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="68a35-106">Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor.</span><span class="sxs-lookup"><span data-stu-id="68a35-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="68a35-107">Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="68a35-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="68a35-108">Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</span><span class="sxs-lookup"><span data-stu-id="68a35-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="68a35-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68a35-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68a35-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68a35-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68a35-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68a35-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="68a35-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68a35-112">Parameters</span></span>

  - <span data-ttu-id="68a35-113">sesid</span><span class="sxs-lookup"><span data-stu-id="68a35-113">sesid</span></span>  
    <span data-ttu-id="68a35-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68a35-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="68a35-115">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="68a35-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="68a35-116">TableID</span><span class="sxs-lookup"><span data-stu-id="68a35-116">tableid</span></span>  
    <span data-ttu-id="68a35-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68a35-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="68a35-118">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="68a35-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="68a35-119">columnid</span><span class="sxs-lookup"><span data-stu-id="68a35-119">columnid</span></span>  
    <span data-ttu-id="68a35-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68a35-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="68a35-121">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="68a35-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="68a35-122">grbit</span><span class="sxs-lookup"><span data-stu-id="68a35-122">grbit</span></span>  
    <span data-ttu-id="68a35-123">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="68a35-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="68a35-124">Recuperar opções de coluna.</span><span class="sxs-lookup"><span data-stu-id="68a35-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="68a35-125">retinfo</span><span class="sxs-lookup"><span data-stu-id="68a35-125">retinfo</span></span>  
    <span data-ttu-id="68a35-126">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="68a35-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="68a35-127">Se pretinfo for atribuído como NULL, a função se comporta como se um itagSequence de 1 e um ibLongValue de 0 (zero) fossem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="68a35-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="68a35-128">Isso faz com que a recuperação de coluna recupere o primeiro valor de uma coluna com vários valores e recupere dados longos no deslocamento 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="68a35-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="68a35-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68a35-129">Return value</span></span>

<span data-ttu-id="68a35-130">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="68a35-130">Type: \[\]</span></span>  
<span data-ttu-id="68a35-131">Os dados recuperados da coluna.</span><span class="sxs-lookup"><span data-stu-id="68a35-131">The data retrieved from the column.</span></span> <span data-ttu-id="68a35-132">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="68a35-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68a35-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="68a35-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68a35-134">Referência</span><span class="sxs-lookup"><span data-stu-id="68a35-134">Reference</span></span>

[<span data-ttu-id="68a35-135">Classe de API</span><span class="sxs-lookup"><span data-stu-id="68a35-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="68a35-136">Membros da API</span><span class="sxs-lookup"><span data-stu-id="68a35-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="68a35-137">Sobrecarga de RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="68a35-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="68a35-138">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="68a35-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
