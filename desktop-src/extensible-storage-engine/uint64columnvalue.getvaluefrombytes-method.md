---
description: 'Saiba mais sobre: método UInt64ColumnValue. GetValueFromBytes'
title: Método UInt64ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ccf4a0d85c6d712a81222f77b954d46f55a28df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785300"
---
# <a name="uint64columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="5d5d2-103">Método UInt64ColumnValue. GetValueFromBytes</span><span class="sxs-lookup"><span data-stu-id="5d5d2-103">UInt64ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="5d5d2-104">Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="5d5d2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d5d2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d5d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d5d2-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="5d5d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d5d2-108">Parameters</span></span>

  - <span data-ttu-id="5d5d2-109">value</span><span class="sxs-lookup"><span data-stu-id="5d5d2-109">value</span></span>  
    <span data-ttu-id="5d5d2-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="5d5d2-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="5d5d2-111">Uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d5d2-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="5d5d2-112">startIndex</span></span>  
    <span data-ttu-id="5d5d2-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5d5d2-114">A posição inicial dentro dos bytes.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d5d2-115">count</span><span class="sxs-lookup"><span data-stu-id="5d5d2-115">count</span></span>  
    <span data-ttu-id="5d5d2-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5d5d2-117">O número de bytes a serem decodificados.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d5d2-118">erra</span><span class="sxs-lookup"><span data-stu-id="5d5d2-118">err</span></span>  
    <span data-ttu-id="5d5d2-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5d5d2-120">O erro retornado de ESENT.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d5d2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d5d2-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d5d2-122">Referência</span><span class="sxs-lookup"><span data-stu-id="5d5d2-122">Reference</span></span>

[<span data-ttu-id="5d5d2-123">Classe UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="5d5d2-123">UInt64ColumnValue class</span></span>](./uint64columnvalue-class.md)

[<span data-ttu-id="5d5d2-124">Membros do UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="5d5d2-124">UInt64ColumnValue members</span></span>](./uint64columnvalue-members.md)

[<span data-ttu-id="5d5d2-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5d5d2-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
