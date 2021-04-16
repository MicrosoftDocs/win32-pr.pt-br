---
description: 'Saiba mais sobre: conversão implícita de tabela (tabela para JET_TABLEID)'
title: Conversão implícita de tabela (tabela para JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772755"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a><span data-ttu-id="8f308-103">Conversão implícita de tabela (tabela para JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="8f308-103">Table Implicit conversion (Table to JET_TABLEID)</span></span>

<span data-ttu-id="8f308-104">Operador de conversão implícita de uma tabela para um JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="8f308-104">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="8f308-105">Isso permite que uma tabela seja usada com APIs que esperam um JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="8f308-105">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span>

<span data-ttu-id="8f308-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f308-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8f308-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f308-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f308-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f308-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a><span data-ttu-id="8f308-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f308-109">Parameters</span></span>

  - <span data-ttu-id="8f308-110">table</span><span class="sxs-lookup"><span data-stu-id="8f308-110">table</span></span>  
    <span data-ttu-id="8f308-111">Tipo: [Microsoft. ISAM. ESENT. Interop. Table](./table-class.md)</span><span class="sxs-lookup"><span data-stu-id="8f308-111">Type: [Microsoft.Isam.Esent.Interop.Table](./table-class.md)</span></span>  
    
    <span data-ttu-id="8f308-112">A tabela a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="8f308-112">The table to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8f308-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f308-113">Return value</span></span>

<span data-ttu-id="8f308-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8f308-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
<span data-ttu-id="8f308-115">O JET_TABLEID da tabela.</span><span class="sxs-lookup"><span data-stu-id="8f308-115">The JET_TABLEID of the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f308-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f308-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f308-117">Referência</span><span class="sxs-lookup"><span data-stu-id="8f308-117">Reference</span></span>

[<span data-ttu-id="8f308-118">Classe de tabela</span><span class="sxs-lookup"><span data-stu-id="8f308-118">Table class</span></span>](./table-class.md)

[<span data-ttu-id="8f308-119">Membros da tabela</span><span class="sxs-lookup"><span data-stu-id="8f308-119">Table members</span></span>](./table-members.md)

[<span data-ttu-id="8f308-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8f308-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
