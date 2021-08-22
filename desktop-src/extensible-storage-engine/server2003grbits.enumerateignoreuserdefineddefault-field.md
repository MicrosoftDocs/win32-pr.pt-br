---
description: 'Saiba mais sobre: campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault'
title: Campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b3c110e1aeb54d38805b5ee6ad116ed8fcbbdc7274d0548b582fd88b0e8ac1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978556"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a>Campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault

Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado. Essa opção impedirá o retorno de chamada que computa o valor padrão definido pelo usuário para que a coluna seja chamada ao enumerar os valores para essa coluna.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a>Comentários

essa opção só está disponível para o Windows Server 2003 SP1 e sistemas operacionais posteriores.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Server2003Grbits](./server2003grbits-class.md)

[Membros do Server2003Grbits](./server2003grbits-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
