---
description: 'Saiba mais sobre: Classe table'
title: Classe Table
TOCTitle: Table class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table(v=EXCHG.10)
ms:contentKeyID: 55104053
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84f7290ca7681d9ed25a2a76e80fd77685312dd6845eebdd3002c29e9f28859b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070851"
---
# <a name="table-class"></a>Classe Table

Uma classe que encapsula um JET_TABLEID em um objeto descartável. Isso abre uma tabela existente. Para criar uma tabela, use o método JetCreateTable.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [Microsoft.Isam.Esent.Interop.EsentResource](./esentresource-class.md)  
    Microsoft.Isam.Esent.Interop.Table  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Class Table _
    Inherits EsentResource
'Usage
Dim instance As Table
```

``` csharp
public class Table : EsentResource
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros da tabela](./table-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
