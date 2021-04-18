---
description: 'Saiba mais sobre: Propriedade Columnvalue. Length'
title: Propriedade columnvalue. Length
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786262"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="58e90-103">Propriedade columnvalue. Length</span><span class="sxs-lookup"><span data-stu-id="58e90-103">ColumnValue.Length property</span></span>

<span data-ttu-id="58e90-104">Obtém o comprimento de byte de um valor de coluna, que será zero se a coluna for nula, caso contrário, ela corresponderá ao tamanho de colunas de tamanho fixo e representará o comprimento de byte de valor real para colunas de tamanho variável (ou seja, binary e String).</span><span class="sxs-lookup"><span data-stu-id="58e90-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="58e90-105">Para cadeias de caracteres, o comprimento é determinado na suposição de dois bytes por caractere.</span><span class="sxs-lookup"><span data-stu-id="58e90-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="58e90-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="58e90-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="58e90-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="58e90-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="58e90-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e90-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="58e90-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="58e90-109">Property value</span></span>

<span data-ttu-id="58e90-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="58e90-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="58e90-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="58e90-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="58e90-112">Referência</span><span class="sxs-lookup"><span data-stu-id="58e90-112">Reference</span></span>

[<span data-ttu-id="58e90-113">Classe columnvalue</span><span class="sxs-lookup"><span data-stu-id="58e90-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="58e90-114">Membros de columnvalue</span><span class="sxs-lookup"><span data-stu-id="58e90-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="58e90-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="58e90-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
