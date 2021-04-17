---
description: 'Saiba mais sobre: classe EsentBadDbSignatureException'
title: Classe EsentBadDbSignatureException
TOCTitle: EsentBadDbSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbaddbsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55107255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c0adf077cf0665c6bee2246c66af882a397c46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784588"
---
# <a name="esentbaddbsignatureexception-class"></a><span data-ttu-id="4ccaf-103">Classe EsentBadDbSignatureException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-103">EsentBadDbSignatureException class</span></span>

<span data-ttu-id="4ccaf-104">Classe base para JET_err. BadDbSignature exceções.</span><span class="sxs-lookup"><span data-stu-id="4ccaf-104">Base class for JET_err.BadDbSignature exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4ccaf-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="4ccaf-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4ccaf-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4ccaf-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4ccaf-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4ccaf-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4ccaf-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4ccaf-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4ccaf-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4ccaf-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="4ccaf-112">Microsoft. ISAM. ESENT. Interop. EsentBadDbSignatureException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-112">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>  

<span data-ttu-id="4ccaf-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ccaf-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ccaf-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ccaf-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccaf-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ccaf-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadDbSignatureException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadDbSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadDbSignatureException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="4ccaf-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="4ccaf-116">Thread safety</span></span>

<span data-ttu-id="4ccaf-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="4ccaf-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4ccaf-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="4ccaf-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ccaf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ccaf-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ccaf-120">Referência</span><span class="sxs-lookup"><span data-stu-id="4ccaf-120">Reference</span></span>

[<span data-ttu-id="4ccaf-121">Membros do EsentBadDbSignatureException</span><span class="sxs-lookup"><span data-stu-id="4ccaf-121">EsentBadDbSignatureException members</span></span>](./esentbaddbsignatureexception-members.md)

[<span data-ttu-id="4ccaf-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4ccaf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
