---
title: Classe Top
description: A classe de nível superior da qual todas as classes são derivadas.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Esquema de classe superior do AD
- Esquema de classe superior do AD
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cd6a72dfba6a80687081d503864c88fd1c5122
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086573"
---
# <a name="top-class"></a>Classe Top

A classe de nível superior da qual todas as classes são derivadas.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Parte superior                                  |
| LDAP-Display-Name | top                                  |
| Privilégio de atualização  | Administrador de esquema                 |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | **Top**<br/>                                                                           |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md)                                                     |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Atributos do Windows 2000 Server

Essa classe contém os seguintes atributos para o Windows 2000 Server:



| Atributo                                                                 | Obrigatório | Derivado de |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                           | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                          | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)      | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                    | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md) | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                 | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                               | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                            | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                      | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                     | Falso     | **Top**      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                  | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                   | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)               | Falso     | **Top**      |
| [**Nome da extensão**](a-extensionname.md)                                 | Falso     | **Top**      |
| [**Flags**](a-flags.md)                                                  | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                         | Falso     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                   | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)             | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                         | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | **Top**      |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                        | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                            | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                               | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                       | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                            | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | **Top**      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                              | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                               | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                     | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                       | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                 | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)               | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md) | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                    | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                         | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                        | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                               | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                     | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                 | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                      | Falso     | **Top**      |
| [**Relatórios**](a-directreports.md)                                        | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                           | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                               | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                            | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                        | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                        | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)            | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                             | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                     | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                       | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                       | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                   | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                         | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                           | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                          | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                     | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                     | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                    | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                           | Falso     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | **Top**<br/>                                                                           |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md)                                                     |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Atributos do Windows Server 2003

Essa classe contém os seguintes atributos para o Windows Server 2003:



| Atributo                                                                   | Obrigatório | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | **Top**      |
| [**Flags**](a-flags.md)                                                    | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top**      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | **Top**      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top**      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top**      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top**      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top**      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                       | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Relatórios**](a-directreports.md)                                          | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | **Top**      |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)



| Entrada | Valor |
|-----------------------------|------------------------------------------|
| System-Only                 | True                                     |
| Object-Category             | 2                                        |
| Categoria de objeto-padrão     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Padrão-ocultando valor        | 1                                        |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>   |
| Subclasse de                 | **Top**<br/>                       |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md) |
| Classes Auxiliares           | \-                                       |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                             |
| Descritor de segurança padrão | D:S:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Atributos do ADAM

Essa classe contém os seguintes atributos para ADAM:



| Atributo                                                                   | Obrigatório | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | **Top**      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                       | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | **Top**<br/>                                                                           |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md)                                                     |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Atributos do Windows Server 2003 R2

Essa classe contém os seguintes atributos para o Windows Server 2003 R2:



| Atributo                                                                   | Obrigatório | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | **Top**      |
| [**Flags**](a-flags.md)                                                    | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top**      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | **Top**      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top**      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top**      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top**      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top**      |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                  | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top**      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                       | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Relatórios**](a-directreports.md)                                          | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | **Top**<br/>                                                                           |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md)                                                     |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Atributos do Windows Server 2008

Essa classe contém os seguintes atributos para o Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                               | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)           | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)      | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                                    | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                           | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | **Top**      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                       | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                        | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                    | Falso     | **Top**      |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | **Top**      |
| [**Flags**](a-flags.md)                                                       | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                              | Falso     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                     | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                        | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                              | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | **Top**      |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                             | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                                 | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                            | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | **Top**      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                    | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | **Top**      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | **Top**      |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | **Top**      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | **Top**      |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | **Top**      |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | **Top**      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                 | Falso     | **Top**      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | Falso     | **Top**      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                          | Falso     | **Top**      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)       | Falso     | **Top**      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | **Top**      |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | **Top**      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                            | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | **Top**      |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                           | Falso     | **Top**      |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                 | Falso     | **Top**      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | **Top**      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                 | Falso     | **Top**      |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                             | Falso     | **Top**      |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | **Top**      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | **Top**      |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                     | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | **Top**      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                   | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                                    | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                          | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                            | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                    | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)      | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                         | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                              | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                             | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                    | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                     | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                          | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                      | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                           | Falso     | **Top**      |
| [**Relatórios**](a-directreports.md)                                             | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                                | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                    | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                                 | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                             | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                             | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                 | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | **Top**      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                     | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                                  | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                          | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                            | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                            | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                     | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                        | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                              | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                                | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                               | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                          | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                          | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                         | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                                | Falso     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | **Top**<br/>                                                                           |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md)                                                     |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Atributos do Windows Server 2008 R2

