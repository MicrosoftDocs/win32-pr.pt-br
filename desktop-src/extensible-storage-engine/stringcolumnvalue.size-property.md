---
description: 'Saiba mais sobre: Propriedade StringColumnValue. Size'
title: Propriedade StringColumnValue. Size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104025
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.StringColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fdd9613061e049d45c4b9bce2772ff580ea1a0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808216"
---
# <a name="stringcolumnvaluesize-property"></a><span data-ttu-id="114a7-103">Propriedade StringColumnValue. Size</span><span class="sxs-lookup"><span data-stu-id="114a7-103">StringColumnValue.Size property</span></span>

<span data-ttu-id="114a7-104">Obtém o tamanho do valor na coluna.</span><span class="sxs-lookup"><span data-stu-id="114a7-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="114a7-105">Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String).</span><span class="sxs-lookup"><span data-stu-id="114a7-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="114a7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="114a7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="114a7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="114a7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="114a7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="114a7-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="114a7-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="114a7-109">Property value</span></span>

<span data-ttu-id="114a7-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="114a7-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="114a7-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="114a7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="114a7-112">Referência</span><span class="sxs-lookup"><span data-stu-id="114a7-112">Reference</span></span>

[<span data-ttu-id="114a7-113">Classe StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="114a7-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="114a7-114">Membros do StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="114a7-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="114a7-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="114a7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
