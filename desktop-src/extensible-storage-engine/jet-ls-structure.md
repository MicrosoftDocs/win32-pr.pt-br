---
description: 'Saiba mais sobre: JET_LS estrutura'
title: JET_LS estrutura
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fa85ea0f3117d6f4f9c0c9102f21f2fb1f626f8c115144998c1a4c94c300626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765082"
---
# <a name="jet_ls-structure"></a>JET_LS estrutura

Armazenamento local para um alça ESENT. Usado por [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) e [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_LS membros](./jet-ls-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
