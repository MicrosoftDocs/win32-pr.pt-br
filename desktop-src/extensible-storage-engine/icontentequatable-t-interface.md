---
description: 'Saiba mais sobre: interface IContentEquatable <T>'
title: Interface IContentEquatable(T)
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6392857aca4b27f15ed3fb8ea13e72c476628ba35115681847a1de5671869def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118077361"
---
# <a name="icontentequatablet-interface"></a>Interface IContentEquatable \<T\>

Interface para objetos que podem ter seu conteúdo em comparação entre si. Isso deve ser usado para comparações de igualdade em objetos de referência mutáveis em que a substituição de Equals() e GetHashCode() não é uma boa ideia.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a>Parâmetros de tipo

  - T  
    O tipo de objetos a ser preterido.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros IContentEquatable \<T\>](./icontentequatable-t-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
