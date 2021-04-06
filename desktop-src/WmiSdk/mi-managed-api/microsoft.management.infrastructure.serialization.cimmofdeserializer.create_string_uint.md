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
# <a name="cimmofdeserializercreate-method-string-uint32"></a>Método CimMofDeserializer. Create (cadeia de caracteres, UInt32)

Cria e inicializa um desserializador personalizado com base no formato e nos sinalizadores especificados.

**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintaxe

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

#### <a name="parameters"></a>Parâmetros

  - format  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    O formato de serialização. Há suporte apenas para "MI_XML".

<!-- end list -->

  - sinalizadores  
    Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Os sinalizadores de serialização. Deve ser 0.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft. Management. Infrastructure. Serialization. CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)

O objeto desserializador recém-criado.

## <a name="see-also"></a>Confira também

[Classe CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md) 
 [Namespace Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
