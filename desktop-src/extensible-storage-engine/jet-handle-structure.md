---
description: 'Saiba mais sobre: estrutura de JET_HANDLE'
title: Estrutura de JET_HANDLE
TOCTitle: JET_HANDLE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_HANDLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle(v=EXCHG.10)
ms:contentKeyID: 39513615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6b1baaaba7162bc8eb405ca0184a4f8dac32290b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297415"
---
# <a name="jet_handle-structure"></a>Estrutura de JET_HANDLE

Um JET_HANDLE contém um identificador genérico.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Structure JET_HANDLE _
    Implements IEquatable(Of JET_HANDLE), IFormattable
'Usage
Dim instance As JET_HANDLE
```

``` csharp
public struct JET_HANDLE : IEquatable<JET_HANDLE>, 
    IFormattable
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do JET_HANDLE](./jet-handle-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
