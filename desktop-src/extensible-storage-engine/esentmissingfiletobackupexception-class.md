---
description: 'Saiba mais sobre: classe EsentMissingFileToBackupException'
title: Classe EsentMissingFileToBackupException
TOCTitle: EsentMissingFileToBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfiletobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102216
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5941140df070abb3a273378f3ec275eaf1c6fdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165123"
---
# <a name="esentmissingfiletobackupexception-class"></a><span data-ttu-id="41a2e-103">Classe EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="41a2e-103">EsentMissingFileToBackupException class</span></span>

<span data-ttu-id="41a2e-104">Classe base para JET_err. MissingFileToBackup exceções.</span><span class="sxs-lookup"><span data-stu-id="41a2e-104">Base class for JET_err.MissingFileToBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="41a2e-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="41a2e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="41a2e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="41a2e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="41a2e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="41a2e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="41a2e-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="41a2e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="41a2e-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="41a2e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="41a2e-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="41a2e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="41a2e-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="41a2e-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="41a2e-112">Microsoft. ISAM. ESENT. Interop. EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="41a2e-112">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>  

<span data-ttu-id="41a2e-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="41a2e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="41a2e-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="41a2e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="41a2e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="41a2e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFileToBackupException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingFileToBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFileToBackupException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="41a2e-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="41a2e-116">Thread safety</span></span>

<span data-ttu-id="41a2e-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="41a2e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="41a2e-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="41a2e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="41a2e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="41a2e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41a2e-120">Referência</span><span class="sxs-lookup"><span data-stu-id="41a2e-120">Reference</span></span>

[<span data-ttu-id="41a2e-121">Membros do EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="41a2e-121">EsentMissingFileToBackupException members</span></span>](./esentmissingfiletobackupexception-members.md)

[<span data-ttu-id="41a2e-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="41a2e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
