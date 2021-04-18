---
description: 'Saiba mais sobre: classe EsentInvalidSettingsException'
title: Classe EsentInvalidSettingsException
TOCTitle: EsentInvalidSettingsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidsettingsexception(v=EXCHG.10)
ms:contentKeyID: 55102084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb8f3983a906182baf394f2e35a9f7f9e288de01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810886"
---
# <a name="esentinvalidsettingsexception-class"></a><span data-ttu-id="39b8d-103">Classe EsentInvalidSettingsException</span><span class="sxs-lookup"><span data-stu-id="39b8d-103">EsentInvalidSettingsException class</span></span>

<span data-ttu-id="39b8d-104">Classe base para JET_err. InvalidSettings exceções.</span><span class="sxs-lookup"><span data-stu-id="39b8d-104">Base class for JET_err.InvalidSettings exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="39b8d-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="39b8d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="39b8d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="39b8d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="39b8d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="39b8d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="39b8d-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="39b8d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="39b8d-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="39b8d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="39b8d-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="39b8d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="39b8d-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="39b8d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="39b8d-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidSettingsException</span><span class="sxs-lookup"><span data-stu-id="39b8d-112">Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException</span></span>  

<span data-ttu-id="39b8d-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39b8d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39b8d-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39b8d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39b8d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="39b8d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidSettingsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidSettingsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidSettingsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="39b8d-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="39b8d-116">Thread safety</span></span>

<span data-ttu-id="39b8d-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="39b8d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="39b8d-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="39b8d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="39b8d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="39b8d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39b8d-120">Referência</span><span class="sxs-lookup"><span data-stu-id="39b8d-120">Reference</span></span>

[<span data-ttu-id="39b8d-121">Membros do EsentInvalidSettingsException</span><span class="sxs-lookup"><span data-stu-id="39b8d-121">EsentInvalidSettingsException members</span></span>](./esentinvalidsettingsexception-members.md)

[<span data-ttu-id="39b8d-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="39b8d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
