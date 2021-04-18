---
description: 'Saiba mais sobre a propriedade: JET_DBINFOMISC. bkinfoIncPrev'
title: Propriedade JET_DBINFOMISC. bkinfoIncPrev
TOCTitle: 'bkinfoIncPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfoincprev(v=EXCHG.10)
ms:contentKeyID: 39510848
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d323c9af95a59895b30c55cc0a2a5b2664a1c043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781115"
---
# <a name="jet_dbinfomiscbkinfoincprev-property"></a><span data-ttu-id="f6a64-103">Propriedade JET_DBINFOMISC. bkinfoIncPrev</span><span class="sxs-lookup"><span data-stu-id="f6a64-103">JET_DBINFOMISC.bkinfoIncPrev property</span></span>

<span data-ttu-id="f6a64-104">Obtém informações sobre o último backup incremental bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f6a64-104">Gets information about the last successful incremental backup.</span></span> <span data-ttu-id="f6a64-105">Esse valor é redefinido quando [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) é definido.</span><span class="sxs-lookup"><span data-stu-id="f6a64-105">This value is reset when [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) is set.</span></span>

<span data-ttu-id="f6a64-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6a64-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6a64-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6a64-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a64-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6a64-108">Syntax</span></span>

``` vb
'Declaration
Public Property bkinfoIncPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoIncPrev
```

``` csharp
public JET_BKINFO bkinfoIncPrev { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="f6a64-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f6a64-109">Property value</span></span>

<span data-ttu-id="f6a64-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f6a64-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6a64-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6a64-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6a64-112">Referência</span><span class="sxs-lookup"><span data-stu-id="f6a64-112">Reference</span></span>

[<span data-ttu-id="f6a64-113">Classe JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="f6a64-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="f6a64-114">Membros do JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="f6a64-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="f6a64-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f6a64-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
