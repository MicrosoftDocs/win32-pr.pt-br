---
description: 'Saiba mais sobre: JET_RETINFO. Método ContentEquals'
title: JET_RETINFO. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103869
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bac25d8184b1dd62e8c622cbdd79df42d4996314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647397"
---
# <a name="jet_retinfocontentequals-method"></a>JET_RETINFO. Método ContentEquals

Retorna um valor que indica se essa instância é igual a outra instância.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RETINFO _
) As Boolean
'Usage
Dim instance As JET_RETINFO
Dim other As JET_RETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RETINFO other
)
```

#### <a name="parameters"></a>Parâmetros

  - outros  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Uma instância para comparar com esta instância.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se as duas instâncias forem iguais.  

#### <a name="implements"></a>Implementações

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_RETINFO](./jet-retinfo-class.md)

[Membros do JET_RETINFO](./jet-retinfo-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
