---
description: 'Saiba mais sobre: classe EsentReadPgnoVerifyFailureException'
title: Classe EsentReadPgnoVerifyFailureException
TOCTitle: EsentReadPgnoVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadpgnoverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102553
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0de6967016196e48fe15bf6f190d1a4207678bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798409"
---
# <a name="esentreadpgnoverifyfailureexception-class"></a><span data-ttu-id="53704-103">Classe EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="53704-103">EsentReadPgnoVerifyFailureException class</span></span>

<span data-ttu-id="53704-104">Classe base para JET_err. ReadPgnoVerifyFailure exceções.</span><span class="sxs-lookup"><span data-stu-id="53704-104">Base class for JET_err.ReadPgnoVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="53704-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="53704-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="53704-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="53704-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="53704-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="53704-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="53704-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="53704-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="53704-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="53704-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="53704-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="53704-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="53704-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="53704-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="53704-112">Microsoft. ISAM. ESENT. Interop. EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="53704-112">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>  

<span data-ttu-id="53704-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53704-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53704-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53704-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53704-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53704-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadPgnoVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadPgnoVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadPgnoVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="53704-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="53704-116">Thread safety</span></span>

<span data-ttu-id="53704-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="53704-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="53704-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="53704-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="53704-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="53704-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53704-120">Referência</span><span class="sxs-lookup"><span data-stu-id="53704-120">Reference</span></span>

[<span data-ttu-id="53704-121">Membros do EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="53704-121">EsentReadPgnoVerifyFailureException members</span></span>](./esentreadpgnoverifyfailureexception-members.md)

[<span data-ttu-id="53704-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="53704-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
