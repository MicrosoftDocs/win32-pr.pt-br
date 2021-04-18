---
description: 'Saiba mais sobre: classe EsentInconsistentException'
title: Classe EsentInconsistentException
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105812805"
---
# <a name="esentinconsistentexception-class"></a>Classe EsentInconsistentException

Classe base para exceções inconsistentes.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentInconsistentException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentInconsistentException](./esentinconsistentexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentInconsistentException  
            [Microsoft. ISAM. ESENT. Interop. EsentAttachedDatabaseMismatchException](./esentattacheddatabasemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadCheckpointSignatureException](./esentbadcheckpointsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadLogSignatureException](./esentbadlogsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadLogVersionException](./esentbadlogversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCheckpointFileNotFoundException](./esentcheckpointfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentConsistentTimeMismatchException](./esentconsistenttimemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseDirtyShutdownException](./esentdatabasedirtyshutdownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseIncompleteIncrementalReseedException](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseLogSetMismatchException](./esentdatabaselogsetmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDbTimeTooNewException](./esentdbtimetoonewexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDbTimeTooOldException](./esentdbtimetoooldexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentEndingRestoreLogTooLowException](./esentendingrestorelogtoolowexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentExistingLogFileHasBadSignatureException](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentExistingLogFileIsNotContiguousException](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileInvalidTypeException](./esentfileinvalidtypeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentGivenLogFileHasBadSignatureException](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentGivenLogFileIsNotContiguousException](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidCreateDbVersionException](./esentinvalidcreatedbversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidDatabaseVersionException](./esentinvaliddatabaseversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogGenerationMismatchException](./esentloggenerationmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingCurrentLogFilesException](./esentmissingcurrentlogfilesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingFileToBackupException](./esentmissingfiletobackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingRestoreLogFilesException](./esentmissingrestorelogfilesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPageSizeMismatchException](./esentpagesizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRequiredLogFilesMissingException](./esentrequiredlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentStartingRestoreLogTooHighException](./esentstartingrestorelogtoohighexception-class.md)