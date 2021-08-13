---
title: classe MS-AuthZ-central-Access-Rule
description: Uma classe que define as regras de acesso central usadas para construir uma política de acesso central.
ms.assetid: 5831179c-c6ae-4980-b0f5-538faa190b60
ms.tgt_platform: multiple
keywords:
- Esquema de AD da classe MS-AuthZ-central-Access-Rule
- Esquema de AD da classe msAuthz-CentralAccessRule
topic_type:
- apiref
api_name:
- ms-Authz-Central-Access-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd7b0f7ca0d649d844de49ac61d86e22a4286d990907248c99112b797d81ef7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323706"
---
# <a name="ms-authz-central-access-rule-class"></a>classe MS-AuthZ-central-Access-Rule

Uma classe que define as regras de acesso central usadas para construir uma política de acesso central.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | MS-AuthZ-central-Access-Rule         |
| LDAP-Display-Name | msAuthz-CentralAccessRule            |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | 5b4a06dc-251c-4edb-8813-0bdd71327226 |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.4.2163                                                                      |
| Padrão-ocultando valor        | 0                                                                                            |
| RDN-ATT-ID                  | \-                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                              |
| Superiores possíveis          | [**MS-AuthZ-central-Access-Rules**](c-msauthz-centralaccessrules.md)                        |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; EA) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                     |
|----------------------------------------------------------------------------------------------|-----------|----------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/>  |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/>  |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/>  |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**Nome comum**](a-cn.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/>  |
| [**DSA-assinatura**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/>  |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**habilitado**](a-enabled.md)                                                                 | Falso     | **MS-AuthZ-central-Access-Rule** |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**Flags**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>  |
| [**De entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/>  |
| [**Tipo de instância**](a-instancetype.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/>  |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**É excluído**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**É reciclado**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**Último-pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**Mestre por**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**MS-AuthZ-efetiva-Security-Policy**](a-msauthz-effectivesecuritypolicy.md)              | Falso     | **MS-AuthZ-central-Access-Rule** |
| [**MS-AuthZ-Last-preeficaz-Security-Policy**](a-msauthz-lasteffectivesecuritypolicy.md)     | Falso     | **MS-AuthZ-central-Access-Rule** |
| [**MS-AuthZ-proposto-Security-Policy**](a-msauthz-proposedsecuritypolicy.md)                | Falso     | **MS-AuthZ-central-Access-Rule** |
| [**MS-AuthZ-Resource-Condition**](a-msauthz-resourcecondition.md)                           | Falso     | **MS-AuthZ-central-Access-Rule** |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/>  |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/>  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/>  |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>  |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>  |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>  |
| [**Categoria de objeto**](a-objectcategory.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/>  |
| [**Classe de objeto**](a-objectclass.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/>  |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/>  |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**Endereços proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/>  |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/>  |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/>  |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/>  |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/>  |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/>  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>  |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/>  |
| [**Sub-refs**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/>  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**USN alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**Criado por USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>  |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/>  |
| [**UsN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/>  |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/>  |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/>  |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/>  |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/>  |
| [**Quando-alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/>  |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/>  |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/>  |



 

 





