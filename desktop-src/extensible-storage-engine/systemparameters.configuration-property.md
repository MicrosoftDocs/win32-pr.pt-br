---
description: 'Saiba mais sobre: SystemParameters.ConfigPropriedade uração'
title: SystemParameters.ConfigPropriedade uração
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828631"
---
# <a name="systemparametersconfiguration-property"></a>SystemParameters.ConfigPropriedade uração

Obtém ou define um valor que especifica os valores padrão para o conjunto inteiro de parâmetros do sistema. Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração. Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão. Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória. Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais. Com suporte no Windows Vista e em cima. Ignorado no Windows XP e no Windows Server 2003.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe SystemParameters](./systemparameters-class.md)

[Membros do SystemParameters](./systemparameters-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
