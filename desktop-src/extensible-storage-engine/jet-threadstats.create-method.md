---
description: 'Saiba mais sobre: JET_THREADSTATS. Criar método'
title: JET_THREADSTATS. Método Create (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662819"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="5b053-103">JET_THREADSTATS. Criar método</span><span class="sxs-lookup"><span data-stu-id="5b053-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="5b053-104">Crie um novo struct [JET_THREADSTATS](./jet-threadstats-structure2.md) com o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="5b053-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="5b053-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b053-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="5b053-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5b053-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b053-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b053-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="5b053-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b053-108">Parameters</span></span>

  - <span data-ttu-id="5b053-109">cPageReferenced</span><span class="sxs-lookup"><span data-stu-id="5b053-109">cPageReferenced</span></span>  
    <span data-ttu-id="5b053-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-111">Número de páginas visitadas.</span><span class="sxs-lookup"><span data-stu-id="5b053-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b053-112">cPageRead</span><span class="sxs-lookup"><span data-stu-id="5b053-112">cPageRead</span></span>  
    <span data-ttu-id="5b053-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-114">Número de páginas lidas.</span><span class="sxs-lookup"><span data-stu-id="5b053-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b053-115">cPagePreread</span><span class="sxs-lookup"><span data-stu-id="5b053-115">cPagePreread</span></span>  
    <span data-ttu-id="5b053-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-117">Número de páginas que são relidas.</span><span class="sxs-lookup"><span data-stu-id="5b053-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b053-118">cPageDirtied</span><span class="sxs-lookup"><span data-stu-id="5b053-118">cPageDirtied</span></span>  
    <span data-ttu-id="5b053-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-120">TNumber de páginas sujos.</span><span class="sxs-lookup"><span data-stu-id="5b053-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b053-121">cPageRedirtied</span><span class="sxs-lookup"><span data-stu-id="5b053-121">cPageRedirtied</span></span>  
    <span data-ttu-id="5b053-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-123">Número de páginas redirtied.</span><span class="sxs-lookup"><span data-stu-id="5b053-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b053-124">cLogRecord</span><span class="sxs-lookup"><span data-stu-id="5b053-124">cLogRecord</span></span>  
    <span data-ttu-id="5b053-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-126">Número de registros de log gerados.</span><span class="sxs-lookup"><span data-stu-id="5b053-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b053-127">cbLogRecord</span><span class="sxs-lookup"><span data-stu-id="5b053-127">cbLogRecord</span></span>  
    <span data-ttu-id="5b053-128">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5b053-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5b053-129">Bytes de registros de log gravados.</span><span class="sxs-lookup"><span data-stu-id="5b053-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5b053-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b053-130">Return value</span></span>

<span data-ttu-id="5b053-131">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5b053-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="5b053-132">Um novo struct [JET_THREADSTATS](./jet-threadstats-structure2.md) com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="5b053-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5b053-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b053-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b053-134">Referência</span><span class="sxs-lookup"><span data-stu-id="5b053-134">Reference</span></span>

[<span data-ttu-id="5b053-135">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="5b053-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="5b053-136">Membros do JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="5b053-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="5b053-137">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="5b053-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
