---
description: 'Saiba mais sobre: classe EsentDatabaseUnavailableException'
title: Classe EsentDatabaseUnavailableException
TOCTitle: EsentDatabaseUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101562
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3210a3d5a546d6c27294473137b0306f87f0888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165160"
---
# <a name="esentdatabaseunavailableexception-class"></a><span data-ttu-id="69b17-103">Classe EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="69b17-103">EsentDatabaseUnavailableException class</span></span>

<span data-ttu-id="69b17-104">Classe base para JET_err. DatabaseUnavailable exceções.</span><span class="sxs-lookup"><span data-stu-id="69b17-104">Base class for JET_err.DatabaseUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="69b17-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="69b17-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="69b17-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="69b17-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="69b17-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="69b17-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="69b17-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="69b17-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="69b17-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="69b17-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="69b17-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="69b17-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="69b17-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="69b17-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="69b17-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="69b17-112">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>  

<span data-ttu-id="69b17-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69b17-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69b17-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69b17-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69b17-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="69b17-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseUnavailableException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabaseUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseUnavailableException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="69b17-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="69b17-116">Thread safety</span></span>

<span data-ttu-id="69b17-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="69b17-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="69b17-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="69b17-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="69b17-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="69b17-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69b17-120">Referência</span><span class="sxs-lookup"><span data-stu-id="69b17-120">Reference</span></span>

[<span data-ttu-id="69b17-121">Membros do EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="69b17-121">EsentDatabaseUnavailableException members</span></span>](./esentdatabaseunavailableexception-members.md)

[<span data-ttu-id="69b17-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="69b17-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
