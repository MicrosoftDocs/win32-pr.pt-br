---
description: 'Saiba mais sobre: método Int32ColumnValue. GetValueFromBytes'
title: Método Int32ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int32ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103331
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c17ee9bc638a0adc2250ac0b3f2e53571ff6fdd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647595"
---
# <a name="int32columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="a2c14-103">Método Int32ColumnValue. GetValueFromBytes</span><span class="sxs-lookup"><span data-stu-id="a2c14-103">Int32ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="a2c14-104">Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue.</span><span class="sxs-lookup"><span data-stu-id="a2c14-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="a2c14-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2c14-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2c14-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a2c14-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2c14-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="a2c14-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2c14-108">Parameters</span></span>

  - <span data-ttu-id="a2c14-109">value</span><span class="sxs-lookup"><span data-stu-id="a2c14-109">value</span></span>  
    <span data-ttu-id="a2c14-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="a2c14-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="a2c14-111">Uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a2c14-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2c14-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="a2c14-112">startIndex</span></span>  
    <span data-ttu-id="a2c14-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a2c14-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a2c14-114">A posição inicial dentro dos bytes.</span><span class="sxs-lookup"><span data-stu-id="a2c14-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2c14-115">count</span><span class="sxs-lookup"><span data-stu-id="a2c14-115">count</span></span>  
    <span data-ttu-id="a2c14-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a2c14-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a2c14-117">O número de bytes a serem decodificados.</span><span class="sxs-lookup"><span data-stu-id="a2c14-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2c14-118">erra</span><span class="sxs-lookup"><span data-stu-id="a2c14-118">err</span></span>  
    <span data-ttu-id="a2c14-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a2c14-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a2c14-120">O erro retornado de ESENT.</span><span class="sxs-lookup"><span data-stu-id="a2c14-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2c14-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2c14-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2c14-122">Referência</span><span class="sxs-lookup"><span data-stu-id="a2c14-122">Reference</span></span>

[<span data-ttu-id="a2c14-123">Classe Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="a2c14-123">Int32ColumnValue class</span></span>](./int32columnvalue-class.md)

[<span data-ttu-id="a2c14-124">Membros do Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="a2c14-124">Int32ColumnValue members</span></span>](./int32columnvalue-members.md)

[<span data-ttu-id="a2c14-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a2c14-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
