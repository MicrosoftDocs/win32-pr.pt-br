---
description: 'Saiba mais sobre: Classe EsentTooManyOpenTablesException'
title: Classe EsentTooManyOpenTablesException
TOCTitle: EsentTooManyOpenTablesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesexception(v=EXCHG.10)
ms:contentKeyID: 55107362
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa166efdba39c3d8d877768cec8e2163664e6811bfbb3831824e27fc9a2003db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604456"
---
# <a name="esenttoomanyopentablesexception-class"></a>Classe EsentTooManyOpenTablesException

Classe base para JET_err. Exceções TooManyOpenTables.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentQuotaException](./esentquotaexception-class.md)  
              Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyOpenTablesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesException : EsentQuotaException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentTooManyOpenTablesException](./esenttoomanyopentablesexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
