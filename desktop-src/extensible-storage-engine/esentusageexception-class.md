---
description: 'Saiba mais sobre: classe EsentUsageException'
title: Classe EsentUsageException
TOCTitle: EsentUsageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUsageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUsageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0319ae3d6185e3075931fb601ec789aba70dfd82
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837561"
---
# <a name="esentusageexception-class"></a>Classe EsentUsageException

Classe base para exceções de uso.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentUsageException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentUsageException _
    Inherits EsentApiException
'Usage
Dim instance As EsentUsageException
```

``` csharp
[SerializableAttribute]
public abstract class EsentUsageException : EsentApiException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentUsageException](./esentusageexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentUsageException  
            [Microsoft. ISAM. ESENT. Interop. EsentAfterInitializationException](./esentafterinitializationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentAlreadyInitializedException](./esentalreadyinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentAlreadyPreparedException](./esentalreadypreparedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBackupDirectoryNotEmptyException](./esentbackupdirectorynotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadColumnIdException](./esentbadcolumnidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadRestoreTargetInstanceException](./esentbadrestoretargetinstanceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCallbackNotResolvedException](./esentcallbacknotresolvedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotBeTaggedException](./esentcannotbetaggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotDeleteSystemTableException](./esentcannotdeletesystemtableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotDeleteTemplateTableException](./esentcannotdeletetemplatetableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotDeleteTempTableException](./esentcannotdeletetemptableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotDisableVersioningException](./esentcannotdisableversioningexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotIndexException](./esentcannotindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotMaterializeForwardOnlySortException](./esentcannotmaterializeforwardonlysortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotNestDDLException](./esentcannotnestddlexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotSeparateIntrinsicLVException](./esentcannotseparateintrinsiclvexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnCannotBeCompressedException](./esentcolumncannotbecompressedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnDoesNotFitException](./esentcolumndoesnotfitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnDuplicateException](./esentcolumnduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnInUseException](./esentcolumninuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnNoChunkException](./esentcolumnnochunkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnNotFoundException](./esentcolumnnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnNotUpdatableException](./esentcolumnnotupdatableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnRedundantException](./esentcolumnredundantexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnTooBigException](./esentcolumntoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseAlreadyRunningMaintenanceException](./esentdatabasealreadyrunningmaintenanceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseCorruptedNoRepairException](./esentdatabasecorruptednorepairexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseDuplicateException](./esentdatabaseduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseFileReadOnlyException](./esentdatabasefilereadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseInUseException](./esentdatabaseinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidIncrementalReseedException](./esentdatabaseinvalidincrementalreseedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidNameException](./esentdatabaseinvalidnameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidPagesException](./esentdatabaseinvalidpagesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidPathException](./esentdatabaseinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseLockedException](./esentdatabaselockedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseNotFoundException](./esentdatabasenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseSharingViolationException](./esentdatabasesharingviolationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseSignInUseException](./esentdatabasesigninuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDDLNotInheritableException](./esentddlnotinheritableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDefaultValueTooBigException](./esentdefaultvaluetoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDensityInvalidException](./esentdensityinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDisabledFunctionalityException](./esentdisabledfunctionalityexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentEntryPointNotFoundException](./esententrypointnotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentExclusiveTableLockRequiredException](./esentexclusivetablelockrequiredexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFeatureNotAvailableException](./esentfeaturenotavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileCompressedException](./esentfilecompressedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFilteredMoveNotSupportedException](./esentfilteredmovenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFixedDDLException](./esentfixedddlexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFixedInheritedDDLException](./esentfixedinheritedddlexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentForceDetachNotAllowedException](./esentforcedetachnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIllegalOperationException](./esentillegaloperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexDuplicateException](./esentindexduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexHasPrimaryException](./esentindexhasprimaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexInvalidDefException](./esentindexinvaliddefexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexMustStayException](./esentindexmuststayexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesCannotRetrieveFromIndexException](./esentindextuplescannotretrievefromindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesInvalidLimitsException](./esentindextuplesinvalidlimitsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesKeyTooSmallException](./esentindextupleskeytoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesNonUniqueOnlyException](./esentindextuplesnonuniqueonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesSecondaryIndexOnlyException](./esentindextuplessecondaryindexonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesTextBinaryColumnsOnlyException](./esentindextuplestextbinarycolumnsonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesVarSegMacNotAllowedException](./esentindextuplesvarsegmacnotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInstanceNameInUseException](./esentinstancenameinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInTransactionException](./esentintransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidBackupException](./esentinvalidbackupexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidBackupSequenceException](./esentinvalidbackupsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidBookmarkException](./esentinvalidbookmarkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidCodePageException](./esentinvalidcodepageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidColumnTypeException](./esentinvalidcolumntypeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidCreateIndexException](./esentinvalidcreateindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidDatabaseException](./esentinvaliddatabaseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidDatabaseIdException](./esentinvaliddatabaseidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidGrbitException](./esentinvalidgrbitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidIndexIdException](./esentinvalidindexidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidInstanceException](./esentinvalidinstanceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidLanguageIdException](./esentinvalidlanguageidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidLCMapStringFlagsException](./esentinvalidlcmapstringflagsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidNameException](./esentinvalidnameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidOperationException](./esentinvalidoperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidParameterException](./esentinvalidparameterexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidPathException](./esentinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidPlaceholderColumnException](./esentinvalidplaceholdercolumnexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidPrereadException](./esentinvalidprereadexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidSesidException](./esentinvalidsesidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidSettingsException](./esentinvalidsettingsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidTableIdException](./esentinvalidtableidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentKeyIsMadeException](./esentkeyismadeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentKeyNotMadeException](./esentkeynotmadeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogFileNotCopiedException](./esentlogfilenotcopiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogFilePathInUseException](./esentlogfilepathinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogFileSizeMismatchException](./esentlogfilesizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLoggingDisabledException](./esentloggingdisabledexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLSAlreadySetException](./esentlsalreadysetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLSCallbackNotSpecifiedException](./esentlscallbacknotspecifiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMultiValuedColumnMustBeTaggedException](./esentmultivaluedcolumnmustbetaggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMultiValuedIndexViolationException](./esentmultivaluedindexviolationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustBeSeparateLongValueException](./esentmustbeseparatelongvalueexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustRollbackException](./esentmustrollbackexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNoBackupDirectoryException](./esentnobackupdirectoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNoCurrentIndexException](./esentnocurrentindexexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNotInitializedException](./esentnotinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNotInTransactionException](./esentnotintransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNullInvalidException](./esentnullinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNullKeyDisallowedException](./esentnullkeydisallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOneDatabasePerSessionException](./esentonedatabasepersessionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOSSnapshotInvalidSequenceException](./esentossnapshotinvalidsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOSSnapshotInvalidSnapIdException](./esentossnapshotinvalidsnapidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPartiallyAttachedDBException](./esentpartiallyattacheddbexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPermissionDeniedException](./esentpermissiondeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentQueryNotSupportedException](./esentquerynotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordNoCopyException](./esentrecordnocopyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRecordPrimaryChangedException](./esentrecordprimarychangedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRestoreOfNonBackupDatabaseException](./esentrestoreofnonbackupdatabaseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRunningInMultiInstanceModeException](./esentrunninginmultiinstancemodeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRunningInOneInstanceModeException](./esentrunninginoneinstancemodeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSesidTableIdMismatchException](./esentsesidtableidmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSessionContextAlreadySetException](./esentsessioncontextalreadysetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSessionContextNotSetByThisThreadException](./esentsessioncontextnotsetbythisthreadexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSessionInUseException](./esentsessioninuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSessionSharingViolationException](./esentsessionsharingviolationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSessionWriteConflictException](./esentsessionwriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSoftRecoveryOnBackupDatabaseException](./esentsoftrecoveryonbackupdatabaseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSpaceHintsInvalidException](./esentspacehintsinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSystemParamsAlreadySetException](./esentsystemparamsalreadysetexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSystemPathInUseException](./esentsystempathinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTableLockedException](./esenttablelockedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTableNotEmptyException](./esenttablenotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTempPathInUseException](./esenttemppathinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyActiveUsersException](./esenttoomanyactiveusersexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyAttachedDatabasesException](./esenttoomanyattacheddatabasesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyColumnsException](./esenttoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyIndexesException](./esenttoomanyindexesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyKeysException](./esenttoomanykeysexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyOpenTablesAndCleanupTimedOutException](./esenttoomanyopentablesandcleanuptimedoutexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyTestInjectionsException](./esenttoomanytestinjectionsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTransReadOnlyException](./esenttransreadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTransTooDeepException](./esenttranstoodeepexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentUnicodeNormalizationNotSupportedException](./esentunicodenormalizationnotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentUpdateMustVersionException](./esentupdatemustversionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentUpdateNotPreparedException](./esentupdatenotpreparedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentVersionStoreOutOfMemoryAndCleanupTimedOutException](./esentversionstoreoutofmemoryandcleanuptimedoutexception-class.md)