Essa classe contém os seguintes atributos para o Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                 | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)             | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)        | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                                      | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                             | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | **Top**      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                         | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                          | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                      | Falso     | **Top**      |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | **Top**      |
| [**Flags**](a-flags.md)                                                         | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                                | Falso     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                       | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                          | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                                | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | **Top**      |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                               | Falso     | **Top**      |
| [**É reciclado**](a-isrecycled.md)                                              | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                                   | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                              | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | **Top**      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                      | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | **Top**      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | **Top**      |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | **Top**      |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | **Top**      |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | **Top**      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | **Top**      |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | **Top**      |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | **Top**      |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md) | Falso     | **Top**      |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)   | Falso     | **Top**      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | **Top**      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | **Top**      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                            | Falso     | **Top**      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)         | Falso     | **Top**      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | **Top**      |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | **Top**      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                              | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | **Top**      |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | **Top**      |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                             | Falso     | **Top**      |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                   | Falso     | **Top**      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | **Top**      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                   | Falso     | **Top**      |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                               | Falso     | **Top**      |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | **Top**      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | **Top**      |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                       | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | **Top**      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                     | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                                      | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                            | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                      | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)        | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                           | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                            | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | **Top**      |
| [**Relatórios**](a-directreports.md)                                               | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                                   | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | **Top**      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Padrão-ocultando valor        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | **Top**<br/>                                                                           |
| Superiores possíveis          | [**Perdido e encontrado**](c-lostandfound.md)                                                     |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Atributos do Windows Server 2012

Essa classe contém os seguintes atributos para o Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | **Top**      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | **Top**      |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | **Top**      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | **Top**      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | **Top**      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | **Top**      |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | **Top**      |
| [**Nome comum**](a-cn.md)                                                                  | Falso     | **Top**      |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | **Top**      |
| [**Descrição**](a-description.md)                                                         | Falso     | **Top**      |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | **Top**      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                     | Falso     | **Top**      |
| [**DSA-assinatura**](a-dsasignature.md)                                                      | Falso     | **Top**      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                  | Falso     | **Top**      |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | **Top**      |
| [**Flags**](a-flags.md)                                                                     | Falso     | **Top**      |
| [**De entrada**](a-fromentry.md)                                                            | Falso     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | **Top**      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                   | Falso     | **Top**      |
| [**Tipo de instância**](a-instancetype.md)                                                      | True      | **Top**      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | **Top**      |
| [**É excluído**](a-isdeleted.md)                                                            | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | **Top**      |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                           | Falso     | **Top**      |
| [**É reciclado**](a-isrecycled.md)                                                          | Falso     | **Top**      |
| [**Último-pai conhecido**](a-lastknownparent.md)                                               | Falso     | **Top**      |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | **Top**      |
| [**Mestre por**](a-masteredby.md)                                                          | Falso     | **Top**      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | **Top**      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                  | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | **Top**      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | **Top**      |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | **Top**      |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | **Top**      |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | **Top**      |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | **Top**      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | **Top**      |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | **Top**      |
| [**ms-DS-is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | **Top**      |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | **Top**      |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md)             | Falso     | **Top**      |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)               | Falso     | **Top**      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                               | Falso     | **Top**      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | **Top**      |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | **Top**      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                                        | Falso     | **Top**      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)                     | Falso     | **Top**      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | **Top**      |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | **Top**      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | **Top**      |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | **Top**      |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                                         | Falso     | **Top**      |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                               | Falso     | **Top**      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | **Top**      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                               | Falso     | **Top**      |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | **Top**      |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | **Top**      |
| [**ms-DS-TDO-egresso-BL**](a-msds-tdoegressbl.md)                                            | Falso     | **Top**      |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | **Top**      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | **Top**      |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                   | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | **Top**      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | **Top**      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                 | Falso     | **Top**      |
| [**Objeto-categoria**](a-objectcategory.md)                                                  | True      | **Top**      |
| [**Classe de objeto**](a-objectclass.md)                                                        | True      | **Top**      |
| [**GUID do objeto**](a-objectguid.md)                                                          | Falso     | **Top**      |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | **Top**      |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | **Top**      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                    | Falso     | **Top**      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                       | Falso     | **Top**      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                            | Falso     | **Top**      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                           | Falso     | **Top**      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                  | Falso     | **Top**      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                   | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                                        | Falso     | **Top**      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                    | Falso     | **Top**      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                                         | Falso     | **Top**      |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | **Top**      |
| [**Representantes-de**](a-repsfrom.md)                                                              | Falso     | **Top**      |
| [**Reps-to**](a-repsto.md)                                                                  | Falso     | **Top**      |
| [**Revisão**](a-revision.md)                                                               | Falso     | **Top**      |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                                           | Falso     | **Top**      |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                                           | Falso     | **Top**      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                               | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | **Top**      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                                   | Falso     | **Top**      |
| [**Sub-referências**](a-subrefs.md)                                                                | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | **Top**      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                                        | Falso     | **Top**      |
| [**USN-alterado**](a-usnchanged.md)                                                          | Falso     | **Top**      |
| [**Criado pelo USN**](a-usncreated.md)                                                          | Falso     | **Top**      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                                   | Falso     | **Top**      |
| [**USN-entre sites**](a-usnintersite.md)                                                      | Falso     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | **Top**      |
| [**USN-fonte**](a-usnsource.md)                                                            | Falso     | **Top**      |
| [**WBEM-caminho**](a-wbempath.md)                                                              | Falso     | **Top**      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                             | Falso     | **Top**      |
| [**Quando-alterado**](a-whenchanged.md)                                                        | Falso     | **Top**      |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | **Top**      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | **Top**      |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | **Top**      |



 

 





