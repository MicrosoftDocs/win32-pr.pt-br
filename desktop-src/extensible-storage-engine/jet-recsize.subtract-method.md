---
description: 'Saiba mais sobre: JET_RECSIZE. Subtrair método'
title: JET_RECSIZE. Método Subtract (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ae459d108db56448d399e6f8de4e50ed912be00a774dbb11ad0bd51d461b0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979596"
---
# <a name="jet_recsizesubtract-method"></a>JET_RECSIZE. Subtrair método

Calcule a diferença em tamanhos entre duas JET_RECSIZE estruturas.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a>Parâmetros

  - s1  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    A primeira JET_RECSIZE.

<!-- end list -->

  - s2  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    O segundo JET_RECSIZE.

#### <a name="return-value"></a>Valor retornado

Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
Um JET_RECSIZE que contém a diferença nos tamanhos entre s1 e s2.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_RECSIZE estrutura](./jet-recsize-structure2.md)

[JET_RECSIZE membros](./jet-recsize-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
