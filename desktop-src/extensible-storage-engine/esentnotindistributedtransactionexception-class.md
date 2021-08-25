---
description: 'Saiba mais sobre: Classe EsentNotInDistributedTransactionException'
title: Classe EsentNotInDistributedTransactionException
TOCTitle: EsentNotInDistributedTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotindistributedtransactionexception(v=EXCHG.10)
ms:contentKeyID: 55102293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d07b185825ed1225756e323f2f7924a7a9e4d596722b2efaca5f1e5e7b2676ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836246"
---
# <a name="esentnotindistributedtransactionexception-class"></a>Classe EsentNotInDistributedTransactionException

Classe base para JET_err. Exceções NotInDistributedTransaction.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInDistributedTransactionException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentNotInDistributedTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInDistributedTransactionException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentNotInDistributedTransactionException](./esentnotindistributedtransactionexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
