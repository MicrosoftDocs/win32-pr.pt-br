---
description: 'Saiba mais sobre: método Columnvalue. GetValueFromBytes'
title: Método columnvalue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 448c0626c0e4cf91b266a6894a021789d52955b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782488"
---
# <a name="columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="f981f-103">Método columnvalue. GetValueFromBytes</span><span class="sxs-lookup"><span data-stu-id="f981f-103">ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="f981f-104">Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue.</span><span class="sxs-lookup"><span data-stu-id="f981f-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="f981f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f981f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f981f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f981f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f981f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f981f-107">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride Sub GetValueFromBytes ( _
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
protected abstract void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="f981f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f981f-108">Parameters</span></span>

  - <span data-ttu-id="f981f-109">value</span><span class="sxs-lookup"><span data-stu-id="f981f-109">value</span></span>  
    <span data-ttu-id="f981f-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="f981f-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="f981f-111">Uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="f981f-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f981f-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="f981f-112">startIndex</span></span>  
    <span data-ttu-id="f981f-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f981f-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f981f-114">A posição inicial dentro dos bytes.</span><span class="sxs-lookup"><span data-stu-id="f981f-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f981f-115">count</span><span class="sxs-lookup"><span data-stu-id="f981f-115">count</span></span>  
    <span data-ttu-id="f981f-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f981f-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f981f-117">O número de bytes a serem decodificados.</span><span class="sxs-lookup"><span data-stu-id="f981f-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="f981f-118">erra</span><span class="sxs-lookup"><span data-stu-id="f981f-118">err</span></span>  
    <span data-ttu-id="f981f-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f981f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f981f-120">O erro retornado de ESENT.</span><span class="sxs-lookup"><span data-stu-id="f981f-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="f981f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f981f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f981f-122">Referência</span><span class="sxs-lookup"><span data-stu-id="f981f-122">Reference</span></span>

[<span data-ttu-id="f981f-123">Classe columnvalue</span><span class="sxs-lookup"><span data-stu-id="f981f-123">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="f981f-124">Membros de columnvalue</span><span class="sxs-lookup"><span data-stu-id="f981f-124">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="f981f-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f981f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
