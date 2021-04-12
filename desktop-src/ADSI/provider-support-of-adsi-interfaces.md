---
title: Suporte do provedor de interfaces ADSI
description: A tabela a seguir lista uma breve descrição das interfaces com suporte dos provedores incluídos com ADSI para o Windows 2000 e o cliente DS.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Suporte do provedor do ADSI de interfaces ADSI
- ADSI ADSI, provedores de serviços, interfaces com suporte de cada provedor
- Suporte do provedor para IADsUser
- Suporte do provedor para IADsComputer
- Suporte do provedor para IADsComputerOperations
- Suporte do provedor para IADsDomain
- Suporte do provedor para IADsFileService
- Suporte do provedor para IADs
- Suporte do provedor para IADsClass
- Suporte do provedor para IADsproperty
- Suporte do provedor para IADsSyntax
- Suporte do provedor para IADsContainer
- Suporte do provedor para IADsNamespaces
- Suporte do provedor para IADsAccessControlEntry
- Suporte do provedor para IADsAccessControlList
- Suporte do provedor para IADsSecurityDescriptor
- Suporte do provedor para IADsObjectOptions
- Suporte do provedor para IADscollection
- Suporte do provedor para IADsMembers
- Suporte do provedor para IADsPathname
- Suporte do provedor para IADsPrintQueue
- Suporte do provedor para IADsPrintQueueOperations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12803929d96a61aac6603be2c528084c91693c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291787"
---
# <a name="provider-support-of-adsi-interfaces"></a>Suporte do provedor de interfaces ADSI

A tabela a seguir lista uma breve descrição das interfaces com suporte dos provedores incluídos com ADSI para o Windows 2000 e o cliente DS. Uma entrada marcada com "Sim" indica que pelo menos um objeto ADSI do provedor especificado dá suporte à interface associada. "Não" indica que nenhum objeto do provedor dá suporte à interface nesta versão. No futuro, as interfaces atualmente sem suporte podem se tornar compatíveis com os provedores fornecidos pelo sistema.

Para obter mais informações sobre detalhes de implementação específicos do provedor ADSI, consulte:

-   [Provedor LDAP ADSI](adsi-ldap-provider.md)
-   [Provedor ADSI de WinNT](adsi-winnt-provider.md)
-   [ROTEADOR ADSI](adsi-router.md)

Para obter mais informações sobre qual propriedade ou método tem suporte para cada interface, clique no nome de interface apropriado na primeira coluna da tabela.



