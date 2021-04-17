---
description: 'Saiba mais sobre: classe EsentInternalErrorException'
title: Classe EsentInternalErrorException
TOCTitle: EsentInternalErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInternalErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinternalerrorexception(v=EXCHG.10)
ms:contentKeyID: 55101889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInternalErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInternalErrorException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bf8da47b64ea65965d02d99f15ab181c5bafcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762382"
---
# <a name="esentinternalerrorexception-class"></a>Classe EsentInternalErrorException

Classe base para JET_err. InternalError exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentInternalErrorException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInternalErrorException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentInternalErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInternalErrorException : EsentOperationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentInternalErrorException](./esentinternalerrorexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
