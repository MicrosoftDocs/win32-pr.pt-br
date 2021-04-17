---
description: 'Saiba mais sobre: Propriedade BytesColumnValue. Value'
title: Propriedade BytesColumnValue. Value
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55107249
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0804a7a05640336be77e5f446ad99227db592f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813630"
---
# <a name="bytescolumnvaluevalue-property"></a><span data-ttu-id="c8e62-103">Propriedade BytesColumnValue. Value</span><span class="sxs-lookup"><span data-stu-id="c8e62-103">BytesColumnValue.Value property</span></span>

<span data-ttu-id="c8e62-104">Obtém ou define o valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="c8e62-104">Gets or sets the value of the column.</span></span> <span data-ttu-id="c8e62-105">Use [SetColumns (JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) para atualizar um registro com o valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="c8e62-105">Use [SetColumns(JET_SESID, JET_TABLEID, \[\])](./api.setcolumns-method.md) to update a record with the column value.</span></span>

<span data-ttu-id="c8e62-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8e62-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8e62-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8e62-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8e62-108">Syntax</span></span>

``` vb
'Declaration
Public Property Value As Byte()
    Get
    Set
'Usage
Dim instance As BytesColumnValue
Dim value As Byte()

value = instance.Value

instance.Value = value
```

``` csharp
public byte[] Value { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c8e62-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c8e62-109">Property value</span></span>

<span data-ttu-id="c8e62-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="c8e62-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="c8e62-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8e62-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8e62-112">Referência</span><span class="sxs-lookup"><span data-stu-id="c8e62-112">Reference</span></span>

[<span data-ttu-id="c8e62-113">Classe BytesColumnValue</span><span class="sxs-lookup"><span data-stu-id="c8e62-113">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="c8e62-114">Membros do BytesColumnValue</span><span class="sxs-lookup"><span data-stu-id="c8e62-114">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="c8e62-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c8e62-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
