---
description: 'Saiba mais sobre: classe EsentOutOfDatabaseSpaceException'
title: Classe EsentOutOfDatabaseSpaceException
TOCTitle: EsentOutOfDatabaseSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdatabasespaceexception(v=EXCHG.10)
ms:contentKeyID: 55102410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ece3a81fa0687299edba0857b15f4c0abc50e403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755923"
---
# <a name="esentoutofdatabasespaceexception-class"></a><span data-ttu-id="49ab2-103">Classe EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="49ab2-103">EsentOutOfDatabaseSpaceException class</span></span>

<span data-ttu-id="49ab2-104">Classe base para JET_err. OutOfDatabaseSpace exceções.</span><span class="sxs-lookup"><span data-stu-id="49ab2-104">Base class for JET_err.OutOfDatabaseSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="49ab2-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="49ab2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="49ab2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="49ab2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="49ab2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="49ab2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="49ab2-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="49ab2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="49ab2-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="49ab2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="49ab2-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="49ab2-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="49ab2-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="49ab2-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="49ab2-112">Microsoft. ISAM. ESENT. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="49ab2-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="49ab2-113">Microsoft. ISAM. ESENT. Interop. EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="49ab2-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>  

<span data-ttu-id="49ab2-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49ab2-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49ab2-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49ab2-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49ab2-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="49ab2-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDatabaseSpaceException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentOutOfDatabaseSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDatabaseSpaceException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="49ab2-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="49ab2-117">Thread safety</span></span>

<span data-ttu-id="49ab2-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="49ab2-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="49ab2-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="49ab2-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="49ab2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="49ab2-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49ab2-121">Referência</span><span class="sxs-lookup"><span data-stu-id="49ab2-121">Reference</span></span>

[<span data-ttu-id="49ab2-122">Membros do EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="49ab2-122">EsentOutOfDatabaseSpaceException members</span></span>](./esentoutofdatabasespaceexception-members.md)

[<span data-ttu-id="49ab2-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="49ab2-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
