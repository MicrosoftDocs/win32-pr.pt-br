---
description: 'Saiba mais sobre: Método Api.JetGetInstanceInfo'
title: Método Api.JetGetInstanceInfo
TOCTitle: 'JetGetInstanceInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo(System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetinstanceinfo(v=EXCHG.10)
ms:contentKeyID: 55100729
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4abe0878f0a63b8492135632c0fe8e771e1af98e509f7753eaf38e898621453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719140"
---
# <a name="apijetgetinstanceinfo-method"></a>Método Api.JetGetInstanceInfo

Recupera informações sobre as instâncias que estão em execução.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetInstanceInfo ( _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO() _
)
'Usage
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()

Api.JetGetInstanceInfo(numInstances, _
    instances)
```

``` csharp
public static void JetGetInstanceInfo(
    out int numInstances,
    out JET_INSTANCE_INFO[] instances
)
```

#### <a name="parameters"></a>Parâmetros

  - numInstances  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Retorna o número de instâncias.

<!-- end list -->

  - instances  
    Tipo: \[\]  
    
    Retorna uma matriz de objetos de informações de instância, um para cada instância em execução.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
