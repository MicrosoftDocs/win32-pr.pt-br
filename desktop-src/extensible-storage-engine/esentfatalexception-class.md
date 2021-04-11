---
description: 'Saiba mais sobre: classe EsentFatalException'
title: Classe EsentFatalException
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172426"
---
# <a name="esentfatalexception-class"></a>Classe EsentFatalException

Classe base para exceções fatais.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentFatalException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentFatalException](./esentfatalexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentFatalException  
            [Microsoft. ISAM. ESENT. Interop. EsentInstanceUnavailableDueToFatalLogDiskFullException](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInstanceUnavailableException](./esentinstanceunavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogDisabledDueToRecoveryFailureException](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRollbackErrorException](./esentrollbackerrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSectorSizeNotSupportedException](./esentsectorsizenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentUnloadableOSFunctionalityException](./esentunloadableosfunctionalityexception-class.md)