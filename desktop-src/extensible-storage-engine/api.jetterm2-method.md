---
description: 'Saiba mais sobre: método API. JetTerm2'
title: Método API. JetTerm2
TOCTitle: 'JetTerm2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm2(v=EXCHG.10)
ms:contentKeyID: 55100829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e8a4aa8c96f9a4d0242657fe7126abf1388a7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789924"
---
# <a name="apijetterm2-method"></a><span data-ttu-id="33ce1-103">Método API. JetTerm2</span><span class="sxs-lookup"><span data-stu-id="33ce1-103">Api.JetTerm2 method</span></span>

<span data-ttu-id="33ce1-104">Finalize uma instância que foi criada com [JetInit (JET_INSTANCE)](./api.jetinit-method.md) ou [JetCreateInstance (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="33ce1-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="33ce1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33ce1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33ce1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33ce1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33ce1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33ce1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm2 ( _
    instance As JET_INSTANCE, _
    grbit As TermGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As TermGrbitApi.JetTerm2(instance, grbit)
```

``` csharp
public static void JetTerm2(
    JET_INSTANCE instance,
    TermGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="33ce1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33ce1-108">Parameters</span></span>

  - <span data-ttu-id="33ce1-109">instance</span><span class="sxs-lookup"><span data-stu-id="33ce1-109">instance</span></span>  
    <span data-ttu-id="33ce1-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="33ce1-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="33ce1-111">A instância a ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="33ce1-111">The instance to terminate.</span></span>

<!-- end list -->

  - <span data-ttu-id="33ce1-112">grbit</span><span class="sxs-lookup"><span data-stu-id="33ce1-112">grbit</span></span>  
    <span data-ttu-id="33ce1-113">Tipo: [Microsoft. ISAM. ESENT. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="33ce1-113">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="33ce1-114">Opções de encerramento.</span><span class="sxs-lookup"><span data-stu-id="33ce1-114">Termination options.</span></span>

## <a name="see-also"></a><span data-ttu-id="33ce1-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="33ce1-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33ce1-116">Referência</span><span class="sxs-lookup"><span data-stu-id="33ce1-116">Reference</span></span>

[<span data-ttu-id="33ce1-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="33ce1-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="33ce1-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="33ce1-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="33ce1-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="33ce1-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
