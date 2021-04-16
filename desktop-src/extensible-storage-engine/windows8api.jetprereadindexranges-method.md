---
description: 'Saiba mais sobre: método Windows8Api. JetPrereadIndexRanges'
title: Método Windows8Api. JetPrereadIndexRanges (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 986213a054dec54e92e4ecfe6fb0abd541b451ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782389"
---
# <a name="windows8apijetprereadindexranges-method"></a><span data-ttu-id="a6325-103">Método Windows8Api. JetPrereadIndexRanges</span><span class="sxs-lookup"><span data-stu-id="a6325-103">Windows8Api.JetPrereadIndexRanges method</span></span>

<span data-ttu-id="a6325-104">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6325-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="a6325-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6325-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="a6325-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6325-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6325-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6325-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.JetPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static void JetPrereadIndexRanges(
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

#### <a name="parameters"></a><span data-ttu-id="a6325-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6325-108">Parameters</span></span>

  - <span data-ttu-id="a6325-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a6325-109">sesid</span></span>  
    <span data-ttu-id="a6325-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6325-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a6325-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a6325-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a6325-112">tableid</span></span>  
    <span data-ttu-id="a6325-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6325-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a6325-114">A tabela na qual os itens são relidos.</span><span class="sxs-lookup"><span data-stu-id="a6325-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="a6325-115">indexRanges</span></span>  
    <span data-ttu-id="a6325-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="a6325-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="a6325-117">Os intervalos de chave a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="a6325-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="a6325-118">rangeIndex</span></span>  
    <span data-ttu-id="a6325-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a6325-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a6325-120">O índice do primeiro intervalo de chaves na matriz a ser lido.</span><span class="sxs-lookup"><span data-stu-id="a6325-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="a6325-121">rangeCount</span></span>  
    <span data-ttu-id="a6325-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a6325-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a6325-123">O número máximo de intervalos de chave a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="a6325-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="a6325-124">rangesPreread</span></span>  
    <span data-ttu-id="a6325-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a6325-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a6325-126">Retorna o número de chaves que realmente são conlidas.</span><span class="sxs-lookup"><span data-stu-id="a6325-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="a6325-127">columnsPreread</span></span>  
    <span data-ttu-id="a6325-128">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="a6325-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="a6325-129">Lista de IDs de coluna para colunas de valor longo a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="a6325-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6325-130">grbit</span><span class="sxs-lookup"><span data-stu-id="a6325-130">grbit</span></span>  
    <span data-ttu-id="a6325-131">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a6325-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a6325-132">Opções de preread.</span><span class="sxs-lookup"><span data-stu-id="a6325-132">Preread options.</span></span> <span data-ttu-id="a6325-133">Usado para especificar a direção da subleitura.</span><span class="sxs-lookup"><span data-stu-id="a6325-133">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6325-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6325-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6325-135">Referência</span><span class="sxs-lookup"><span data-stu-id="a6325-135">Reference</span></span>

[<span data-ttu-id="a6325-136">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="a6325-136">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="a6325-137">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="a6325-137">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="a6325-138">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="a6325-138">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
