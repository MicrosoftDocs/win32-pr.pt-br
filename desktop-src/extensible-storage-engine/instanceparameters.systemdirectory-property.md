---
description: 'Saiba mais sobre: InstanceParameters.Syspropriedade temDirectory'
title: InstanceParameters.Syspropriedade temDirectory
TOCTitle: 'SystemDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.systemdirectory(v=EXCHG.10)
ms:contentKeyID: 55103561
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_SystemDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 870a039e15e42170dc6ae85127866cd2075773468ac71fcc5b8d7b3ee56635c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017656"
---
# <a name="instanceparameterssystemdirectory-property"></a>InstanceParameters.Syspropriedade temDirectory

Obtém ou define o caminho do sistema de arquivos relativo ou absoluto da pasta que conterá o arquivo de ponto de verificação para a instância.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property SystemDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.SystemDirectory

instance.SystemDirectory = value
```

``` csharp
public string SystemDirectory { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe InstanceParameters](./instanceparameters-class.md)

[Membros instanceParameters](./instanceparameters-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
