---
description: 'Saiba mais sobre: classe EsentStateException'
title: Classe EsentStateException
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172425"
---
# <a name="esentstateexception-class"></a>Classe EsentStateException

Classe base para exceções de estado.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentStateException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentStateException](./esentstateexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentStateException  
            [Microsoft. ISAM. ESENT. Interop. EsentBackupInProgressException](./esentbackupinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBackupNotAllowedYetException](./esentbackupnotallowedyetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadItagSequenceException](./esentbaditagsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBufferTooSmallException](./esentbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCallbackFailedException](./esentcallbackfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseAlreadyUpgradedException](./esentdatabasealreadyupgradedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseFailedIncrementalReseedException](./esentdatabasefailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseIncompleteUpgradeException](./esentdatabaseincompleteupgradeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseLeakInSpaceException](./esentdatabaseleakinspaceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDirtyShutdownException](./esentdirtyshutdownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileNotFoundException](./esentfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexInUseException](./esentindexinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexNotFoundException](./esentindexnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidBufferSizeException](./esentinvalidbuffersizeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidLogDataSequenceException](./esentinvalidlogdatasequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentKeyDuplicateException](./esentkeyduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentKeyTruncatedException](./esentkeytruncatedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogFileSizeMismatchDatabasesConsistentException](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogSectorSizeMismatchDatabasesConsistentException](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLSNotSetException](./esentlsnotsetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingFullBackupException](./esentmissingfullbackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMultiValuedDuplicateAfterTruncationException](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMultiValuedDuplicateException](./esentmultivaluedduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNoAttachmentsFailedIncrementalReseedException](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNoBackupException](./esentnobackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNoCurrentRecordException](./esentnocurrentrecordexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentObjectNotFoundException](./esentobjectnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOSSnapshotNotAllowedException](./esentossnapshotnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordDeletedException](./esentrecorddeletedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordNotFoundException](./esentrecordnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordTooBigException](./esentrecordtoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordTooBigForBackwardCompatibilityException](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithErrorsException](./esentrecoveredwitherrorsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithoutUndoDatabasesConsistentException](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithoutUndoException](./esentrecoveredwithoutundoexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRestoreInProgressException](./esentrestoreinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSeparatedLongValueException](./esentseparatedlongvalueexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSurrogateBackupInProgressException](./esentsurrogatebackupinprogressexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTableDuplicateException](./esenttableduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTableInUseException](./esenttableinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTestInjectionNotSupportedException](./esenttestinjectionnotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentWriteConflictException](./esentwriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentWriteConflictPrimaryIndexException](./esentwriteconflictprimaryindexexception-class.md)