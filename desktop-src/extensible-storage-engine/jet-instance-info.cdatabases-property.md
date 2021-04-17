---
description: 'Saiba mais sobre a propriedade: JET_INSTANCE_INFO. cDatabases'
title: Propriedade JET_INSTANCE_INFO. cDatabases
TOCTitle: 'cDatabases property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.cdatabases(v=EXCHG.10)
ms:contentKeyID: 55103699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.set_cDatabases
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_cDatabases
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc6d81fc4389caf57ae5375a5548a1832b0cebfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756115"
---
# <a name="jet_instance_infocdatabases-property"></a>Propriedade JET_INSTANCE_INFO. cDatabases

Obtém o número de bancos de dados que estão anexados à instância de Database.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cDatabases As Integer
    Get
    Private Set
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As Integer

value = instance.cDatabases
```

``` csharp
public int cDatabases { get; private set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INSTANCE_INFO](./jet-instance-info-class.md)

[Membros do JET_INSTANCE_INFO](./jet-instance-info-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
