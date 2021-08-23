---
description: 'Saiba mais sobre: JET_TABLECREATE. Método ContentEquals'
title: JET_TABLECREATE. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103993
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 653aec23752d992059def6698b1d1eabadbdfc52d8988c047720648b844ebf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979205"
---
# <a name="jet_tablecreatecontentequals-method"></a>JET_TABLECREATE. Método ContentEquals

Retorna um valor que indica se essa instância é igual a outra instância.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_TABLECREATE _
) As Boolean
'Usage
Dim instance As JET_TABLECREATE
Dim other As JET_TABLECREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_TABLECREATE other
)
```

#### <a name="parameters"></a>Parâmetros

  - outros  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)  
    
    Uma instância a ser comparada com essa instância.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias são iguais.  

#### <a name="implements"></a>Implementações

[IContentEquatable. \<T\> ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_TABLECREATE classe](./jet-tablecreate-class.md)

[JET_TABLECREATE membros](./jet-tablecreate-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
