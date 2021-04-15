---
description: 'Saiba mais sobre: classe EsentObsoleteException'
title: Classe EsentObsoleteException
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104506322"
---
# <a name="esentobsoleteexception-class"></a>Classe EsentObsoleteException

Classe base para exceções obsoletas.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentObsoleteException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentObsoleteException](./esentobsoleteexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentObsoleteException  
            [Microsoft. ISAM. ESENT. Interop. EsentAccessDeniedException](./esentaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadBackupDatabaseSizeException](./esentbadbackupdatabasesizeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadBookmarkException](./esentbadbookmarkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadDbSignatureException](./esentbaddbsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadPatchPageException](./esentbadpatchpageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentBadSLVSignatureException](./esentbadslvsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotAddFixedVarColumnToDerivedTableException](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCannotNestDistributedTransactionsException](./esentcannotnestdistributedtransactionsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnIndexedException](./esentcolumnindexedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnInRelationshipException](./esentcolumninrelationshipexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentColumnLongException](./esentcolumnlongexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentContainerNotEmptyException](./esentcontainernotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentCurrencyStackOutOfMemoryException](./esentcurrencystackoutofmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException](./esentdatabase200formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase400FormatException](./esentdatabase400formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase500FormatException](./esentdatabase500formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseIdInUseException](./esentdatabaseidinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabasePatchFileMismatchException](./esentdatabasepatchfilemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabasesNotFromSameSnapshotException](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseStreamingFileMismatchException](./esentdatabasestreamingfilemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabaseUnavailableException](./esentdatabaseunavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDataHasChangedException](./esentdatahaschangedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDistributedTransactionAlreadyPreparedToCommitException](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDistributedTransactionNotYetPreparedToCommitException](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDTCCallbackUnexpectedErrorException](./esentdtccallbackunexpectederrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDTCMissingCallbackException](./esentdtcmissingcallbackexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDTCMissingCallbackOnRecoveryException](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileCloseException](./esentfilecloseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileIOAbortException](./esentfileioabortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileIOFailException](./esentfileiofailexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileIORetryException](./esentfileioretryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentFileIOSparseException](./esentfileiosparseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexCantBuildException](./esentindexcantbuildexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesTooManyColumnsException](./esentindextuplestoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidCountryException](./esentinvalidcountryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidFilenameException](./esentinvalidfilenameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidLogDirectoryException](./esentinvalidlogdirectoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidLoggedOperationException](./esentinvalidloggedoperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidObjectException](./esentinvalidobjectexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidOnSortException](./esentinvalidonsortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentInvalidSystemPathException](./esentinvalidsystempathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentKeyBoundaryException](./esentkeyboundaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentKeyTooBigException](./esentkeytoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLanguageNotSupportedException](./esentlanguagenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLinkNotSupportedException](./esentlinknotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogBufferTooSmallException](./esentlogbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMissingPatchPageException](./esentmissingpatchpageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustDisableLoggingForDbUpgradeException](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentNotInDistributedTransactionException](./esentnotindistributedtransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentObjectDuplicateException](./esentobjectduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPageBoundaryException](./esentpageboundaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentPatchFileMissingException](./esentpatchfilemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRfsFailureException](./esentrfsfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRfsNotArmedException](./esentrfsnotarmedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentRollbackRequiredException](./esentrollbackrequiredexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVBufferTooSmallException](./esentslvbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVColumnCannotDeleteException](./esentslvcolumncannotdeleteexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVColumnDefaultValueNotAllowedException](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVCorruptedException](./esentslvcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVDatabaseMissingException](./esentslvdatabasemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVEAListCorruptException](./esentslvealistcorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVEAListTooBigException](./esentslvealisttoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVEAListZeroAllocationException](./esentslvealistzeroallocationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileAccessDeniedException](./esentslvfileaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileInUseException](./esentslvfileinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileInvalidPathException](./esentslvfileinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileIOException](./esentslvfileioexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileNotFoundException](./esentslvfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileStaleException](./esentslvfilestaleexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVFileUnknownException](./esentslvfileunknownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVHeaderBadChecksumException](./esentslvheaderbadchecksumexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVHeaderCorruptedException](./esentslvheadercorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVInvalidPathException](./esentslvinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVOwnerMapAlreadyExistsException](./esentslvownermapalreadyexistsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVOwnerMapCorruptedException](./esentslvownermapcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVOwnerMapPageNotFoundException](./esentslvownermappagenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotCommittedException](./esentslvpagesnotcommittedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotDeletedException](./esentslvpagesnotdeletedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotFreeException](./esentslvpagesnotfreeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotReservedException](./esentslvpagesnotreservedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVProviderNotLoadedException](./esentslvprovidernotloadedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVProviderVersionMismatchException](./esentslvproviderversionmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVReadVerifyFailureException](./esentslvreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVRootNotSpecifiedException](./esentslvrootnotspecifiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVRootPathInvalidException](./esentslvrootpathinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVRootStillOpenException](./esentslvrootstillopenexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVSpaceCorruptedException](./esentslvspacecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVSpaceWriteConflictException](./esentslvspacewriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileAlreadyExistsException](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileFullException](./esentslvstreamingfilefullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileInUseException](./esentslvstreamingfileinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileMissingException](./esentslvstreamingfilemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileNotCreatedException](./esentslvstreamingfilenotcreatedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileReadOnlyException](./esentslvstreamingfilereadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSoftRecoveryOnSnapshotException](./esentsoftrecoveryonsnapshotexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCacheOutOfMemoryException](./esentspavailextcacheoutofmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCacheOutOfSyncException](./esentspavailextcacheoutofsyncexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentSQLLinkNotSupportedException](./esentsqllinknotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentStreamingDataNotLoggedException](./esentstreamingdatanotloggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTaggedNotNULLException](./esenttaggednotnullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTempFileOpenErrorException](./esenttempfileopenerrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManyOpenDatabasesException](./esenttoomanyopendatabasesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentTooManySplitsException](./esenttoomanysplitsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentUnicodeTranslationBufferTooSmallException](./esentunicodetranslationbuffertoosmallexception-class.md)