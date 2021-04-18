---
description: 'Saiba mais sobre: método Windows8Api. JetTryPrereadIndexRanges'
title: Método Windows8Api. JetTryPrereadIndexRanges (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813317"
---
# <a name="windows8apijettryprereadindexranges-method"></a><span data-ttu-id="84317-103">Método Windows8Api. JetTryPrereadIndexRanges</span><span class="sxs-lookup"><span data-stu-id="84317-103">Windows8Api.JetTryPrereadIndexRanges method</span></span>

<span data-ttu-id="84317-104">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="84317-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="84317-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="84317-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="84317-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="84317-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="84317-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84317-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="84317-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84317-108">Parameters</span></span>

  - <span data-ttu-id="84317-109">sesid</span><span class="sxs-lookup"><span data-stu-id="84317-109">sesid</span></span>  
    <span data-ttu-id="84317-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84317-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="84317-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="84317-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-112">TableID</span><span class="sxs-lookup"><span data-stu-id="84317-112">tableid</span></span>  
    <span data-ttu-id="84317-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84317-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="84317-114">A tabela na qual os itens são relidos.</span><span class="sxs-lookup"><span data-stu-id="84317-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="84317-115">indexRanges</span></span>  
    <span data-ttu-id="84317-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="84317-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="84317-117">Os intervalos de chave a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="84317-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="84317-118">rangeIndex</span></span>  
    <span data-ttu-id="84317-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="84317-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="84317-120">O índice do primeiro intervalo de chaves na matriz a ser lido.</span><span class="sxs-lookup"><span data-stu-id="84317-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="84317-121">rangeCount</span></span>  
    <span data-ttu-id="84317-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="84317-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="84317-123">O número máximo de intervalos de chave a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="84317-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="84317-124">rangesPreread</span></span>  
    <span data-ttu-id="84317-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="84317-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="84317-126">Retorna o número de chaves que realmente são conlidas.</span><span class="sxs-lookup"><span data-stu-id="84317-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="84317-127">columnsPreread</span></span>  
    <span data-ttu-id="84317-128">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="84317-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="84317-129">Lista de IDs de coluna para colunas de valor longo a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="84317-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="84317-130">grbit</span><span class="sxs-lookup"><span data-stu-id="84317-130">grbit</span></span>  
    <span data-ttu-id="84317-131">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="84317-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="84317-132">Opções de preread.</span><span class="sxs-lookup"><span data-stu-id="84317-132">Preread options.</span></span> <span data-ttu-id="84317-133">Usado para especificar a direção da subleitura.</span><span class="sxs-lookup"><span data-stu-id="84317-133">Used to specify the direction of the preread.</span></span>

#### <a name="return-value"></a><span data-ttu-id="84317-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84317-134">Return value</span></span>

<span data-ttu-id="84317-135">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="84317-135">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="84317-136">**\[ true \]** se alguma preread estiver concluída; caso contrário, **\[ false \]** .</span><span class="sxs-lookup"><span data-stu-id="84317-136">**\[true\]** if some preread done, **\[false\]** otherwise.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84317-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="84317-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="84317-138">Referência</span><span class="sxs-lookup"><span data-stu-id="84317-138">Reference</span></span>

[<span data-ttu-id="84317-139">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="84317-139">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="84317-140">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="84317-140">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="84317-141">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="84317-141">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
