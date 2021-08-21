---
title: Classe ms-net-ieee-8023-GroupPolicy
description: Essa classe representa um objeto de rede com fio 802.3 Política de Grupo objeto . Essa classe contém identificadores e dados de configuração relevantes para uma rede com fio 802.3.
ms.assetid: ca213f8b-99d4-48c9-8104-bb982f0c077a
ms.tgt_platform: multiple
keywords:
- Esquema AD da classe ms-net-ieee-8023-GroupPolicy
topic_type:
- apiref
api_name:
- ms-net-ieee-8023-GroupPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ed8c9299200f88cbb9098c07d62149104a8e5bee3c911ce4afef924299930a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680880"
---
# <a name="ms-net-ieee-8023-grouppolicy-class"></a>Classe ms-net-ieee-8023-GroupPolicy

Essa classe representa um objeto de rede com fio 802.3 Política de Grupo objeto . Essa classe contém identificadores e dados de configuração relevantes para uma rede com fio 802.3.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-net-ieee-8023-GroupPolicy         |
| Ldap-Display-Name | ms-net-ieee-8023-GroupPolicy         |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Schema-Id-Guid    | 99a03a6a-ab19-4446-9350-0cb878ed2d9b |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.252                                                                       |
| Valor ocultado padrão        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Parte superior**](c-top.md)<br/>                                                              |
| Possíveis superiores          | [**Computador de**](c-person.md)[**contêiner de**](c-container.md)[**pessoa**](c-computer.md)     |
| Classes Auxiliares           | \-                                                                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos do Server 2008

Essa classe contém os seguintes atributos para Windows Server 2008:



| Atributo                                                                          | Obrigatório | Derivado de                     |
|------------------------------------------------------------------------------------|-----------|----------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Atributos permitidos**](a-allowedattributes.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome canônico**](a-canonicalname.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Common-Name**](a-cn.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Descrição**](a-description.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome de exibição**](a-displayname.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Assinatura DSA**](a-dsasignature.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome da extensão**](a-extensionname.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sinalizadores**](a-flags.md)                                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**De entrada**](a-fromentry.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Tipo de instância**](a-instancetype.md)                                            | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**É excluído**](a-isdeleted.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Is-member-of-DL**](a-memberof.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Último-pai conhecido**](a-lastknownparent.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objetos gerenciados**](a-managedobjects.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Mestre por**](a-masteredby.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-net-IEEE-8023-GP-PolicyData**](a-ms-net-ieee-8023-gp-policydata.md)         | Falso     | **MS-net-IEEE-8023-GroupPolicy** |
| [**MS-net-IEEE-8023-GP-PolicyGUID**](a-ms-net-ieee-8023-gp-policyguid.md)         | Falso     | **MS-net-IEEE-8023-GroupPolicy** |
| [**MS-net-IEEE-8023-GP-PolicyReserved**](a-ms-net-ieee-8023-gp-policyreserved.md) | Falso     | **MS-net-IEEE-8023-GroupPolicy** |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                           | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**Obj-dist-Name**](a-distinguishedname.md)                                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objeto-categoria**](a-objectcategory.md)                                        | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**Classe de objeto**](a-objectclass.md)                                              | True      | [**Parte superior**](c-top.md)<br/>  |
| [**GUID do objeto**](a-objectguid.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Versão do objeto**](a-objectversion.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Endereços de proxy**](a-proxyaddresses.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Consulta-política-BL**](a-querypolicybl.md)                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**RDN**](a-name.md)                                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Relatórios**](a-directreports.md)                                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Reps-From**](a-repsfrom.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Reps-To**](a-repsto.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Revisão**](a-revision.md)                                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sub-refs**](a-subrefs.md)                                                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN alterado**](a-usnchanged.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Criado por USN**](a-usncreated.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**UsN-Intersite**](a-usnintersite.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-Source**](a-usnsource.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Wbem-Path**](a-wbempath.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Quando alterado**](a-whenchanged.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Quando criado**](a-whencreated.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**WWW-Home Page**](a-wwwhomepage.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**WWW-Page-Other**](a-url.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.252                                                                       |
| Valor ocultado padrão        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Parte superior**](c-top.md)<br/>                                                              |
| Possíveis superiores          | [**Computador de**](c-person.md)[**contêiner de**](c-container.md)[**pessoa**](c-computer.md)     |
| Classes Auxiliares           | \-                                                                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos do Server 2008 R2

Essa classe contém os seguintes atributos para Windows Server 2008 R2:



