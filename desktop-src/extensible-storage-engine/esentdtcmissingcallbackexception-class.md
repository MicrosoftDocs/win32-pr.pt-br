---
description: 'Saiba mais sobre: classe EsentDTCMissingCallbackException'
title: Classe EsentDTCMissingCallbackException
TOCTitle: EsentDTCMissingCallbackException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdtcmissingcallbackexception(v=EXCHG.10)
ms:contentKeyID: 55101556
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3e9409b03b103ade25fde08fd01949a1a84dbf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505909"
---
# <a name="esentdtcmissingcallbackexception-class"></a><span data-ttu-id="99cab-103">Classe EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="99cab-103">EsentDTCMissingCallbackException class</span></span>

<span data-ttu-id="99cab-104">Classe base para JET_err. DTCMissingCallback exceções.</span><span class="sxs-lookup"><span data-stu-id="99cab-104">Base class for JET_err.DTCMissingCallback exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="99cab-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="99cab-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="99cab-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="99cab-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="99cab-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="99cab-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="99cab-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="99cab-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="99cab-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="99cab-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="99cab-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="99cab-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="99cab-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="99cab-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="99cab-112">Microsoft. ISAM. ESENT. Interop. EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="99cab-112">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>  

<span data-ttu-id="99cab-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99cab-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99cab-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99cab-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99cab-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="99cab-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDTCMissingCallbackException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDTCMissingCallbackException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDTCMissingCallbackException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="99cab-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="99cab-116">Thread safety</span></span>

<span data-ttu-id="99cab-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="99cab-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="99cab-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="99cab-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="99cab-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="99cab-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99cab-120">Referência</span><span class="sxs-lookup"><span data-stu-id="99cab-120">Reference</span></span>

[<span data-ttu-id="99cab-121">Membros do EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="99cab-121">EsentDTCMissingCallbackException members</span></span>](./esentdtcmissingcallbackexception-members.md)

[<span data-ttu-id="99cab-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="99cab-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
