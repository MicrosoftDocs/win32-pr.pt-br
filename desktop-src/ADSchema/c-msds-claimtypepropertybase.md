---
title: Classe ms-DS-Claim-Type-Property-Base
description: Uma classe abstrata que define a classe base para classes de propriedade de recurso ou tipo de declaração.
ms.assetid: 85ec891b-0fdd-4b65-bc4d-6d0d2ca4e85d
ms.tgt_platform: multiple
keywords:
- Esquema do AD da classe ms-DS-Claim-Type-Property-Base
- Esquema do AD da classe msDS-ClaimTypePropertyBase
topic_type:
- apiref
api_name:
- ms-DS-Claim-Type-Property-Base
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe39dcbd29f3cdf60421ebb7fe31436ca8d457313433c6d6fcf7ce9411007825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422781"
---
# <a name="ms-ds-claim-type-property-base-class"></a>Classe ms-DS-Claim-Type-Property-Base

Uma classe abstrata que define a classe base para classes de propriedade de recurso ou tipo de declaração.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-Claim-Type-Property-Base       |
| Ldap-Display-Name | msDS-ClaimTypePropertyBase           |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Schema-Id-Guid    | b8442f58-c490-4487-8a9d-d80b883271ad |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.269                                                                       |
| Valor ocultado padrão        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                              |
| Possíveis superiores          | \-                                                                                           |
| Classes Auxiliares           | \-                                                                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; EA)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/>    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/>    |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/>    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**Common-Name**](a-cn.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/>    |
| [**Assinatura DSA**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/>    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**habilitado**](a-enabled.md)                                                                 | Falso     | **ms-DS-Claim-Type-Property-Base** |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**Sinalizadores**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>    |
| [**Entrada de entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/>    |
| [**Tipo de instância**](a-instancetype.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/>    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**Is-Recycled**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**Último pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Claim-Possible-Values**](a-msds-claimpossiblevalues.md)                            | Falso     | **ms-DS-Claim-Type-Property-Base** |
| [**ms-DS-Claim-Shares-Possible-Values-With**](a-msds-claimsharespossiblevalueswith.md)      | Falso     | **ms-DS-Claim-Type-Property-Base** |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/>    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/>    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/>    |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>    |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>    |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>    |
| [**Objeto-categoria**](a-objectcategory.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/>    |
| [**Classe de objeto**](a-objectclass.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/>    |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/>    |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**Endereços proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/>    |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/>    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/>    |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/>    |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/>    |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/>    |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>    |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/>    |
| [**Sub-refs**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/>    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>    |
| [**Sinalizadores de sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**USN alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**Criado por USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/>    |
| [**UsN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/>    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/>    |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/>    |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/>    |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/>    |
| [**Quando alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/>    |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/>    |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/>    |



 

 





