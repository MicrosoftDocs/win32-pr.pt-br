---
description: 'Saiba mais sobre: classe EsentBackupInProgressException'
title: Classe EsentBackupInProgressException
TOCTitle: EsentBackupInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101081
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cae492abaaeac2b4f21b2afd109f8504fdc663f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297485"
---
# <a name="esentbackupinprogressexception-class"></a><span data-ttu-id="43c84-103">Classe EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="43c84-103">EsentBackupInProgressException class</span></span>

<span data-ttu-id="43c84-104">Classe base para JET_err. BackupInProgress exceções.</span><span class="sxs-lookup"><span data-stu-id="43c84-104">Base class for JET_err.BackupInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="43c84-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="43c84-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="43c84-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="43c84-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="43c84-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="43c84-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="43c84-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="43c84-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="43c84-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="43c84-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="43c84-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="43c84-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="43c84-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="43c84-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="43c84-112">Microsoft. ISAM. ESENT. Interop. EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="43c84-112">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>  

<span data-ttu-id="43c84-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43c84-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43c84-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43c84-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43c84-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="43c84-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBackupInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="43c84-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="43c84-116">Thread safety</span></span>

<span data-ttu-id="43c84-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="43c84-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="43c84-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="43c84-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="43c84-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="43c84-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43c84-120">Referência</span><span class="sxs-lookup"><span data-stu-id="43c84-120">Reference</span></span>

[<span data-ttu-id="43c84-121">Membros do EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="43c84-121">EsentBackupInProgressException members</span></span>](./esentbackupinprogressexception-members.md)

[<span data-ttu-id="43c84-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="43c84-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