| Atributo                                                                          | Obrigatório | Derivado de                     |
|------------------------------------------------------------------------------------|-----------|----------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Atributos permitidos**](a-allowedattributes.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome canônico**](a-canonicalname.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Common-Name**](a-cn.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Descrição**](a-description.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome de exibição**](a-displayname.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Assinatura DSA**](a-dsasignature.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome da extensão**](a-extensionname.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sinalizadores**](a-flags.md)                                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Entrada de entrada**](a-fromentry.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Tipo de instância**](a-instancetype.md)                                            | True      | [**Parte superior**](c-top.md)<br/>  |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Is-Deleted**](a-isdeleted.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Is-Member-of-DL**](a-memberof.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Is-Recycled**](a-isrecycled.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Último pai conhecido**](a-lastknownparent.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objetos gerenciados**](a-managedobjects.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Mastered-By**](a-masteredby.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-net-ieee-8023-GP-PolicyData**](a-ms-net-ieee-8023-gp-policydata.md)         | Falso     | **ms-net-ieee-8023-GroupPolicy** |
| [**ms-net-ieee-8023-GP-PolicyGUID**](a-ms-net-ieee-8023-gp-policyguid.md)         | Falso     | **ms-net-ieee-8023-GroupPolicy** |
| [**ms-net-ieee-8023-GP-PolicyReserved**](a-ms-net-ieee-8023-gp-policyreserved.md) | Falso     | **ms-net-ieee-8023-GroupPolicy** |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                           | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Categoria de objeto**](a-objectcategory.md)                                        | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**Classe de objeto**](a-objectclass.md)                                              | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**Guid de objeto**](a-objectguid.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Versão do objeto**](a-objectversion.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Endereços proxy**](a-proxyaddresses.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Rdn**](a-name.md)                                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Relatórios**](a-directreports.md)                                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Reps-From**](a-repsfrom.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Reps-To**](a-repsto.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Revisão**](a-revision.md)                                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sub-refs**](a-subrefs.md)                                                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN alterado**](a-usnchanged.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Criado por USN**](a-usncreated.md)                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**UsN-Intersite**](a-usnintersite.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-Source**](a-usnsource.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Wbem-Path**](a-wbempath.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Quando alterado**](a-whenchanged.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Quando criado**](a-whencreated.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**WWW-Home Page**](a-wwwhomepage.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**WWW-Page-Other**](a-url.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.252                                                                       |
| Valor ocultado padrão        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Parte superior**](c-top.md)<br/>                                                              |
| Possíveis superiores          | [**Computador de**](c-person.md)[**contêiner de**](c-container.md)[**pessoa**](c-computer.md)     |
| Classes Auxiliares           | \-                                                                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                     |
|----------------------------------------------------------------------------------------------|-----------|----------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome comum**](a-cn.md)                                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**DSA-assinatura**](a-dsasignature.md)                                                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sinalizadores**](a-flags.md)                                                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**De entrada**](a-fromentry.md)                                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Tipo de instância**](a-instancetype.md)                                                      | True      | [**Parte superior**](c-top.md)<br/>  |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**É excluído**](a-isdeleted.md)                                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**É reciclado**](a-isrecycled.md)                                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Último-pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Mestre por**](a-masteredby.md)                                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**ms-net-ieee-8023-GP-PolicyData**](a-ms-net-ieee-8023-gp-policydata.md)                   | Falso     | **ms-net-ieee-8023-GroupPolicy** |
| [**ms-net-ieee-8023-GP-PolicyGUID**](a-ms-net-ieee-8023-gp-policyguid.md)                   | Falso     | **ms-net-ieee-8023-GroupPolicy** |
| [**ms-net-ieee-8023-GP-PolicyReserved**](a-ms-net-ieee-8023-gp-policyreserved.md)           | Falso     | **ms-net-ieee-8023-GroupPolicy** |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Parte superior**](c-top.md)<br/>  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Categoria de objeto**](a-objectcategory.md)                                                  | True      | [**Parte superior**](c-top.md)<br/>  |
| [**Classe de objeto**](a-objectclass.md)                                                        | True      | [**Parte superior**](c-top.md)<br/>  |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Endereços proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sub-refs**](a-subrefs.md)                                                                | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN alterado**](a-usnchanged.md)                                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Criado por USN**](a-usncreated.md)                                                          | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**UsN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Quando alterado**](a-whenchanged.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**Quando criado**](a-whencreated.md)                                                        | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**WWW-Home Page**](a-wwwhomepage.md)                                                       | Falso     | [**Parte superior**](c-top.md)<br/>  |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**Parte superior**](c-top.md)<br/>  |



 

 





