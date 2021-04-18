---
description: 'Saiba mais sobre: classe EsentInitInProgressException'
title: Classe EsentInitInProgressException
TOCTitle: EsentInitInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInitInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinitinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b035465e575dd94f68b38cf72f8771c24add49d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752549"
---
# <a name="esentinitinprogressexception-class"></a><span data-ttu-id="10602-103">Classe EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="10602-103">EsentInitInProgressException class</span></span>

<span data-ttu-id="10602-104">Classe base para exceções de JET_err.InitInProgress.</span><span class="sxs-lookup"><span data-stu-id="10602-104">Base class for JET_err.InitInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="10602-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="10602-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="10602-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="10602-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="10602-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="10602-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="10602-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="10602-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="10602-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="10602-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="10602-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="10602-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="10602-111">Microsoft. ISAM. ESENT. Interop. EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="10602-111">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>  

<span data-ttu-id="10602-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10602-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10602-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10602-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10602-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="10602-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInitInProgressException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentInitInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInitInProgressException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="10602-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="10602-115">Thread safety</span></span>

<span data-ttu-id="10602-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="10602-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="10602-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="10602-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="10602-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="10602-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10602-119">Referência</span><span class="sxs-lookup"><span data-stu-id="10602-119">Reference</span></span>

[<span data-ttu-id="10602-120">Membros do EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="10602-120">EsentInitInProgressException members</span></span>](./esentinitinprogressexception-members.md)

[<span data-ttu-id="10602-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="10602-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
