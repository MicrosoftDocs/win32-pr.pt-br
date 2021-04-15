---
description: 'Saiba mais sobre: método CimMofDeserializer. DeserializeClasses (Byte [], UInt32)'
title: Método CimMofDeserializer. DeserializeClasses (Byte [], UInt32) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 983fa9e8fe36b872d05c3140c74f572b7d1ebf50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501243"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a><span data-ttu-id="9292c-103">Método CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="9292c-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="9292c-104">Desserializa classes CIM com base em dados serializados.</span><span class="sxs-lookup"><span data-stu-id="9292c-104">Deserializes CIM classes based on serialized data.</span></span>

<span data-ttu-id="9292c-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9292c-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="9292c-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="9292c-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="9292c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9292c-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="9292c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9292c-108">Parameters</span></span>

  - <span data-ttu-id="9292c-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="9292c-109">serializedData</span></span>  
    <span data-ttu-id="9292c-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="9292c-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="9292c-111">Um buffer que contém os dados serializados.</span><span class="sxs-lookup"><span data-stu-id="9292c-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="9292c-112">deslocamento</span><span class="sxs-lookup"><span data-stu-id="9292c-112">offset</span></span>  
    <span data-ttu-id="9292c-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="9292c-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="9292c-114">O deslocamento de byte para o local no qual começar a ler os dados.</span><span class="sxs-lookup"><span data-stu-id="9292c-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="9292c-115">Quando o método retornar, o deslocamento estará apontando para o próximo byte após as classes desserializadas.</span><span class="sxs-lookup"><span data-stu-id="9292c-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9292c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9292c-116">Return value</span></span>

<span data-ttu-id="9292c-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="9292c-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="9292c-118">Uma [interface \<T\> IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que pode ser usada para enumerar as classes CIM.</span><span class="sxs-lookup"><span data-stu-id="9292c-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="9292c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9292c-119">See also</span></span>

<span data-ttu-id="9292c-120">[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9292c-120">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="9292c-121">[Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9292c-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
