---
description: 'Saiba mais sobre: Classe EsentCurrencyStackOutOfMemoryException'
title: Classe EsentCurrencyStackOutOfMemoryException
TOCTitle: EsentCurrencyStackOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcurrencystackoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55101301
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 317067e55cef0a6079d319fc4a199f6d973421fe9f35fd4b5559e8d09967f728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119041654"
---
# <a name="esentcurrencystackoutofmemoryexception-class"></a>Classe EsentCurrencyStackOutOfMemoryException

Classe base para JET_err. Exceções CurrencyStackOutOfMemory.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCurrencyStackOutOfMemoryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentCurrencyStackOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCurrencyStackOutOfMemoryException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentCurrencyStackOutOfMemoryException](./esentcurrencystackoutofmemoryexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
