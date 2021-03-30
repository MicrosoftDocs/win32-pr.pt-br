---
description: 'Saiba mais sobre: classe de instância'
title: Classe de instância
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647603"
---
# <a name="instance-class"></a><span data-ttu-id="edf57-103">Classe de instância</span><span class="sxs-lookup"><span data-stu-id="edf57-103">Instance class</span></span>

<span data-ttu-id="edf57-104">Uma classe que encapsula um [JET_INSTANCE](./jet-instance-structure.md) em um objeto descartável.</span><span class="sxs-lookup"><span data-stu-id="edf57-104">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="edf57-105">A instância deve ser fechada por último e o fechamento da instância libera todos os outros recursos da instância.</span><span class="sxs-lookup"><span data-stu-id="edf57-105">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="edf57-106">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="edf57-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="edf57-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="edf57-107">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="edf57-108">System. Runtime. ConstrainedExecution. CriticalFinalizerObject</span><span class="sxs-lookup"><span data-stu-id="edf57-108">System.Runtime.ConstrainedExecution.CriticalFinalizerObject</span></span>](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [<span data-ttu-id="edf57-109">System.Runtime.InteropServices.SafeHandle</span><span class="sxs-lookup"><span data-stu-id="edf57-109">System.Runtime.InteropServices.SafeHandle</span></span>](/dotnet/api/system.runtime.interopservices.safehandle)  
      [<span data-ttu-id="edf57-110">Microsoft. Win32. SafeHandles. SafeHandleZeroOrMinusOneIsInvalid</span><span class="sxs-lookup"><span data-stu-id="edf57-110">Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span></span>](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        <span data-ttu-id="edf57-111">Microsoft. ISAM. ESENT. Interop. Instance</span><span class="sxs-lookup"><span data-stu-id="edf57-111">Microsoft.Isam.Esent.Interop.Instance</span></span>  

<span data-ttu-id="edf57-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="edf57-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="edf57-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="edf57-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="edf57-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edf57-114">Syntax</span></span>

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a><span data-ttu-id="edf57-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="edf57-115">Thread safety</span></span>

<span data-ttu-id="edf57-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="edf57-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="edf57-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="edf57-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="edf57-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="edf57-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="edf57-119">Referência</span><span class="sxs-lookup"><span data-stu-id="edf57-119">Reference</span></span>

[<span data-ttu-id="edf57-120">Membros da Instância </span><span class="sxs-lookup"><span data-stu-id="edf57-120">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="edf57-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="edf57-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
