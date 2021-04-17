---
description: 'Saiba mais sobre: método API. JetSetSessionContext'
title: Método API. JetSetSessionContext
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811488"
---
# <a name="apijetsetsessioncontext-method"></a><span data-ttu-id="547c2-103">Método API. JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="547c2-103">Api.JetSetSessionContext method</span></span>

<span data-ttu-id="547c2-104">Associa uma sessão com o thread atual usando o identificador de contexto fornecido.</span><span class="sxs-lookup"><span data-stu-id="547c2-104">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="547c2-105">Essa associação substitui o requisito de mecanismo padrão que uma transação para uma determinada sessão deve ocorrer inteiramente no mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="547c2-105">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="547c2-106">Use [JetResetSessionContext (JET_SESID)](./api.jetresetsessioncontext-method.md) para remover a associação.</span><span class="sxs-lookup"><span data-stu-id="547c2-106">Use [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) to remove the association.</span></span>

<span data-ttu-id="547c2-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="547c2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="547c2-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="547c2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="547c2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="547c2-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a><span data-ttu-id="547c2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="547c2-110">Parameters</span></span>

  - <span data-ttu-id="547c2-111">sesid</span><span class="sxs-lookup"><span data-stu-id="547c2-111">sesid</span></span>  
    <span data-ttu-id="547c2-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="547c2-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="547c2-113">A sessão na qual definir o contexto.</span><span class="sxs-lookup"><span data-stu-id="547c2-113">The session to set the context on.</span></span>

<!-- end list -->

  - <span data-ttu-id="547c2-114">contexto</span><span class="sxs-lookup"><span data-stu-id="547c2-114">context</span></span>  
    <span data-ttu-id="547c2-115">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="547c2-115">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="547c2-116">O contexto a ser definido.</span><span class="sxs-lookup"><span data-stu-id="547c2-116">The context to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="547c2-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="547c2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="547c2-118">Referência</span><span class="sxs-lookup"><span data-stu-id="547c2-118">Reference</span></span>

[<span data-ttu-id="547c2-119">Classe de API</span><span class="sxs-lookup"><span data-stu-id="547c2-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="547c2-120">Membros da API</span><span class="sxs-lookup"><span data-stu-id="547c2-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="547c2-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="547c2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
