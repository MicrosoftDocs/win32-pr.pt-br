---
description: 'Saiba mais sobre: classe EsentDatabaseUnavailableException'
title: Classe EsentDatabaseUnavailableException
TOCTitle: EsentDatabaseUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101562
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3210a3d5a546d6c27294473137b0306f87f0888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165160"
---
# <a name="esentdatabaseunavailableexception-class"></a>Classe EsentDatabaseUnavailableException

Classe base para JET_err. DatabaseUnavailable exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentDatabaseUnavailableException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseUnavailableException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabaseUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseUnavailableException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentDatabaseUnavailableException](./esentdatabaseunavailableexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
