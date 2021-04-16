---
description: 'Saiba mais sobre: classe EsentDatabaseFileReadOnlyException'
title: Classe EsentDatabaseFileReadOnlyException
TOCTitle: EsentDatabaseFileReadOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefilereadonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9a086aa4ba07125b437114fcf3b52ca705f1851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461160"
---
# <a name="esentdatabasefilereadonlyexception-class"></a><span data-ttu-id="c3951-103">Classe EsentDatabaseFileReadOnlyException</span><span class="sxs-lookup"><span data-stu-id="c3951-103">EsentDatabaseFileReadOnlyException class</span></span>

<span data-ttu-id="c3951-104">Classe base para JET_err. DatabaseFileReadOnly exceções.</span><span class="sxs-lookup"><span data-stu-id="c3951-104">Base class for JET_err.DatabaseFileReadOnly exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c3951-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="c3951-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c3951-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3951-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c3951-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c3951-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c3951-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="c3951-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c3951-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c3951-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c3951-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="c3951-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="c3951-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="c3951-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="c3951-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseFileReadOnlyException</span><span class="sxs-lookup"><span data-stu-id="c3951-112">Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException</span></span>  

<span data-ttu-id="c3951-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3951-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3951-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3951-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3951-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3951-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFileReadOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseFileReadOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFileReadOnlyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="c3951-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="c3951-116">Thread safety</span></span>

<span data-ttu-id="c3951-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="c3951-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c3951-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="c3951-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3951-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3951-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3951-120">Referência</span><span class="sxs-lookup"><span data-stu-id="c3951-120">Reference</span></span>

[<span data-ttu-id="c3951-121">Membros do EsentDatabaseFileReadOnlyException</span><span class="sxs-lookup"><span data-stu-id="c3951-121">EsentDatabaseFileReadOnlyException members</span></span>](./esentdatabasefilereadonlyexception-members.md)

[<span data-ttu-id="c3951-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c3951-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
