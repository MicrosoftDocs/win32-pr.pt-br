---
description: 'Saiba mais sobre: método API. JetGetSecondaryIndexBookmark'
title: Método API. JetGetSecondaryIndexBookmark
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010416"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="ca7c7-103">Método API. JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="ca7c7-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="ca7c7-104">Recupera um indicador especial para a entrada de índice secundário na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="ca7c7-105">Esse indicador pode então ser usado para reposicionar com eficiência esse cursor de volta para a mesma entrada de índice usando JetGotoSecondaryIndexBookmark.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="ca7c7-106">Isso é mais útil ao reposicionar em um índice secundário que contém chaves duplicadas ou que contém várias entradas de índice para o mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="ca7c7-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ca7c7-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7c7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca7c7-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ca7c7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca7c7-110">Parameters</span></span>

  - <span data-ttu-id="ca7c7-111">sesid</span><span class="sxs-lookup"><span data-stu-id="ca7c7-111">sesid</span></span>  
    <span data-ttu-id="ca7c7-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ca7c7-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-114">TableID</span><span class="sxs-lookup"><span data-stu-id="ca7c7-114">tableid</span></span>  
    <span data-ttu-id="ca7c7-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ca7c7-116">O cursor do qual recuperar o indicador.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="ca7c7-117">secondaryKey</span></span>  
    <span data-ttu-id="ca7c7-118">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="ca7c7-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="ca7c7-119">Buffer de saída para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="ca7c7-120">secondaryKeySize</span></span>  
    <span data-ttu-id="ca7c7-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ca7c7-122">Tamanho do buffer de chave secundária.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-123">actualSecondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="ca7c7-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="ca7c7-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ca7c7-125">Retorna o tamanho da chave secundária.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="ca7c7-126">primaryKey</span></span>  
    <span data-ttu-id="ca7c7-127">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="ca7c7-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="ca7c7-128">Buffer de saída para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-129">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="ca7c7-129">primaryKeySize</span></span>  
    <span data-ttu-id="ca7c7-130">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ca7c7-131">Tamanho do buffer de chave primária.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-132">actualPrimaryKeySize</span><span class="sxs-lookup"><span data-stu-id="ca7c7-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="ca7c7-133">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ca7c7-134">Retorna o tamanho da chave primária.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="ca7c7-135">grbit</span><span class="sxs-lookup"><span data-stu-id="ca7c7-135">grbit</span></span>  
    <span data-ttu-id="ca7c7-136">Tipo: [Microsoft. ISAM. ESENT. Interop. GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ca7c7-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ca7c7-137">Opções para a chamada.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca7c7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca7c7-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ca7c7-139">Referência</span><span class="sxs-lookup"><span data-stu-id="ca7c7-139">Reference</span></span>

[<span data-ttu-id="ca7c7-140">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ca7c7-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ca7c7-141">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ca7c7-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ca7c7-142">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ca7c7-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
