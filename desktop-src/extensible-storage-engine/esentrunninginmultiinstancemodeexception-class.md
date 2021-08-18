---
description: 'Saiba mais sobre: Classe EsentRunningInMultiInstanceModeException'
title: Classe EsentRunningInMultiInstanceModeException
TOCTitle: EsentRunningInMultiInstanceModeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrunninginmultiinstancemodeexception(v=EXCHG.10)
ms:contentKeyID: 55102667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3183b3ec68ae86874d8b450a55c236f6787f009ba850c66a5090e87d8d429f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118981826"
---
# <a name="esentrunninginmultiinstancemodeexception-class"></a>Classe EsentRunningInMultiInstanceModeException

Classe base para JET_err. Exceções RunningInMultiInstanceMode.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRunningInMultiInstanceModeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRunningInMultiInstanceModeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRunningInMultiInstanceModeException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentRunningInMultiInstanceModeException](./esentrunninginmultiinstancemodeexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
