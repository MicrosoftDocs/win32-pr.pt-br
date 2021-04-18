---
description: 'Saiba mais sobre: estrutura de JET_LOGTIME'
title: Estrutura de JET_LOGTIME
TOCTitle: JET_LOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime(v=EXCHG.10)
ms:contentKeyID: 39510198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617911c8f9f0246a836de11d9530536bf9c6e6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813307"
---
# <a name="jet_logtime-structure"></a>Estrutura de JET_LOGTIME

Descreve uma data/hora.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_LOGTIME _
    Implements IEquatable(Of JET_LOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_LOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_LOGTIME : IEquatable<JET_LOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do JET_LOGTIME](./jet-logtime-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
