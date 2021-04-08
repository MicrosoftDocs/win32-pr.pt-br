---
description: 'Saiba mais sobre: método API. JetMakeKey'
title: Método API. JetMakeKey
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922590"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="0f932-103">Método API. JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="0f932-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="0f932-104">Constrói chaves de pesquisa que podem ser usadas por [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="0f932-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="0f932-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f932-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0f932-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f932-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f932-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f932-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0f932-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f932-108">Parameters</span></span>

  - <span data-ttu-id="0f932-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0f932-109">sesid</span></span>  
    <span data-ttu-id="0f932-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0f932-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0f932-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0f932-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f932-112">TableID</span><span class="sxs-lookup"><span data-stu-id="0f932-112">tableid</span></span>  
    <span data-ttu-id="0f932-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0f932-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0f932-114">O cursor no qual criar a chave.</span><span class="sxs-lookup"><span data-stu-id="0f932-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f932-115">data</span><span class="sxs-lookup"><span data-stu-id="0f932-115">data</span></span>  
    <span data-ttu-id="0f932-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="0f932-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="0f932-117">Dados da coluna para a coluna de chave atual do índice atual.</span><span class="sxs-lookup"><span data-stu-id="0f932-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f932-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="0f932-118">dataSize</span></span>  
    <span data-ttu-id="0f932-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0f932-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0f932-120">Tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="0f932-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f932-121">grbit</span><span class="sxs-lookup"><span data-stu-id="0f932-121">grbit</span></span>  
    <span data-ttu-id="0f932-122">Tipo: [Microsoft. ISAM. ESENT. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0f932-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0f932-123">Opções de chave.</span><span class="sxs-lookup"><span data-stu-id="0f932-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f932-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f932-124">Remarks</span></span>

<span data-ttu-id="0f932-125">As funções MakeKey fornecem a funcionalidade de chave Make específica de DataType.</span><span class="sxs-lookup"><span data-stu-id="0f932-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f932-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f932-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f932-127">Referência</span><span class="sxs-lookup"><span data-stu-id="0f932-127">Reference</span></span>

[<span data-ttu-id="0f932-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="0f932-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0f932-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="0f932-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0f932-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0f932-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
