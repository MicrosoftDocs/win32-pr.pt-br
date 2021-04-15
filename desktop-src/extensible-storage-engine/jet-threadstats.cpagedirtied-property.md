---
description: 'Saiba mais sobre a propriedade: JET_THREADSTATS. cPageDirtied'
title: Propriedade JET_THREADSTATS. cPageDirtied (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'cPageDirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagedirtied(v=EXCHG.10)
ms:contentKeyID: 39512428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageDirtied
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d1f628ce821a6e35c231ccf4b469b5b1c1ff60c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501303"
---
# <a name="jet_threadstatscpagedirtied-property"></a><span data-ttu-id="bb627-103">Propriedade JET_THREADSTATS. cPageDirtied</span><span class="sxs-lookup"><span data-stu-id="bb627-103">JET_THREADSTATS.cPageDirtied property</span></span>

<span data-ttu-id="bb627-104">Obtém o número total de páginas de banco de dados, sem alterações não gravadas, que foram modificadas pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="bb627-104">Gets the total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="bb627-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bb627-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="bb627-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bb627-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bb627-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb627-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageDirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageDirtied
```

``` csharp
public int cPageDirtied { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="bb627-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bb627-108">Property value</span></span>

<span data-ttu-id="bb627-109">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bb627-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb627-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb627-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb627-111">Referência</span><span class="sxs-lookup"><span data-stu-id="bb627-111">Reference</span></span>

[<span data-ttu-id="bb627-112">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="bb627-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="bb627-113">Membros do JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="bb627-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="bb627-114">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="bb627-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
