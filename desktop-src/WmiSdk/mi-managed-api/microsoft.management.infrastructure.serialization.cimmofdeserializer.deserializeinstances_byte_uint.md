---
description: 'Saiba mais sobre: método CimMofDeserializer. DeserializeInstances (Byte [], UInt32)'
title: Método CimMofDeserializer. DeserializeInstances (Byte [], UInt32) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 90cc4f9d88afa9f4ec566ff4733995bce8160eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501242"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a><span data-ttu-id="d750b-103">Método CimMofDeserializer. DeserializeInstances (byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="d750b-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="d750b-104">Desserializa instâncias CIM com base em dados serializados.</span><span class="sxs-lookup"><span data-stu-id="d750b-104">Deserializes CIM instances based on serialized data.</span></span>

<span data-ttu-id="d750b-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d750b-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="d750b-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="d750b-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="d750b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d750b-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="d750b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d750b-108">Parameters</span></span>

  - <span data-ttu-id="d750b-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="d750b-109">serializedData</span></span>  
    <span data-ttu-id="d750b-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="d750b-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="d750b-111">Um buffer que contém os dados serializados.</span><span class="sxs-lookup"><span data-stu-id="d750b-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="d750b-112">deslocamento</span><span class="sxs-lookup"><span data-stu-id="d750b-112">offset</span></span>  
    <span data-ttu-id="d750b-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="d750b-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="d750b-114">O deslocamento de byte para o local no qual começar a ler os dados.</span><span class="sxs-lookup"><span data-stu-id="d750b-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="d750b-115">Quando o método retornar, o deslocamento será apontado para o próximo byte após as instâncias desserializadas.</span><span class="sxs-lookup"><span data-stu-id="d750b-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d750b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d750b-116">Return value</span></span>

<span data-ttu-id="d750b-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="d750b-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="d750b-118">Uma [interface \<T\> IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que pode ser usada para enumerar as classes CIM.</span><span class="sxs-lookup"><span data-stu-id="d750b-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="d750b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d750b-119">See also</span></span>

<span data-ttu-id="d750b-120">[Classe CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d750b-120">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="d750b-121">[Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d750b-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
