---
description: 'Saiba mais sobre: classe EsentOperationException'
title: Classe EsentOperationException
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105761570"
---
# <a name="esentoperationexception-class"></a>Classe EsentOperationException

Classe base para exceções de operação.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. EsentOperationException  
          

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentOperationException](./esentoperationexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. EsentOperationException  
          [Microsoft. ISAM. ESENT. Interop. EsentBackupAbortByServerException](./esentbackupabortbyserverexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentCheckpointDepthTooDeepException](./esentcheckpointdepthtoodeepexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentClientRequestToStopJetServiceException](./esentclientrequesttostopjetserviceexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentFatalException](./esentfatalexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentInitInProgressException](./esentinitinprogressexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentInternalErrorException](./esentinternalerrorexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentIOException](./esentioexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentNTSystemCallFailedException](./esentntsystemcallfailedexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentOSSnapshotTimeOutException](./esentossnapshottimeoutexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentRecordNotDeletedException](./esentrecordnotdeletedexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentResourceException](./esentresourceexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentTermInProgressException](./esentterminprogressexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUnicodeLanguageValidationFailureException](./esentunicodelanguagevalidationfailureexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUnicodeTranslationFailException](./esentunicodetranslationfailexception-class.md)