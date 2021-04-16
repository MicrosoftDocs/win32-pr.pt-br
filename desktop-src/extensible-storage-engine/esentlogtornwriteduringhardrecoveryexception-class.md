---
description: 'Saiba mais sobre: classe EsentLogTornWriteDuringHardRecoveryException'
title: Classe EsentLogTornWriteDuringHardRecoveryException
TOCTitle: EsentLogTornWriteDuringHardRecoveryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogtornwriteduringhardrecoveryexception(v=EXCHG.10)
ms:contentKeyID: 55102218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96a9f286008cc6d540ebbf6c44fb31b6b0f498d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772930"
---
# <a name="esentlogtornwriteduringhardrecoveryexception-class"></a><span data-ttu-id="bf67c-103">Classe EsentLogTornWriteDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="bf67c-103">EsentLogTornWriteDuringHardRecoveryException class</span></span>

<span data-ttu-id="bf67c-104">Classe base para JET_err. LogTornWriteDuringHardRecovery exceções.</span><span class="sxs-lookup"><span data-stu-id="bf67c-104">Base class for JET_err.LogTornWriteDuringHardRecovery exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bf67c-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="bf67c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bf67c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bf67c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bf67c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bf67c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bf67c-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="bf67c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bf67c-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="bf67c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bf67c-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="bf67c-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="bf67c-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="bf67c-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="bf67c-112">Microsoft. ISAM. ESENT. Interop. EsentLogTornWriteDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="bf67c-112">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>  

<span data-ttu-id="bf67c-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf67c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bf67c-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bf67c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf67c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf67c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogTornWriteDuringHardRecoveryException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogTornWriteDuringHardRecoveryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogTornWriteDuringHardRecoveryException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="bf67c-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="bf67c-116">Thread safety</span></span>

<span data-ttu-id="bf67c-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bf67c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bf67c-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bf67c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf67c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf67c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf67c-120">Referência</span><span class="sxs-lookup"><span data-stu-id="bf67c-120">Reference</span></span>

[<span data-ttu-id="bf67c-121">Membros do EsentLogTornWriteDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="bf67c-121">EsentLogTornWriteDuringHardRecoveryException members</span></span>](./esentlogtornwriteduringhardrecoveryexception-members.md)

[<span data-ttu-id="bf67c-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bf67c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
