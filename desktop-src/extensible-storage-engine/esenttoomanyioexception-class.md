---
description: 'Saiba mais sobre: classe EsentTooManyIOException'
title: Classe EsentTooManyIOException
TOCTitle: EsentTooManyIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyioexception(v=EXCHG.10)
ms:contentKeyID: 55103065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyIOException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf5ae411c13f6b7ed68ee869ef0ec5cca3631b56594727ac45064aaab2a0eaed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850466"
---
# <a name="esenttoomanyioexception-class"></a>Classe EsentTooManyIOException

Classe base para JET_err. TooManyIO exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentTooManyIOException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyIOException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentTooManyIOException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyIOException : EsentResourceException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentTooManyIOException](./esenttoomanyioexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
