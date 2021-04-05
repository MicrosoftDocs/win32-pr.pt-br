---
description: 'Saiba mais sobre: classe EsentFileSystemCorruptionException'
title: Classe EsentFileSystemCorruptionException
TOCTitle: EsentFileSystemCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilesystemcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101716
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 863766b5b4b768546ade161abf8c30659db1d720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662899"
---
# <a name="esentfilesystemcorruptionexception-class"></a><span data-ttu-id="2af75-103">Classe EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2af75-103">EsentFileSystemCorruptionException class</span></span>

<span data-ttu-id="2af75-104">Classe base para JET_err. FileSystemCorruption exceções.</span><span class="sxs-lookup"><span data-stu-id="2af75-104">Base class for JET_err.FileSystemCorruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2af75-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="2af75-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2af75-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2af75-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2af75-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2af75-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2af75-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="2af75-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2af75-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2af75-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2af75-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="2af75-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2af75-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2af75-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="2af75-112">Microsoft. ISAM. ESENT. Interop. EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2af75-112">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>  

<span data-ttu-id="2af75-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2af75-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2af75-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2af75-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2af75-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2af75-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileSystemCorruptionException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentFileSystemCorruptionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileSystemCorruptionException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="2af75-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="2af75-116">Thread safety</span></span>

<span data-ttu-id="2af75-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="2af75-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2af75-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="2af75-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2af75-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2af75-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2af75-120">Referência</span><span class="sxs-lookup"><span data-stu-id="2af75-120">Reference</span></span>

[<span data-ttu-id="2af75-121">Membros do EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2af75-121">EsentFileSystemCorruptionException members</span></span>](./esentfilesystemcorruptionexception-members.md)

[<span data-ttu-id="2af75-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2af75-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
