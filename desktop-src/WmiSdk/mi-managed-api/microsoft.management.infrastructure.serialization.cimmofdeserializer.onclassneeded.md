---
description: 'Saiba mais sobre: CimMofDeserializer. OnClassNeeded delegate (String, String, String)'
title: Delegado CimMofDeserializer.OnClassNeeded (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::OnClassNeeded
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: fd7dd361483b951783ccb47f7295589611bbb5cce98dab5b13e96613a479c054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818332"
---
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a>CimMofDeserializer. OnClassNeeded delegate (String, String, String)

Representa um retorno de chamada para recuperar uma classe CIM para o servidor, o namespace e o nome de classe especificados.

**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintaxe

``` csharp
public delegate CimClass OnClassNeeded(
    string serverName,
    string namespaceName,
    string className
)
```

``` c++
public delegate CimClass^ OnClassNeeded(
    String^ serverName,
    String^ namespaceName,
    String^ className
)
```

``` fsharp
type OnClassNeeded = 
    delegate of 
        serverName:string *
        namespaceName:string *
        className:string -> CimClass
```

``` vb
Public Delegate Function OnClassNeeded (
    serverName As String,
    namespaceName As String,
    className As String,
) As CimClass
```

#### <a name="parameters"></a>Parâmetros

  - serverName  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    O nome do servidor para a classe CIM.

<!-- end list -->

  - namespaceName  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    O nome do namespace para a classe CIM.

<!-- end list -->

  - className  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    O nome da classe para a classe CIM.

#### <a name="return-value"></a>Valor Retornado

Tipo: [classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))

Retorna a classe CIM correspondente aos argumentos especificados, ou **NULL** se a classe não puder ser encontrada.

## <a name="see-also"></a>Consulte Também

[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
