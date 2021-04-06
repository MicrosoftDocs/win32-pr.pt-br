---
description: 'Saiba mais sobre: método CimMofDeserializer. Create (cadeia de caracteres, UInt32)'
title: Método CimMofDeserializer.Create (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.Create method (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create(System.String,System.UInt32)
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
- Microsoft::Management::Infrastructure::.Serialization::CimMofDeserializer::Create
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: c8f9b30fb0b9b06c2f1aaeb1fcfcaf65fb3606d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011544"
---
# <a name="cimmofdeserializercreate-method-string-uint32"></a><span data-ttu-id="80839-103">Método CimMofDeserializer. Create (cadeia de caracteres, UInt32)</span><span class="sxs-lookup"><span data-stu-id="80839-103">CimMofDeserializer.Create method (String, UInt32)</span></span>

<span data-ttu-id="80839-104">Cria e inicializa um desserializador personalizado com base no formato e nos sinalizadores especificados.</span><span class="sxs-lookup"><span data-stu-id="80839-104">Creates and initializes a custom deserializer, based on the specified format and flags.</span></span>

<span data-ttu-id="80839-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80839-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="80839-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="80839-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="80839-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80839-107">Syntax</span></span>

``` csharp
public static CimMofDeserializer Create(
    string format,
    uint flags
)
```

``` c++
public:
static CimMofDeserializer^ Create(
    String^ format,
    unsigned int flags
)
```

``` fsharp
static member Create : 
        format:string *
        flags:uint32 -> CimMofDeserializer
```

``` vb
Public Shared Function Create (
    format As String,
    flags As UInteger
) As CimMofDeserializer
```

#### <a name="parameters"></a><span data-ttu-id="80839-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80839-108">Parameters</span></span>

  - <span data-ttu-id="80839-109">format</span><span class="sxs-lookup"><span data-stu-id="80839-109">format</span></span>  
    <span data-ttu-id="80839-110">Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="80839-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="80839-111">O formato de serialização.</span><span class="sxs-lookup"><span data-stu-id="80839-111">The serialization format.</span></span> <span data-ttu-id="80839-112">Há suporte apenas para "MI_XML".</span><span class="sxs-lookup"><span data-stu-id="80839-112">Only "MI_XML" is supported.</span></span>

<!-- end list -->

  - <span data-ttu-id="80839-113">sinalizadores</span><span class="sxs-lookup"><span data-stu-id="80839-113">flags</span></span>  
    <span data-ttu-id="80839-114">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="80839-114">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="80839-115">Os sinalizadores de serialização.</span><span class="sxs-lookup"><span data-stu-id="80839-115">The serialization flags.</span></span> <span data-ttu-id="80839-116">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="80839-116">Must be 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="80839-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80839-117">Return value</span></span>

<span data-ttu-id="80839-118">Tipo: [Microsoft. Management. Infrastructure. Serialization. CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)</span><span class="sxs-lookup"><span data-stu-id="80839-118">Type: [Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)</span></span>

<span data-ttu-id="80839-119">O objeto desserializador recém-criado.</span><span class="sxs-lookup"><span data-stu-id="80839-119">The newly created deserializer object.</span></span>

## <a name="see-also"></a><span data-ttu-id="80839-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="80839-120">See also</span></span>

<span data-ttu-id="80839-121">[Classe CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md) 
 [Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80839-121">[CimMofDeserializer class](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)
[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
