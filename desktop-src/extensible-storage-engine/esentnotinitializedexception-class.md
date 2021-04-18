---
description: 'Saiba mais sobre: classe EsentNotInitializedException'
title: Classe EsentNotInitializedException
TOCTitle: EsentNotInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55102300
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInitializedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c026bf7e5e6f9cb132f5c1ca19d23f180b325906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784526"
---
# <a name="esentnotinitializedexception-class"></a>Classe EsentNotInitializedException

Classe base para JET_err. Exceções não inicializadas.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentNotInitializedException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInitializedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNotInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInitializedException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentNotInitializedException](./esentnotinitializedexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
