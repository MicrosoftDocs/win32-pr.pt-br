---
description: 'Saiba mais sobre: Propriedade BoolColumnValue. Size'
title: Propriedade BoolColumnValue. Size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55100904
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95458e02780b1a0a96c46c857dc168be3125a816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105795478"
---
# <a name="boolcolumnvaluesize-property"></a><span data-ttu-id="b2d27-103">Propriedade BoolColumnValue. Size</span><span class="sxs-lookup"><span data-stu-id="b2d27-103">BoolColumnValue.Size property</span></span>

<span data-ttu-id="b2d27-104">Obtém o tamanho do valor na coluna.</span><span class="sxs-lookup"><span data-stu-id="b2d27-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="b2d27-105">Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String).</span><span class="sxs-lookup"><span data-stu-id="b2d27-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="b2d27-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2d27-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b2d27-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2d27-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d27-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2d27-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="b2d27-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b2d27-109">Property value</span></span>

<span data-ttu-id="b2d27-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2d27-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2d27-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2d27-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2d27-112">Referência</span><span class="sxs-lookup"><span data-stu-id="b2d27-112">Reference</span></span>

[<span data-ttu-id="b2d27-113">Classe BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="b2d27-113">BoolColumnValue class</span></span>](./boolcolumnvalue-class.md)

[<span data-ttu-id="b2d27-114">Membros do BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="b2d27-114">BoolColumnValue members</span></span>](./boolcolumnvalue-members.md)

[<span data-ttu-id="b2d27-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b2d27-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
