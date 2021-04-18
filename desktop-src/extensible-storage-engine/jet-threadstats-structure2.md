---
description: 'Saiba mais sobre: estrutura de JET_THREADSTATS'
title: Estrutura de JET_THREADSTATS (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761585"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="ed0af-103">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="ed0af-103">JET_THREADSTATS structure</span></span>

<span data-ttu-id="ed0af-104">Contém estatísticas cumulativas no trabalho executado pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="ed0af-104">Contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="ed0af-105">Essas informações são retornadas por meio de JetGetThreadStats.</span><span class="sxs-lookup"><span data-stu-id="ed0af-105">This information is returned via JetGetThreadStats.</span></span>

<span data-ttu-id="ed0af-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed0af-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ed0af-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed0af-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0af-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed0af-108">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a><span data-ttu-id="ed0af-109">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ed0af-109">Thread safety</span></span>

<span data-ttu-id="ed0af-110">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ed0af-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ed0af-111">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ed0af-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed0af-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed0af-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed0af-113">Referência</span><span class="sxs-lookup"><span data-stu-id="ed0af-113">Reference</span></span>

[<span data-ttu-id="ed0af-114">Membros do JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="ed0af-114">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="ed0af-115">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="ed0af-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
