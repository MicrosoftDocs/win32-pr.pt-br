---
description: 'Saiba mais sobre: Propriedade Columnvalue. Size'
title: Propriedade columnvalue. Size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101207
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 20893eba6516b53045463ce664cdb77ae7e9b768
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010620"
---
# <a name="columnvaluesize-property"></a><span data-ttu-id="97460-103">Propriedade columnvalue. Size</span><span class="sxs-lookup"><span data-stu-id="97460-103">ColumnValue.Size property</span></span>

<span data-ttu-id="97460-104">Obtém o tamanho do valor na coluna.</span><span class="sxs-lookup"><span data-stu-id="97460-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="97460-105">Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String).</span><span class="sxs-lookup"><span data-stu-id="97460-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="97460-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97460-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97460-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97460-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97460-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="97460-108">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected abstract int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="97460-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="97460-109">Property value</span></span>

<span data-ttu-id="97460-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="97460-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="97460-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="97460-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97460-112">Referência</span><span class="sxs-lookup"><span data-stu-id="97460-112">Reference</span></span>

[<span data-ttu-id="97460-113">Classe columnvalue</span><span class="sxs-lookup"><span data-stu-id="97460-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="97460-114">Membros de columnvalue</span><span class="sxs-lookup"><span data-stu-id="97460-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="97460-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="97460-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
