---
description: 'Saiba mais sobre a propriedade: JET_ENUMCOLUMN. rgEnumColumnValue'
title: Propriedade JET_ENUMCOLUMN. rgEnumColumnValue
TOCTitle: 'rgEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.rgenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103505
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_rgEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d0e131723ae9fb8e1f68193c96d5ed2671a74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501315"
---
# <a name="jet_enumcolumnrgenumcolumnvalue-property"></a><span data-ttu-id="bf502-103">Propriedade JET_ENUMCOLUMN. rgEnumColumnValue</span><span class="sxs-lookup"><span data-stu-id="bf502-103">JET_ENUMCOLUMN.rgEnumColumnValue property</span></span>

<span data-ttu-id="bf502-104">Obtém os valores da coluna enumerada para a coluna.</span><span class="sxs-lookup"><span data-stu-id="bf502-104">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="bf502-105">Esse membro só será usado se [Err](./jet-enumcolumn.err-property.md) não for [ColumnSingleValue](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="bf502-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is not [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="bf502-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf502-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bf502-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bf502-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf502-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf502-108">Syntax</span></span>

``` vb
'Declaration
Public Property rgEnumColumnValue As JET_ENUMCOLUMNVALUE()
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_ENUMCOLUMNVALUE()

value = instance.rgEnumColumnValue
```

``` csharp
public JET_ENUMCOLUMNVALUE[] rgEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="bf502-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bf502-109">Property value</span></span>

<span data-ttu-id="bf502-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="bf502-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf502-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf502-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf502-112">Referência</span><span class="sxs-lookup"><span data-stu-id="bf502-112">Reference</span></span>

[<span data-ttu-id="bf502-113">Classe JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="bf502-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="bf502-114">Membros do JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="bf502-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="bf502-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bf502-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
