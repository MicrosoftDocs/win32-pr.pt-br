---
description: 'Saiba mais sobre a propriedade: Instanceparameters. AlternateDatabaseRecoveryDirectory'
title: Propriedade instanceparameters. AlternateDatabaseRecoveryDirectory
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813989"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a>Propriedade instanceparameters. AlternateDatabaseRecoveryDirectory

Obtém ou define o caminho relativo ou absoluto do sistema de arquivos de uma pasta na qual a recuperação de falha ou uma operação de restauração pode encontrar os bancos de dados referenciados no log de transações na pasta especificada.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="remarks"></a>Comentários

Esse parâmetro é ignorado no Windows XP.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe instanceparameters](./instanceparameters-class.md)

[Membros de instanceparameters](./instanceparameters-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
