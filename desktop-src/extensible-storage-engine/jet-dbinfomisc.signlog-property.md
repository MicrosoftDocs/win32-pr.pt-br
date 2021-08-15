---
description: 'Saiba mais sobre a propriedade: JET_DBINFOMISC. signLog'
title: Propriedade JET_DBINFOMISC. signLog
TOCTitle: 'signLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.signlog(v=EXCHG.10)
ms:contentKeyID: 39511875
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_signLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3235224ab65ef32eabb5567215284eed7a938672f8e77ccdade40f70e8b85538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486224"
---
# <a name="jet_dbinfomiscsignlog-property"></a>Propriedade JET_DBINFOMISC. signLog

Obtém a assinatura de arquivo de log dos logs usados para modificar o banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property signLog As JET_SIGNATURE
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_SIGNATURE

value = instance.signLog
```

``` csharp
public JET_SIGNATURE signLog { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Membros do JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
