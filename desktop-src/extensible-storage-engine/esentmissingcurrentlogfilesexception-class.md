---
description: 'Saiba mais sobre: classe EsentMissingCurrentLogFilesException'
title: Classe EsentMissingCurrentLogFilesException
TOCTitle: EsentMissingCurrentLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingcurrentlogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c00bec8ba2dee02bf0240bda78f29b3b8f4eafa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770054"
---
# <a name="esentmissingcurrentlogfilesexception-class"></a><span data-ttu-id="ed88a-103">Classe EsentMissingCurrentLogFilesException</span><span class="sxs-lookup"><span data-stu-id="ed88a-103">EsentMissingCurrentLogFilesException class</span></span>

<span data-ttu-id="ed88a-104">Classe base para JET_err. MissingCurrentLogFiles exceções.</span><span class="sxs-lookup"><span data-stu-id="ed88a-104">Base class for JET_err.MissingCurrentLogFiles exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ed88a-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="ed88a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ed88a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ed88a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ed88a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ed88a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ed88a-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="ed88a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ed88a-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ed88a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ed88a-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="ed88a-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ed88a-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="ed88a-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="ed88a-112">Microsoft. ISAM. ESENT. Interop. EsentMissingCurrentLogFilesException</span><span class="sxs-lookup"><span data-stu-id="ed88a-112">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>  

<span data-ttu-id="ed88a-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed88a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed88a-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed88a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed88a-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed88a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingCurrentLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingCurrentLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingCurrentLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="ed88a-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ed88a-116">Thread safety</span></span>

<span data-ttu-id="ed88a-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ed88a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ed88a-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ed88a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed88a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed88a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed88a-120">Referência</span><span class="sxs-lookup"><span data-stu-id="ed88a-120">Reference</span></span>

[<span data-ttu-id="ed88a-121">Membros do EsentMissingCurrentLogFilesException</span><span class="sxs-lookup"><span data-stu-id="ed88a-121">EsentMissingCurrentLogFilesException members</span></span>](./esentmissingcurrentlogfilesexception-members.md)

[<span data-ttu-id="ed88a-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ed88a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
