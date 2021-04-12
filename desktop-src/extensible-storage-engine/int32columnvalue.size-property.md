---
description: 'Saiba mais sobre: Propriedade Int32ColumnValue. Size'
title: Propriedade Int32ColumnValue. Size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103332
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10710a8705dfaf63959c1287cae7195841a2f039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296493"
---
# <a name="int32columnvaluesize-property"></a><span data-ttu-id="c9c2b-103">Propriedade Int32ColumnValue. Size</span><span class="sxs-lookup"><span data-stu-id="c9c2b-103">Int32ColumnValue.Size property</span></span>

<span data-ttu-id="c9c2b-104">Obtém o tamanho do valor na coluna.</span><span class="sxs-lookup"><span data-stu-id="c9c2b-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="c9c2b-105">Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String).</span><span class="sxs-lookup"><span data-stu-id="c9c2b-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="c9c2b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9c2b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9c2b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9c2b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c2b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9c2b-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="c9c2b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c9c2b-109">Property value</span></span>

<span data-ttu-id="c9c2b-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c9c2b-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c9c2b-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9c2b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9c2b-112">Referência</span><span class="sxs-lookup"><span data-stu-id="c9c2b-112">Reference</span></span>

[<span data-ttu-id="c9c2b-113">Classe Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="c9c2b-113">Int32ColumnValue class</span></span>](./int32columnvalue-class.md)

[<span data-ttu-id="c9c2b-114">Membros do Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="c9c2b-114">Int32ColumnValue members</span></span>](./int32columnvalue-members.md)

[<span data-ttu-id="c9c2b-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c9c2b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
