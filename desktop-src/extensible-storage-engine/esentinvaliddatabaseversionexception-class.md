---
description: 'Saiba mais sobre: classe EsentInvalidDatabaseVersionException'
title: Classe EsentInvalidDatabaseVersionException
TOCTitle: EsentInvalidDatabaseVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvaliddatabaseversionexception(v=EXCHG.10)
ms:contentKeyID: 55101922
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24b3e348c0c0adaf4d261705c1e4de7bf5d7297b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172271"
---
# <a name="esentinvaliddatabaseversionexception-class"></a><span data-ttu-id="75d7f-103">Classe EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="75d7f-103">EsentInvalidDatabaseVersionException class</span></span>

<span data-ttu-id="75d7f-104">Classe base para JET_err. InvalidDatabaseVersion exceções.</span><span class="sxs-lookup"><span data-stu-id="75d7f-104">Base class for JET_err.InvalidDatabaseVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="75d7f-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="75d7f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="75d7f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="75d7f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="75d7f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="75d7f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="75d7f-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="75d7f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="75d7f-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="75d7f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="75d7f-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="75d7f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="75d7f-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="75d7f-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="75d7f-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="75d7f-112">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>  

<span data-ttu-id="75d7f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75d7f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75d7f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75d7f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75d7f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="75d7f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidDatabaseVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidDatabaseVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidDatabaseVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="75d7f-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="75d7f-116">Thread safety</span></span>

<span data-ttu-id="75d7f-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="75d7f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="75d7f-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="75d7f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="75d7f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="75d7f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75d7f-120">Referência</span><span class="sxs-lookup"><span data-stu-id="75d7f-120">Reference</span></span>

[<span data-ttu-id="75d7f-121">Membros do EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="75d7f-121">EsentInvalidDatabaseVersionException members</span></span>](./esentinvaliddatabaseversionexception-members.md)

[<span data-ttu-id="75d7f-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="75d7f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
