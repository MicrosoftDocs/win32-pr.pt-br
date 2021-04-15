---
description: 'Saiba mais sobre: classe EsentLinkNotSupportedException'
title: Classe EsentLinkNotSupportedException
TOCTitle: EsentLinkNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlinknotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55102133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72a8f516e3c3a9c3e2a78f0397442bad9236a6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505907"
---
# <a name="esentlinknotsupportedexception-class"></a>Classe EsentLinkNotSupportedException

Classe base para JET_err. LinkNotSupported exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentLinkNotSupportedException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLinkNotSupportedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentLinkNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLinkNotSupportedException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentLinkNotSupportedException](./esentlinknotsupportedexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
