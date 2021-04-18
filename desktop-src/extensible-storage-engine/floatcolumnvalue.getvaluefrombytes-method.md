---
description: 'Saiba mais sobre: método FloatColumnValue. GetValueFromBytes'
title: Método FloatColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103242
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21fade2ca6c2febc5c28bdad217f450f81c2673f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760607"
---
# <a name="floatcolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="1edd5-103">Método FloatColumnValue. GetValueFromBytes</span><span class="sxs-lookup"><span data-stu-id="1edd5-103">FloatColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="1edd5-104">Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue.</span><span class="sxs-lookup"><span data-stu-id="1edd5-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="1edd5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1edd5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1edd5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1edd5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1edd5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1edd5-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="1edd5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1edd5-108">Parameters</span></span>

  - <span data-ttu-id="1edd5-109">value</span><span class="sxs-lookup"><span data-stu-id="1edd5-109">value</span></span>  
    <span data-ttu-id="1edd5-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="1edd5-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="1edd5-111">Uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="1edd5-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="1edd5-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="1edd5-112">startIndex</span></span>  
    <span data-ttu-id="1edd5-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1edd5-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1edd5-114">A posição inicial dentro dos bytes.</span><span class="sxs-lookup"><span data-stu-id="1edd5-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="1edd5-115">count</span><span class="sxs-lookup"><span data-stu-id="1edd5-115">count</span></span>  
    <span data-ttu-id="1edd5-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1edd5-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1edd5-117">O número de bytes a serem decodificados.</span><span class="sxs-lookup"><span data-stu-id="1edd5-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="1edd5-118">erra</span><span class="sxs-lookup"><span data-stu-id="1edd5-118">err</span></span>  
    <span data-ttu-id="1edd5-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1edd5-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1edd5-120">O erro retornado de ESENT.</span><span class="sxs-lookup"><span data-stu-id="1edd5-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="1edd5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1edd5-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1edd5-122">Referência</span><span class="sxs-lookup"><span data-stu-id="1edd5-122">Reference</span></span>

[<span data-ttu-id="1edd5-123">Classe FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="1edd5-123">FloatColumnValue class</span></span>](./floatcolumnvalue-class.md)

[<span data-ttu-id="1edd5-124">Membros do FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="1edd5-124">FloatColumnValue members</span></span>](./floatcolumnvalue-members.md)

[<span data-ttu-id="1edd5-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1edd5-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
