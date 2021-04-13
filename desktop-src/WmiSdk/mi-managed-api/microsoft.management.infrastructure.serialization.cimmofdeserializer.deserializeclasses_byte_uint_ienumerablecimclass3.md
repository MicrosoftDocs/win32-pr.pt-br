---
description: 'Saiba mais sobre: método CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable <CimClass> , String, String, OnClassNeeded, GetIncludedFileContent)'
title: Método CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable (CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},System.String,System.String,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 5772ca08a94c27e1ae0b110e05192004b9e4df2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501241"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="8c6dc-103">Método CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> , String, String, OnClassNeeded, GetIncludedFileContent)</span><span class="sxs-lookup"><span data-stu-id="8c6dc-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, String, String, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="8c6dc-104">Desserializa as classes CIM com base em dados serializados, coleção de classes CIM pai, nomes de computador e namespace e retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-104">Deserializes CIM classes based on serialized data, collection of parent CIM classes, computer and namespace names, and callbacks.</span></span>

<span data-ttu-id="8c6dc-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c6dc-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="8c6dc-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="8c6dc-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="8c6dc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c6dc-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    string computerName,
    string namespaceName,
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
    String^ computerName,
    String^ namespaceName,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        computerName:string *
        namespaceName:string *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    computerName As String,
    namespaceName As String,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="8c6dc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c6dc-108">Parameters</span></span>

  - <span data-ttu-id="8c6dc-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="8c6dc-109">serializedData</span></span>  
    <span data-ttu-id="8c6dc-110">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="8c6dc-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="8c6dc-111">Um buffer que contém os dados serializados.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c6dc-112">deslocamento</span><span class="sxs-lookup"><span data-stu-id="8c6dc-112">offset</span></span>  
    <span data-ttu-id="8c6dc-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="8c6dc-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="8c6dc-114">O deslocamento de byte para o local no qual começar a ler os dados.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="8c6dc-115">Quando o método retornar, o deslocamento estará apontando para o próximo byte após as classes desserializadas.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c6dc-116">classes</span><span class="sxs-lookup"><span data-stu-id="8c6dc-116">classes</span></span>  
    <span data-ttu-id="8c6dc-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="8c6dc-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="8c6dc-118">Um cache opcional de classes CIM pai.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c6dc-119">computerName</span><span class="sxs-lookup"><span data-stu-id="8c6dc-119">computerName</span></span>  
    [<span data-ttu-id="8c6dc-120">System.String</span><span class="sxs-lookup"><span data-stu-id="8c6dc-120">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="8c6dc-121">O nome do computador.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-121">The computer name.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c6dc-122">namespaceName</span><span class="sxs-lookup"><span data-stu-id="8c6dc-122">namespaceName</span></span>  
    [<span data-ttu-id="8c6dc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8c6dc-123">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="8c6dc-124">O nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-124">The namespace name.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c6dc-125">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="8c6dc-125">onClassNeededCallback</span></span>  
    <span data-ttu-id="8c6dc-126">Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="8c6dc-126">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="8c6dc-127">Uma função de retorno de chamada usada para fornecer um objeto de classe solicitado durante a desserialização.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-127">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c6dc-128">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="8c6dc-128">getIncludedFileCallback</span></span>  
    <span data-ttu-id="8c6dc-129">Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="8c6dc-129">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="8c6dc-130">Uma função de retorno de chamada usada para fornecer o conteúdo do buffer de arquivo de um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-130">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8c6dc-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c6dc-131">Return value</span></span>

<span data-ttu-id="8c6dc-132">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="8c6dc-132">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="8c6dc-133">Uma [interface \<T\> IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que pode ser usada para enumerar as classes CIM.</span><span class="sxs-lookup"><span data-stu-id="8c6dc-133">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c6dc-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c6dc-134">See also</span></span>

<span data-ttu-id="8c6dc-135">[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c6dc-135">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="8c6dc-136">[Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c6dc-136">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
