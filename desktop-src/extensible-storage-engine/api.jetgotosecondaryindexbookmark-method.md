---
description: 'Saiba mais sobre: método API. JetGotoSecondaryIndexBookmark'
title: Método API. JetGotoSecondaryIndexBookmark
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759787"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="756e7-103">Método API. JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="756e7-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="756e7-104">Posiciona um cursor para uma entrada de índice que está associada ao indicador de índice secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="756e7-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="756e7-105">O indicador de índice secundário deve ser usado com o mesmo índice na mesma tabela da qual ele foi recuperado originalmente.</span><span class="sxs-lookup"><span data-stu-id="756e7-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="756e7-106">O indicador de índice secundário para uma entrada de índice pode ser recuperado usando JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] Int32, GotoSecondaryIndexBookmarkGrbit).</span><span class="sxs-lookup"><span data-stu-id="756e7-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="756e7-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="756e7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="756e7-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="756e7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="756e7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="756e7-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="756e7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="756e7-110">Parameters</span></span>

  - <span data-ttu-id="756e7-111">sesid</span><span class="sxs-lookup"><span data-stu-id="756e7-111">sesid</span></span>  
    <span data-ttu-id="756e7-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="756e7-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="756e7-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="756e7-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="756e7-114">TableID</span><span class="sxs-lookup"><span data-stu-id="756e7-114">tableid</span></span>  
    <span data-ttu-id="756e7-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="756e7-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="756e7-116">O cursor de tabela a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="756e7-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="756e7-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="756e7-117">secondaryKey</span></span>  
    <span data-ttu-id="756e7-118">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="756e7-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="756e7-119">O buffer que contém a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="756e7-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="756e7-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="756e7-120">secondaryKeySize</span></span>  
    <span data-ttu-id="756e7-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="756e7-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="756e7-122">O tamanho da chave secundária.</span><span class="sxs-lookup"><span data-stu-id="756e7-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="756e7-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="756e7-123">primaryKey</span></span>  
    <span data-ttu-id="756e7-124">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="756e7-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="756e7-125">O buffer que contém a chave primária.</span><span class="sxs-lookup"><span data-stu-id="756e7-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="756e7-126">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="756e7-126">primaryKeySize</span></span>  
    <span data-ttu-id="756e7-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="756e7-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="756e7-128">O tamanho da chave primária.</span><span class="sxs-lookup"><span data-stu-id="756e7-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="756e7-129">grbit</span><span class="sxs-lookup"><span data-stu-id="756e7-129">grbit</span></span>  
    <span data-ttu-id="756e7-130">Tipo: [Microsoft. ISAM. ESENT. Interop. GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="756e7-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="756e7-131">Opções para posicionamento do indicador.</span><span class="sxs-lookup"><span data-stu-id="756e7-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="756e7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="756e7-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="756e7-133">Referência</span><span class="sxs-lookup"><span data-stu-id="756e7-133">Reference</span></span>

[<span data-ttu-id="756e7-134">Classe de API</span><span class="sxs-lookup"><span data-stu-id="756e7-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="756e7-135">Membros da API</span><span class="sxs-lookup"><span data-stu-id="756e7-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="756e7-136">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="756e7-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