| Nome da Interface                                                 | LDAP | WinNT |
|----------------------------------------------------------------|------|-------|
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Sim  | Sim   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Sim  | Não    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Sim  | Não    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | Não   | Não    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | Não   | Não    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | Não   | Não    |
| [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Sim  | Sim   |
| [**IADscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | Não   | Sim   |
| [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | Não   | Sim   |
| [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | Não   | Sim   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Sim  | Sim   |
| [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Sim  | Não    |
| [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | Não   | Sim   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | Não   | Não    |
| [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Sim  | Sim   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | Não   | Não    |
| [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | Não   | Sim   |
| [**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | Não   | Sim   |
| [**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | Não   | Sim   |
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Sim  | Sim   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | Não   | Não    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Sim  | Não    |
| [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Sim  | Não    |
| [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Sim  | Sim   |
| [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Sim  | Sim   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | Não   | Não    |
| [**IADso**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Sim  | Não    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Sim  | Não    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | Não   | Não    |
| [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Sim  | Sim   |
| [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Sim  | Não    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | Não   | Não    |
| [**IADsPathName**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Sim  | Sim   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | Não   | Não    |
| [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | Não   | Sim   |
| [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | Não   | Sim   |
| [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Sim  | Sim   |
| [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Sim  | Sim   |
| [**IADsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Sim  | Sim   |
| [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Sim  | Sim   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Sim  | Sim   |
| [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Sim  | Sim   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Sim  | Sim   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | Não   | Não    |
| [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | Não   | Sim   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Sim  | Não    |
| [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | Não   | Sim   |
| [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | Não   | Sim   |
| [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | Não   | Sim   |
| [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Sim  | Sim   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | Não   | Não    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | Não   | Não    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Sim  | Sim   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Sim  | Não    |
| [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Sim  | Não    |



 

## <a name="provider-support-for-iadsuser"></a>Suporte do provedor para IADsUser



| Propriedade                                                    | LDAP          | WinNT         |
|-------------------------------------------------------------|---------------|---------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | Com suporte     | Com suporte     |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | Com suporte     | Com suporte     |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Sem suporte   | Sem suporte |
| [**BadLoginCount**](iadsuser-property-methods.md)          | Com suporte     | Com suporte     |
| [**Inteiros**](iadsuser-property-methods.md)             | Com suporte     | Sem suporte   |
| [**Descrição**](iadsuser-property-methods.md)            | Com suporte     | Com suporte     |
| [**Divisão**](iadsuser-property-methods.md)               | Com suporte     | Sem suporte   |
| [**EmailAddress**](iadsuser-property-methods.md)           | Com suporte     | Sem suporte   |
| [**Funcionário**](iadsuser-property-methods.md)             | Com suporte     | Sem suporte   |
| [**FaxNumber**](iadsuser-property-methods.md)              | Com suporte     | Sem suporte   |
| [**FirstName**](iadsuser-property-methods.md)              | Com suporte     | Sem suporte   |
| [**FullName**](iadsuser-property-methods.md)               | Com suporte     | Com suporte     |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Sem suporte | Sem suporte   |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Sem suporte | Sem suporte   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Com suporte     | Com suporte     |
| [**Principal**](iadsuser-property-methods.md)               | Com suporte     | Sem suporte   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | Com suporte     | Com suporte     |
| [**Idiomas**](iadsuser-property-methods.md)              | Sem suporte | Sem suporte   |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | Com suporte     | Sem suporte   |
| [**LastLogin**](iadsuser-property-methods.md)              | Com suporte     | Com suporte     |
| [**LastLogoff**](iadsuser-property-methods.md)             | Com suporte     | Com suporte     |
| [**LastName**](iadsuser-property-methods.md)               | Com suporte     | Sem suporte   |
| [**LoginHours**](iadsuser-property-methods.md)             | Com suporte     | Com suporte     |
| [**LoginScript**](iadsuser-property-methods.md)            | Com suporte     | Com suporte     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | Com suporte     | Com suporte     |
| [**Manager**](iadsuser-property-methods.md)                | Com suporte     | Sem suporte   |
| [**MaxLogins**](iadsuser-property-methods.md)              | Sem suporte   | Sem suporte   |
| [**MaxStorage**](iadsuser-property-methods.md)             | Com suporte     | Com suporte     |
| [**NamePrefix**](iadsuser-property-methods.md)             | Com suporte     | Sem suporte   |
| [**NameSuffix**](iadsuser-property-methods.md)             | Com suporte     | Sem suporte   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | Com suporte     | Sem suporte   |
| [**Outro**](iadsuser-property-methods.md)              | Com suporte     | Sem suporte   |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Sem suporte   | Com suporte     |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | Com suporte     | Sem suporte   |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Sem suporte   | Com suporte     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | Com suporte     | Com suporte     |
| [**Imagem**](iadsuser-property-methods.md)                | Com suporte     | Sem suporte   |
| [**PostalAddresses**](iadsuser-property-methods.md)        | Com suporte     | Sem suporte   |
| [**PostalCodes**](iadsuser-property-methods.md)            | Com suporte     | Sem suporte   |
| [**Perfil**](iadsuser-property-methods.md)                | Com suporte     | Com suporte     |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Sem suporte   | Sem suporte   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Com suporte     | Sem suporte   |
| [**TelephoneHome**](iadsuser-property-methods.md)          | Com suporte     | Sem suporte   |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | Com suporte     | Sem suporte   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Com suporte     | Sem suporte   |
| [**TelephonePager**](iadsuser-property-methods.md)         | Com suporte     | Sem suporte   |
| [**Título**](iadsuser-property-methods.md)                  | Com suporte     | Sem suporte   |



 

## <a name="provider-support-for-iadscomputer"></a>Suporte do provedor para IADsComputer



| Propriedades                                     | LDAP                    | WinNT       |
|------------------------------------------------|-------------------------|-------------|
| [**Computadorid**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interface sem suporte | Sem suporte |
| [**Inteiros**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interface sem suporte | Sem suporte |
| [**Descrição**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interface sem suporte | Sem suporte |
| [**Divisão**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interface sem suporte | Com suporte   |
| [**Local**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interface sem suporte | Sem suporte |
| [**Tamanho da memória**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interface sem suporte | Sem suporte |
| [**Deprecia**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interface sem suporte | Sem suporte |
| [**Endereços de**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Interface sem suporte | Sem suporte |
| [**Operacional**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interface sem suporte | Com suporte   |
| [**OperatingSystemVersion**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Interface sem suporte | Com suporte   |
| [**Proprietário**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interface sem suporte | Com suporte   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interface sem suporte | Sem suporte |
| [**661**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Interface sem suporte | Com suporte   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Interface sem suporte | Com suporte   |
| [**Role**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interface sem suporte | Sem suporte |
| [**Site**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interface sem suporte | Sem suporte |
| [**StorageCapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interface sem suporte | Sem suporte |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Suporte do provedor para IADsComputerOperations



| Propriedade                                   | LDAP                    | WinNT           |
|--------------------------------------------|-------------------------|-----------------|
| [**Desligar**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | Interface sem suporte | Não implementado |
| [**Status**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | Interface sem suporte | Não implementado |



 

## <a name="provider-support-for-iadsdomain"></a>Suporte do provedor para IADsDomain



| Propriedade                                         | LDAP                    | WinNT           |
|--------------------------------------------------|-------------------------|-----------------|
| [**Grupo de trabalho**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | Interface sem suporte | Não implementado |
| [**MinPasswordLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | Interface sem suporte | Com suporte       |
| [**MinPasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Interface sem suporte | Com suporte       |
| [**MaxpasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Interface sem suporte | Com suporte       |
| [**MaxBadPasswordsAllowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | Interface sem suporte | Com suporte       |
| [**PasswordHistoryLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | Interface sem suporte | Com suporte       |
| [**Senhaattributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Interface sem suporte | Sem suporte     |
| [**AutoUnlockInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Interface sem suporte | Com suporte       |
| [**LockoutObservationInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | Interface sem suporte | Com suporte       |



 

## <a name="provider-support-for-iadsfileservice"></a>Suporte do provedor para IADsFileService



| Propriedade                                | LDAP                    | WinNT     |
|-----------------------------------------|-------------------------|-----------|
| [**Descrição**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | Interface sem suporte | Com suporte |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | Interface sem suporte | Com suporte |



 

## <a name="provider-support-for-iadsgroup"></a>Suporte do provedor para IADs



| Propriedade                         | LDAP      | WinNT     |
|----------------------------------|-----------|-----------|
| [**Descrição**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Com suporte | Com suporte |



 

## <a name="provider-support-for-iadsclass"></a>Suporte do provedor para IADsClass



| Propriedade                                   | LDAP               | WinNT           |
|--------------------------------------------|--------------------|-----------------|
| [**PrimaryInterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Com suporte          | Com suporte       |
| [**CLSID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Com suporte          | Com suporte       |
| [**OIDs**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Com suporte          | Com suporte       |
| [**Resumo**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Com suporte          | Com suporte       |
| [**Auxiliar**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Com suporte          | Com suporte       |
| [**Obrigatórioproperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Com suporte          | Com suporte       |
| [**OptionalProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Com suporte          | Com suporte       |
| [**Nome da nomenclatura**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Com suporte          | Não implementado |
| [**DerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Com suporte          | Sem suporte     |
| [**AuxDerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Com suporte          | Sem suporte     |
| [**PossibleSuperiors**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Com suporte          | Com suporte       |
| [**Contenção**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Com suporte para leitura | Com suporte       |
| [**Contêiner**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Com suporte para leitura | Com suporte       |
| [**Arquivodeajudaname**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Com suporte          | Com suporte       |
| [**HelpFileContext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Com suporte          | Com suporte       |
| Método                                     | LDAP               | WinNT           |
| [**Qualificadores**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | Não implementado    | Não implementado |



 

## <a name="provider-support-for-iadsproperty"></a>Suporte do provedor para IADsproperty



| Propriedade                            | LDAP      | WinNT     |
|-------------------------------------|-----------|-----------|
| [**OIDs**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Com suporte | Com suporte |
| [**Sintaxe**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Com suporte | Com suporte |
| [**MaxRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Com suporte | Com suporte |
| [**MinRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Com suporte | Com suporte |
| [**Múltiplos valores**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Com suporte | Com suporte |



 

## <a name="provider-support-for-iadssyntax"></a>Suporte do provedor para IADsSyntax



| Propriedade                              | LDAP      | WinNT     |
|---------------------------------------|-----------|-----------|
| [**OleAutoDataType**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Com suporte | Com suporte |



 

## <a name="provider-support-for-iadscontainer"></a>Suporte do provedor para IADsContainer



| Propriedade                        | LDAP            | WinNT           |
|---------------------------------|-----------------|-----------------|
| [**Contar**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Não implementado | Não implementado |
| [**Dicas**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Com suporte       | Não implementado |
| [**Filter**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Com suporte       | Com suporte       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Suporte do provedor para IADsNamespaces



| Propriedade                                   | LDAP      | WinNT     |
|--------------------------------------------|-----------|-----------|
| [**defaultcontainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Com suporte | Com suporte |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Suporte do provedor para IADsAccessControlEntry



| Propriedade                                              | LDAP      | WinNT       |
|-------------------------------------------------------|-----------|-------------|
| [**AccessMask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Com suporte | Sem suporte |
| [**AccessType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Com suporte | Sem suporte |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Com suporte | Sem suporte |
| [**Flags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Com suporte | Sem suporte |
| [**ObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Com suporte | Sem suporte |
| [**InheritedObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Com suporte | Sem suporte |
| [**Confiança**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Com suporte | Sem suporte |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Suporte do provedor para IADsAccessControlList



| Propriedade                                                       | LDAP      | WinNT       |
|----------------------------------------------------------------|-----------|-------------|
| [**AceCount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Com suporte | Sem suporte |
| [**AceRevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Com suporte | Sem suporte |
| Método                                                         | LDAP      | WinNT       |
| [**AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Com suporte | Sem suporte |
| [**CopyAccessList**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Com suporte | Sem suporte |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Com suporte | Sem suporte |
| [**obter \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Com suporte | Sem suporte |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Suporte do provedor para IADsSecurityDescriptor



| Propriedade                                                                        | LDAP      | WinNT       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Control**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Com suporte | Sem suporte |
| [**DaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Com suporte | Sem suporte |
| [**DiscretionaryAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Com suporte | Sem suporte |
| [**Group**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Com suporte | Sem suporte |
| [**GroupDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Com suporte | Sem suporte |
| [**Proprietário**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Com suporte | Sem suporte |
| [**OwnerDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Com suporte | Sem suporte |
| [**SaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Com suporte | Sem suporte |
| [**SystemAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Com suporte | Sem suporte |
| Método                                                                          | LDAP      | WinNT       |
| [**CopySecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Com suporte | Sem suporte |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Suporte do provedor para IADsObjectOptions



| Método                                           | LDAP      | WinNT                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Com suporte | Interface sem suporte |
| [**SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Com suporte | Interface sem suporte |



 

## <a name="provider-support-for-iadscollection"></a>Suporte do provedor para IADscollection



| Método                                                | LDAP                    | WinNT       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Adicionar**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Interface sem suporte | Sem suporte |
| [**obter \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Interface sem suporte | Com suporte   |
| [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Interface sem suporte | Com suporte   |
| [**Remover**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Interface sem suporte | Com suporte   |



 

## <a name="provider-support-for-iadsmembers"></a>Suporte do provedor para IADsMembers



| Propriedade                                           | LDAP                                                      | WinNT       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Contar**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Com suporte para GroupCollection, mas não para UserCollection | Sem suporte |
| [**Filter**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Com suporte                                                 | Com suporte   |
| Método                                             | LDAP                                                      | WinNT       |
| [**obter \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Com suporte                                                 | Com suporte   |



 

## <a name="provider-support-for-iadspathname"></a>Suporte do provedor para IADsPathname



| Propriedade                                                    | LDAP      | WinNT       |
|-------------------------------------------------------------|-----------|-------------|
| [**Escapemode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Com suporte | Com suporte   |
| Método                                                      | LDAP      | WinNT       |
| [**Definir**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Com suporte | Com suporte   |
| [**Setdisplaytype**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Com suporte | Com suporte   |
| [**Recuperar**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Com suporte | Com suporte   |
| [**GetNumElements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Com suporte | Com suporte   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Com suporte | Com suporte   |
| [**Getescapeelement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Com suporte | Sem suporte |
| [**RemoveLeafElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Com suporte | Com suporte   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Com suporte | Com suporte   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Suporte do provedor para IADsPrintQueue



| Propriedade                                     | LDAP        | WinNT       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Com suporte   | Sem suporte |
| [**Deprecia**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Com suporte   | Com suporte.  |
| [**Tipo de dados**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Sem suporte | Com suporte   |
| [**Multiprocessador**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | Sem suporte | Com suporte   |
| [**Descrição**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Com suporte   | Com suporte   |
| [**Local**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Com suporte   | Com suporte   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Com suporte   | Com suporte   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Com suporte   | Com suporte   |
| [**DefaultJobPriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | Sem suporte | Com suporte   |
| [**Priority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Com suporte   | Com suporte   |
| [**BannerPage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Com suporte   | Com suporte   |
| [**Dispositivos de redispositivo**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Com suporte   | Com suporte   |
| [**Endereços de**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Sem suporte | Sem suporte |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Suporte do provedor para IADsPrintQueueOperations



| Propriedade                                                | LDAP      | WinNT      |
|---------------------------------------------------------|-----------|------------|
| [**Status**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Com suporte | Com suporte  |
| Método                                                  | LDAP      | WinNT      |
| [**Pausar**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Com suporte | Com suporte. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Com suporte | Com suporte  |
| [**Limpar**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Com suporte | Com suporte  |
| [**Retomar**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Com suporte | Com suporte  |



 

 

 




