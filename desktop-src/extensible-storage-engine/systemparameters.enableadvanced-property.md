---
description: 'Saiba mais sobre: propriedade SystemParameters.EnableAdvanced'
title: Propriedade SystemParameters.EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07fd683ad6f2f0d2a9afd88b46a7786131e15c370c9046945ad3e9594a533391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106990"
---
# <a name="systemparametersenableadvanced-property"></a>Propriedade SystemParameters.EnableAdvanced

Obtém ou define um valor que indica se o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema. Esse parâmetro é usado em conjunto com [a Configuração](./systemparameters.configuration-property.md) para impedir que alguns parâmetros do sistema seja definido fora dos padrões da configuração selecionada. Com suporte no Windows Vista e para cima. Ignorado no Windows XP e Windows Server 2003.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe SystemParameters](./systemparameters-class.md)

[Membros do SystemParameters](./systemparameters-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
