---
description: 'Saiba mais sobre: método CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable <CimClass> , OnClassNeeded, GetIncludedFileContent)'
title: Método CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable (CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 5fd78e1c377db3a8fba0005539bb5d7c28cab232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296516"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="97dff-103">Método CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> , OnClassNeeded, GetIncludedFileContent)</span><span class="sxs-lookup"><span data-stu-id="97dff-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="97dff-104">Desserializa as classes CIM com base em dados serializados, uma coleção de classes CIM pai e retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="97dff-104">Deserializes CIM classes based on serialized data, a collection of parent CIM classes, and callbacks.</span></span>

<span data-ttu-id="97dff-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97dff-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="97dff-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="97dff-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="97dff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97dff-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="97dff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97dff-108">Parameters</span></span>

  - <span data-ttu-id="97dff-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="97dff-109">serializedData</span></span>  
    <span data-ttu-id="97dff-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="97dff-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="97dff-111">Um buffer que contém os dados serializados.</span><span class="sxs-lookup"><span data-stu-id="97dff-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="97dff-112">deslocamento</span><span class="sxs-lookup"><span data-stu-id="97dff-112">offset</span></span>  
    <span data-ttu-id="97dff-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="97dff-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="97dff-114">O deslocamento de byte para o local no qual começar a ler os dados.</span><span class="sxs-lookup"><span data-stu-id="97dff-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="97dff-115">Quando o método retornar, o deslocamento estará apontando para o próximo byte após as classes desserializadas.</span><span class="sxs-lookup"><span data-stu-id="97dff-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="97dff-116">classes</span><span class="sxs-lookup"><span data-stu-id="97dff-116">classes</span></span>  
    <span data-ttu-id="97dff-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="97dff-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="97dff-118">Um cache opcional de classes CIM pai.</span><span class="sxs-lookup"><span data-stu-id="97dff-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="97dff-119">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="97dff-119">onClassNeededCallback</span></span>  
    <span data-ttu-id="97dff-120">Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="97dff-120">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="97dff-121">Uma função de retorno de chamada usada para fornecer um objeto de classe solicitado durante a desserialização.</span><span class="sxs-lookup"><span data-stu-id="97dff-121">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="97dff-122">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="97dff-122">getIncludedFileCallback</span></span>  
    <span data-ttu-id="97dff-123">Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="97dff-123">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="97dff-124">Uma função de retorno de chamada usada para fornecer o conteúdo do buffer de arquivo de um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="97dff-124">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="97dff-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97dff-125">Return value</span></span>

<span data-ttu-id="97dff-126">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="97dff-126">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="97dff-127">Uma [interface \<T\> IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que pode ser usada para enumerar as classes CIM.</span><span class="sxs-lookup"><span data-stu-id="97dff-127">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="97dff-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="97dff-128">See also</span></span>

<span data-ttu-id="97dff-129">[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97dff-129">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="97dff-130">[Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97dff-130">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
