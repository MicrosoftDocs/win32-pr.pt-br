---
description: 'Saiba mais sobre a propriedade: Instanceparameters. DbExtensionSize'
title: Propriedade instanceparameters. DbExtensionSize
TOCTitle: 'DbExtensionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbextensionsize(v=EXCHG.10)
ms:contentKeyID: 55107443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbExtensionSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402c37ca649a9e9ff70435c8a8ef58f79376842b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765365"
---
# <a name="instanceparametersdbextensionsize-property"></a>Propriedade instanceparameters. DbExtensionSize

Obtém ou define o número de páginas que são adicionadas a um arquivo de banco de dados cada vez que ele precisa aumentar para acomodar mais informações.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property DbExtensionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbExtensionSize

instance.DbExtensionSize = value
```

``` csharp
public int DbExtensionSize { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe instanceparameters](./instanceparameters-class.md)

[Membros de instanceparameters](./instanceparameters-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
