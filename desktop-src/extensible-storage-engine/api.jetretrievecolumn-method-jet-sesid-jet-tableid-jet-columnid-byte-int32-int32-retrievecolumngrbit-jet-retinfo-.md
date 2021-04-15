---
description: 'Saiba mais sobre: método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d417e188c72914f871df4b46dede204f6633a8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760928"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="e8b8a-103">Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="e8b8a-104">Recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="e8b8a-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="e8b8a-106">Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="e8b8a-107">Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="e8b8a-108">Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="e8b8a-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8b8a-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b8a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8b8a-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="e8b8a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8b8a-112">Parameters</span></span>

  - <span data-ttu-id="e8b8a-113">sesid</span><span class="sxs-lookup"><span data-stu-id="e8b8a-113">sesid</span></span>  
    <span data-ttu-id="e8b8a-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e8b8a-115">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-116">TableID</span><span class="sxs-lookup"><span data-stu-id="e8b8a-116">tableid</span></span>  
    <span data-ttu-id="e8b8a-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e8b8a-118">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-119">columnid</span><span class="sxs-lookup"><span data-stu-id="e8b8a-119">columnid</span></span>  
    <span data-ttu-id="e8b8a-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e8b8a-121">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-122">data</span><span class="sxs-lookup"><span data-stu-id="e8b8a-122">data</span></span>  
    <span data-ttu-id="e8b8a-123">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="e8b8a-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="e8b8a-124">O buffer de dados a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="e8b8a-125">dataSize</span></span>  
    <span data-ttu-id="e8b8a-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e8b8a-127">O tamanho do buffer de dados.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-128">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="e8b8a-128">actualDataSize</span></span>  
    <span data-ttu-id="e8b8a-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e8b8a-130">Retorna o tamanho real do buffer de dados.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-130">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-131">grbit</span><span class="sxs-lookup"><span data-stu-id="e8b8a-131">grbit</span></span>  
    <span data-ttu-id="e8b8a-132">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-132">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e8b8a-133">Recuperar opções de coluna.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-133">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8b8a-134">retinfo</span><span class="sxs-lookup"><span data-stu-id="e8b8a-134">retinfo</span></span>  
    <span data-ttu-id="e8b8a-135">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-135">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="e8b8a-136">Se pretinfo for atribuído como NULL, a função se comporta como se um itagSequence de 1 e um ibLongValue de 0 (zero) fossem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-136">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="e8b8a-137">Isso faz com que a recuperação de coluna recupere o primeiro valor de uma coluna com vários valores e recupere dados longos no deslocamento 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e8b8a-137">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="e8b8a-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8b8a-138">Return value</span></span>

<span data-ttu-id="e8b8a-139">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8b8a-139">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e8b8a-140">Um código de aviso de ESENT.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-140">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="e8b8a-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8b8a-141">Remarks</span></span>

<span data-ttu-id="e8b8a-142">As funções RetrieveColumnAs fornecem funções de recuperação específicas de DataType.</span><span class="sxs-lookup"><span data-stu-id="e8b8a-142">The RetrieveColumnAs functions provide datatype-specific retrieval functions.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8b8a-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8b8a-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8b8a-144">Referência</span><span class="sxs-lookup"><span data-stu-id="e8b8a-144">Reference</span></span>

[<span data-ttu-id="e8b8a-145">Classe de API</span><span class="sxs-lookup"><span data-stu-id="e8b8a-145">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e8b8a-146">Membros da API</span><span class="sxs-lookup"><span data-stu-id="e8b8a-146">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e8b8a-147">Sobrecarga de JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="e8b8a-147">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="e8b8a-148">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e8b8a-148">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
