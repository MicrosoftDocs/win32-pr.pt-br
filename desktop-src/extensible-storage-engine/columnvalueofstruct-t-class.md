---
description: 'Saiba mais sobre: <T> classe ColumnValueOfStruct'
title: Classe ColumnValueOfStruct(T)
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297867"
---
# <a name="columnvalueofstructt-class"></a><span data-ttu-id="39d53-103">\<T\>Classe ColumnValueOfStruct</span><span class="sxs-lookup"><span data-stu-id="39d53-103">ColumnValueOfStruct\<T\> class</span></span>

<span data-ttu-id="39d53-104">Defina uma coluna de um tipo de struct (por exemplo, Int32/GUID).</span><span class="sxs-lookup"><span data-stu-id="39d53-104">Set a column of a struct type (e.g. Int32/Guid).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="39d53-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="39d53-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="39d53-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="39d53-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="39d53-107">Microsoft. ISAM. ESENT. Interop. Columnvalue</span><span class="sxs-lookup"><span data-stu-id="39d53-107">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="39d53-108">Microsoft. ISAM. ESENT. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="39d53-108">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      

<span data-ttu-id="39d53-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39d53-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39d53-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39d53-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39d53-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d53-111">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="39d53-112">Parâmetros de tipo</span><span class="sxs-lookup"><span data-stu-id="39d53-112">Type parameters</span></span>

  - <span data-ttu-id="39d53-113">T</span><span class="sxs-lookup"><span data-stu-id="39d53-113">T</span></span>  
    <span data-ttu-id="39d53-114">Digite para definir.</span><span class="sxs-lookup"><span data-stu-id="39d53-114">Type to set.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="39d53-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="39d53-115">Thread safety</span></span>

<span data-ttu-id="39d53-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="39d53-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="39d53-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="39d53-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="39d53-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="39d53-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39d53-119">Referência</span><span class="sxs-lookup"><span data-stu-id="39d53-119">Reference</span></span>

[<span data-ttu-id="39d53-120">Membros do ColumnValueOfStruct \<T\></span><span class="sxs-lookup"><span data-stu-id="39d53-120">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="39d53-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="39d53-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="39d53-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="39d53-122">Derived types</span></span>

[<span data-ttu-id="39d53-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="39d53-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="39d53-124">Microsoft. ISAM. ESENT. Interop. Columnvalue</span><span class="sxs-lookup"><span data-stu-id="39d53-124">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="39d53-125">Microsoft. ISAM. ESENT. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="39d53-125">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      [<span data-ttu-id="39d53-126">Microsoft. ISAM. ESENT. Interop. BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-126">Microsoft.Isam.Esent.Interop.BoolColumnValue</span></span>](./boolcolumnvalue-class.md)  
      [<span data-ttu-id="39d53-127">Microsoft. ISAM. ESENT. Interop. ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-127">Microsoft.Isam.Esent.Interop.ByteColumnValue</span></span>](./bytecolumnvalue-class.md)  
      [<span data-ttu-id="39d53-128">Microsoft. ISAM. ESENT. Interop. DateTimeColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-128">Microsoft.Isam.Esent.Interop.DateTimeColumnValue</span></span>](./datetimecolumnvalue-class.md)  
      [<span data-ttu-id="39d53-129">Microsoft. ISAM. ESENT. Interop. DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-129">Microsoft.Isam.Esent.Interop.DoubleColumnValue</span></span>](./doublecolumnvalue-class.md)  
      [<span data-ttu-id="39d53-130">Microsoft. ISAM. ESENT. Interop. FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-130">Microsoft.Isam.Esent.Interop.FloatColumnValue</span></span>](./floatcolumnvalue-class.md)  
      [<span data-ttu-id="39d53-131">Microsoft. ISAM. ESENT. Interop. GuidColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-131">Microsoft.Isam.Esent.Interop.GuidColumnValue</span></span>](./guidcolumnvalue-class.md)  
      [<span data-ttu-id="39d53-132">Microsoft. ISAM. ESENT. Interop. Int16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-132">Microsoft.Isam.Esent.Interop.Int16ColumnValue</span></span>](./int16columnvalue-class.md)  
      [<span data-ttu-id="39d53-133">Microsoft. ISAM. ESENT. Interop. Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-133">Microsoft.Isam.Esent.Interop.Int32ColumnValue</span></span>](./int32columnvalue-class.md)  
      [<span data-ttu-id="39d53-134">Microsoft. ISAM. ESENT. Interop. Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-134">Microsoft.Isam.Esent.Interop.Int64ColumnValue</span></span>](./int64columnvalue-class.md)  
      [<span data-ttu-id="39d53-135">Microsoft. ISAM. ESENT. Interop. UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-135">Microsoft.Isam.Esent.Interop.UInt16ColumnValue</span></span>](./uint16columnvalue-class.md)  
      [<span data-ttu-id="39d53-136">Microsoft. ISAM. ESENT. Interop. UInt32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-136">Microsoft.Isam.Esent.Interop.UInt32ColumnValue</span></span>](./uint32columnvalue-class.md)  
      [<span data-ttu-id="39d53-137">Microsoft. ISAM. ESENT. Interop. UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="39d53-137">Microsoft.Isam.Esent.Interop.UInt64ColumnValue</span></span>](./uint64columnvalue-class.md)