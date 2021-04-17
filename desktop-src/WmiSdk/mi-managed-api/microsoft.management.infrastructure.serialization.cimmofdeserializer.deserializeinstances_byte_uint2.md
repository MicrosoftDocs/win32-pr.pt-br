---
description: 'Saiba mais sobre: método CimMofDeserializer. DeserializeInstances (Byte [], UInt32, OnClassNeeded, GetIncludedFileContent)'
title: Método CimMofDeserializer. DeserializeInstances (Byte [], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 17a8a84f841f07439b716909fbc8d63232032263
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791096"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32-onclassneeded-getincludedfilecontent"></a>Método CimMofDeserializer. DeserializeInstances (byte \[ \] , UInt32, OnClassNeeded, GetIncludedFileContent)

Desserializa instâncias de CIM com base em dados serializados e retornos de chamada.

**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintaxe

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a>Parâmetros

  - serializedData  
    Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Um buffer que contém os dados serializados.

<!-- end list -->

  - deslocamento  
    Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    O deslocamento de byte para o local no qual começar a ler os dados. Quando o método retornar, o deslocamento será apontado para o próximo byte após as instâncias desserializadas.

<!-- end list -->

  - onClassNeededCallback  
    Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    Uma função de retorno de chamada usada para fornecer um objeto de classe solicitado durante a desserialização.

<!-- end list -->

  - getIncludedFileCallback  
    Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    Uma função de retorno de chamada usada para fornecer o conteúdo do buffer de arquivo de um arquivo especificado.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

Uma [interface \<T\> IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que pode ser usada para enumerar as classes CIM.

## <a name="see-also"></a>Confira também

[Classe CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
