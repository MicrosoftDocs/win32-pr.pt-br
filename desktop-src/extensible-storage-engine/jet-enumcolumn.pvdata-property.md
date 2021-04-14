---
description: 'Saiba mais sobre a propriedade: JET_ENUMCOLUMN. pvData'
title: Propriedade JET_ENUMCOLUMN. pvData
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7d4c72a45d90fd8004af2011f9f6081a59cfabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461102"
---
# <a name="jet_enumcolumnpvdata-property"></a><span data-ttu-id="2ea06-103">Propriedade JET_ENUMCOLUMN. pvData</span><span class="sxs-lookup"><span data-stu-id="2ea06-103">JET_ENUMCOLUMN.pvData property</span></span>

<span data-ttu-id="2ea06-104">Obtém o valor que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="2ea06-104">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="2ea06-105">Esse membro só será usado se [Err](./jet-enumcolumn.err-property.md) for igual a [ColumnSingleValue](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="2ea06-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is equal to [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="2ea06-106">Isso aponta para a memória alocada com o retorno de chamada de alocador de [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) passado para [JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md).</span><span class="sxs-lookup"><span data-stu-id="2ea06-106">This points to memory allocated with the [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) allocator callback passed to [JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md).</span></span> <span data-ttu-id="2ea06-107">Lembre-se de liberar a memória quando terminar.</span><span class="sxs-lookup"><span data-stu-id="2ea06-107">Remember to release the memory when finished.</span></span>

<span data-ttu-id="2ea06-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ea06-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ea06-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2ea06-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea06-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ea06-110">Syntax</span></span>

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="2ea06-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2ea06-111">Property value</span></span>

<span data-ttu-id="2ea06-112">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="2ea06-112">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ea06-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ea06-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ea06-114">Referência</span><span class="sxs-lookup"><span data-stu-id="2ea06-114">Reference</span></span>

[<span data-ttu-id="2ea06-115">Classe JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2ea06-115">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="2ea06-116">Membros do JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2ea06-116">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="2ea06-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2ea06-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
