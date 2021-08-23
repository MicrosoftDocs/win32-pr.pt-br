---
description: 'Saiba mais sobre: JET_SESID estrutura'
title: JET_SESID estrutura
TOCTitle: JET_SESID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid(v=EXCHG.10)
ms:contentKeyID: 39516065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 704d4dc763bb886d2c09e0aa6e6c942f0c171dcf03041e3b35db5ac781863d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979416"
---
# <a name="jet_sesid-structure"></a>JET_SESID estrutura

Um JET_SESID contém um handle para a sessão a ser usada para chamadas para o JET APIr-.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Structure JET_SESID _
    Implements IEquatable(Of JET_SESID), IFormattable
'Usage
Dim instance As JET_SESID
```

``` csharp
public struct JET_SESID : IEquatable<JET_SESID>, 
    IFormattable
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_SESID membros](./jet-sesid-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
