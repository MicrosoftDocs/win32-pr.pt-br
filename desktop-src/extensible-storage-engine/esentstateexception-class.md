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
ms.openlocfilehash: 125680795e7cb1bda2a63dd871ef02bf4595970ba774fa74a72490de628f1b5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064046"
---
# <a name="esentstateexception-class"></a>Classe EsentStateException

Classe base para exceções de Estado.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentStateException  
            

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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

[Membros EsentStateException](./esentstateexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentStateException  
            [Microsoft.Isam.Esent.Interop.EsentBackupInProgressException](./esentbackupinprogressexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException](./esentbackupnotallowedyetexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException](./esentbaditagsequenceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException](./esentbuffertoosmallexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCallbackFailedException](./esentcallbackfailedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException](./esentdatabasealreadyupgradedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException](./esentdatabasefailedincrementalreseedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException](./esentdatabaseincompleteupgradeexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException](./esentdatabaseleakinspaceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException](./esentdirtyshutdownexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileNotFoundException](./esentfilenotfoundexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentIndexInUseException](./esentindexinuseexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException](./esentindexnotfoundexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException](./esentinvalidbuffersizeexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException](./esentinvalidlogdatasequenceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException](./esentkeyduplicateexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException](./esentkeytruncatedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchDatabasesConsistentException](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLSNotSetException](./esentlsnotsetexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException](./esentmissingfullbackupexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException](./esentmultivaluedduplicateexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentNoAttachmentsFailedIncrementalReseedException](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentNoBackupException](./esentnobackupexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException](./esentnocurrentrecordexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException](./esentobjectnotfoundexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException](./esentossnapshotnotallowedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecordDeletedException](./esentrecorddeletedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException](./esentrecordnotfoundexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecordTooBigException](./esentrecordtoobigexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException](./esentrecoveredwitherrorsexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException](./esentrecoveredwithoutundoexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException](./esentrestoreinprogressexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException](./esentseparatedlongvalueexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException](./esentsurrogatebackupinprogressexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentTableDuplicateException](./esenttableduplicateexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentTableInUseException](./esenttableinuseexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException](./esenttestinjectionnotsupportedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentWriteConflictException](./esentwriteconflictexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException](./esentwriteconflictprimaryindexexception-class.md)