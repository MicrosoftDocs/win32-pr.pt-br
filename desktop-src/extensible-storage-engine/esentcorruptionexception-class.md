---
description: 'Saiba mais sobre: classe EsentCorruptionException'
title: Classe EsentCorruptionException
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac3d1884f41602490af23e3d63a388cd4d28e56fe92d80055ad8aaf462e0ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020896"
---
# <a name="esentcorruptionexception-class"></a>Classe EsentCorruptionException

Classe base para exceções de corrupção.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentCorruptionException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentCorruptionException](./esentcorruptionexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentCorruptionException  
            [Microsoft. ISAM. ESENT. Interop. EsentBadEmptyPageException](./esentbademptypageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadPageLinkException](./esentbadpagelinkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadParentPageLinkException](./esentbadparentpagelinkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCatalogCorruptedException](./esentcatalogcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCheckpointCorruptException](./esentcheckpointcorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCommittedLogFileCorruptException](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCommittedLogFilesMissingException](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseBufferDependenciesCorruptedException](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseCorruptedException](./esentdatabasecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDbTimeCorruptedException](./esentdbtimecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDecompressionFailedException](./esentdecompressionfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDerivedColumnCorruptionException](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDiskReadVerificationFailureException](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileIOBeyondEOFException](./esentfileiobeyondeofexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileSystemCorruptionException](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexBuildCorruptedException](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidLogSequenceException](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogCorruptDuringHardRecoveryException](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogCorruptDuringHardRestoreException](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogCorruptedException](./esentlogcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogFileCorruptException](./esentlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogReadVerifyFailureException](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogTornWriteDuringHardRecoveryException](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogTornWriteDuringHardRestoreException](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLVCorruptedException](./esentlvcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingLogFileException](./esentmissinglogfileexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingPreviousLogFileException](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPageNotInitializedException](./esentpagenotinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPrimaryIndexCorruptedException](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentReadLostFlushVerifyFailureException](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentReadPgnoVerifyFailureException](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentReadVerifyFailureException](./esentreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordFormatConversionFailedException](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecoveryVerifyFailureException](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRedoAbruptEndedException](./esentredoabruptendedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSecondaryIndexCorruptedException](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCorruptedException](./esentspavailextcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSPOwnExtCorruptedException](./esentspownextcorruptedexception-class.md)