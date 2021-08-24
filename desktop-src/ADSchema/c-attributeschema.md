---
title: Attribute-Schema classe
description: Define um objeto de atributo no esquema.
ms.assetid: 2338d0ca-b090-4c76-be39-3f54ecb9932d
ms.tgt_platform: multiple
keywords:
- Attribute-Schema classe AD Schema
- Esquema do AD da classe attributeSchema
topic_type:
- apiref
api_name:
- Attribute-Schema
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a75225aa034503a2f08beb827f00cb44ccb656b387a1edb601b7ea430f05c0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703886"
---
# <a name="attribute-schema-class"></a>Attribute-Schema classe

Define um objeto de atributo no esquema.



| Entrada | Valor |
|-------------------|-----------------------------------------------|
| CN                | Attribute-Schema                              |
| Ldap-Display-Name | attributeSchema                               |
| Privilégio de atualização  | Esse valor é definido pelo administrador do esquema |
| Frequência de atualização  | \-                                            |
| Schema-Id-Guid    | bf967a80-0de6-11d0-a285-00aa003049e2          |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor ocultado padrão        | 1                                      |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Possíveis superiores          | [**Dmd**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| Descritor de segurança NT      | O:BAG:BAD:S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-2000-server-attributes"></a>Windows atributos de servidor 2000

Essa classe contém os seguintes atributos para Windows 2000 Server:



| Atributo                                                                     | Obrigatório | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                         | Verdadeiro      | **Esquema de atributo**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | Falso     | **Esquema de atributo**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                 | Verdadeiro      | **Esquema de atributo**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | Falso     | **Esquema de atributo**                                 |
| [**Common-Name**](a-cn.md)                                                   | Verdadeiro      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DSA-assinatura**](a-dsasignature.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Caracteres estendidos-permitidos**](a-extendedcharsallowed.md)                      | Falso     | **Atributo-esquema**                                 |
| [**Nome da extensão**](a-extensionname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Flags**](a-flags.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É-extinto**](a-isdefunct.md)                                             | Falso     | **Atributo-esquema**                                 |
| [**É excluído**](a-isdeleted.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-efêmero**](a-isephemeral.md)                                         | Falso     | **Atributo-esquema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É membro-do-conjunto de atributos parciais**](a-ismemberofpartialattributeset.md) | Falso     | **Atributo-esquema**                                 |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É de valor único**](a-issinglevalued.md)                                  | Verdadeiro      | **Atributo-esquema**                                 |
| [**Último-pai conhecido**](a-lastknownparent.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Verdadeiro      | **Atributo-esquema**                                 |
| [**ID do link**](a-linkid.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Mestre por**](a-masteredby.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                      | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objeto-categoria**](a-objectcategory.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                         | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**GUID do objeto**](a-objectguid.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**OM-objeto-classe**](a-omobjectclass.md)                                    | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de OM**](a-omsyntax.md)                                               | Verdadeiro      | **Atributo-esquema**                                 |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo-menor**](a-rangelower.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**Intervalo-superior**](a-rangeupper.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**RDN**](a-name.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Relatórios**](a-directreports.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Representantes-de**](a-repsfrom.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-to**](a-repsto.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Esquema-sinalizadores-ex**](a-schemaflagsex.md)                                    | Falso     | **Atributo-esquema**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Verdadeiro      | **Atributo-esquema**                                 |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Pesquisar-sinalizadores**](a-searchflags.md)                                         | Falso     | **Atributo-esquema**                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-referências**](a-subrefs.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**USN-alterado**](a-usnchanged.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado por USN**](a-usncreated.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**UsN-Intersite**](a-usnintersite.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Source**](a-usnsource.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Wbem-Path**](a-wbempath.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos conhecidos**](a-wellknownobjects.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando alterado**](a-whenchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando criado**](a-whencreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home Page**](a-wwwhomepage.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Page-Other**](a-url.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor ocultado padrão        | 1                                      |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Possíveis superiores          | [**Dmd**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| Descritor de segurança NT      | O:BAG:BAD:S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2003-attributes"></a>Windows Atributos do Server 2003

Essa classe contém os seguintes atributos para Windows Server 2003:



| Atributo                                                                     | Obrigatório | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                         | Verdadeiro      | **Esquema de atributo**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | Falso     | **Esquema de atributo**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                 | Verdadeiro      | **Esquema de atributo**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | Falso     | **Atributo-esquema**                                 |
| [**Nome comum**](a-cn.md)                                                   | Verdadeiro      | **Atributo-** [ **parte superior** do esquema](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DSA-assinatura**](a-dsasignature.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Caracteres estendidos-permitidos**](a-extendedcharsallowed.md)                      | Falso     | **Atributo-esquema**                                 |
| [**Nome da extensão**](a-extensionname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Flags**](a-flags.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É-extinto**](a-isdefunct.md)                                             | Falso     | **Atributo-esquema**                                 |
| [**É excluído**](a-isdeleted.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-efêmero**](a-isephemeral.md)                                         | Falso     | **Atributo-esquema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É membro-do-conjunto de atributos parciais**](a-ismemberofpartialattributeset.md) | Falso     | **Atributo-esquema**                                 |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É de valor único**](a-issinglevalued.md)                                  | Verdadeiro      | **Atributo-esquema**                                 |
| [**Último-pai conhecido**](a-lastknownparent.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Verdadeiro      | **Atributo-esquema**                                 |
| [**ID do link**](a-linkid.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Mestre por**](a-masteredby.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-inicial**](a-msds-intid.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Schema-Extensions**](a-msds-schema-extensions.md)                   | Falso     | **Atributo-esquema**                                 |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                      | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objeto-categoria**](a-objectcategory.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                         | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**GUID do objeto**](a-objectguid.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**OM-objeto-classe**](a-omobjectclass.md)                                    | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de OM**](a-omsyntax.md)                                               | Verdadeiro      | **Atributo-esquema**                                 |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo-menor**](a-rangelower.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**Intervalo-superior**](a-rangeupper.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**RDN**](a-name.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Relatórios**](a-directreports.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Representantes-de**](a-repsfrom.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-to**](a-repsto.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Esquema-sinalizadores-ex**](a-schemaflagsex.md)                                    | Falso     | **Atributo-esquema**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Verdadeiro      | **Atributo-esquema**                                 |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Pesquisar-sinalizadores**](a-searchflags.md)                                         | Falso     | **Atributo-esquema**                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-referências**](a-subrefs.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                           | Falso     | **Atributo-esquema**                                 |
| [**USN-alterado**](a-usnchanged.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado pelo USN**](a-usncreated.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-entre sites**](a-usnintersite.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-fonte**](a-usnsource.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WBEM-caminho**](a-wbempath.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando-alterado**](a-whenchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando-criado**](a-whencreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-página-outro**](a-url.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Categoria de objeto-padrão     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Padrão-ocultando valor        | 1                                      |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Superiores possíveis          | [**DMD**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="adam-attributes"></a>Atributos do ADAM

Essa classe contém os seguintes atributos para ADAM:



| Atributo                                                                     | Obrigatório | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                         | Verdadeiro      | **Atributo-esquema**                                 |
| [**Atributo-Security-GUID**](a-attributesecurityguid.md)                    | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                 | Verdadeiro      | **Atributo-esquema**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição de classe**](a-classdisplayname.md)                              | Falso     | **Atributo-esquema**                                 |
| [**Nome comum**](a-cn.md)                                                   | Verdadeiro      | **Atributo-** [ **parte superior** do esquema](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DSA-assinatura**](a-dsasignature.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Caracteres estendidos-permitidos**](a-extendedcharsallowed.md)                      | Falso     | **Atributo-esquema**                                 |
| [**De entrada**](a-fromentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Defunct**](a-isdefunct.md)                                             | Falso     | **Esquema de atributo**                                 |
| [**Is-Deleted**](a-isdeleted.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É efêmero**](a-isephemeral.md)                                         | Falso     | **Esquema de atributo**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Member-of-Partial-Attribute-Set**](a-ismemberofpartialattributeset.md) | Falso     | **Esquema de atributo**                                 |
| [**Tem valor único**](a-issinglevalued.md)                                  | Verdadeiro      | **Esquema de atributo**                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Verdadeiro      | **Esquema de atributo**                                 |
| [**ID do link**](a-linkid.md)                                                   | Falso     | **Esquema de atributo**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Mastered-By**](a-masteredby.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-ds-Schema-Extensions**](a-msds-schema-extensions.md)                   | Falso     | **Esquema de atributo**                                 |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                      | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Categoria de objeto**](a-objectcategory.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                         | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Guid de objeto**](a-objectguid.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe OM-Object**](a-omobjectclass.md)                                    | Falso     | **Esquema de atributo**                                 |
| [**Sintaxe do OM**](a-omsyntax.md)                                               | Verdadeiro      | **Esquema de atributo**                                 |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis inferiores**](a-possibleinferiors.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços proxy**](a-proxyaddresses.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo menor**](a-rangelower.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**Intervalo superior**](a-rangeupper.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**Rdn**](a-name.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-From**](a-repsfrom.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-To**](a-repsto.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Schema-Flags-Ex**](a-schemaflagsex.md)                                    | Falso     | **Esquema de atributo**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Verdadeiro      | **Esquema de atributo**                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de pesquisa**](a-searchflags.md)                                         | Falso     | **Esquema de atributo**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-refs**](a-subrefs.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de sistema**](a-systemflags.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**USN alterado**](a-usnchanged.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado por USN**](a-usncreated.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**UsN-Intersite**](a-usnintersite.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-fonte**](a-usnsource.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WBEM-caminho**](a-wbempath.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando-alterado**](a-whenchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando-criado**](a-whencreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-página-outro**](a-url.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Categoria de objeto-padrão     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Padrão-ocultando valor        | 1                                      |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Superiores possíveis          | [**DMD**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos do Server 2003 R2

essa classe contém os seguintes atributos para o Windows Server 2003 R2:



| Atributo                                                                     | Obrigatório | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                         | Verdadeiro      | **Atributo-esquema**                                 |
| [**Atributo-Security-GUID**](a-attributesecurityguid.md)                    | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                 | Verdadeiro      | **Atributo-esquema**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição de classe**](a-classdisplayname.md)                              | Falso     | **Atributo-esquema**                                 |
| [**Nome comum**](a-cn.md)                                                   | Verdadeiro      | **Atributo-** [ **parte superior** do esquema](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DSA-assinatura**](a-dsasignature.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Caracteres estendidos-permitidos**](a-extendedcharsallowed.md)                      | Falso     | **Atributo-esquema**                                 |
| [**Nome da extensão**](a-extensionname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Flags**](a-flags.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É-extinto**](a-isdefunct.md)                                             | Falso     | **Atributo-esquema**                                 |
| [**É excluído**](a-isdeleted.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-efêmero**](a-isephemeral.md)                                         | Falso     | **Atributo-esquema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É membro-do-conjunto de atributos parciais**](a-ismemberofpartialattributeset.md) | Falso     | **Atributo-esquema**                                 |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É de valor único**](a-issinglevalued.md)                                  | Verdadeiro      | **Atributo-esquema**                                 |
| [**Último-pai conhecido**](a-lastknownparent.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Verdadeiro      | **Atributo-esquema**                                 |
| [**ID do link**](a-linkid.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Mestre por**](a-masteredby.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-inicial**](a-msds-intid.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-ds-Schema-Extensions**](a-msds-schema-extensions.md)                   | Falso     | **Esquema de atributo**                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                      | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Categoria de objeto**](a-objectcategory.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                         | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Guid de objeto**](a-objectguid.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe OM-Object**](a-omobjectclass.md)                                    | Falso     | **Esquema de atributo**                                 |
| [**Sintaxe do OM**](a-omsyntax.md)                                               | Verdadeiro      | **Esquema de atributo**                                 |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis inferiores**](a-possibleinferiors.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços proxy**](a-proxyaddresses.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo menor**](a-rangelower.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**Intervalo superior**](a-rangeupper.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**Rdn**](a-name.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Relatórios**](a-directreports.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-From**](a-repsfrom.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-To**](a-repsto.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Schema-Flags-Ex**](a-schemaflagsex.md)                                    | Falso     | **Esquema de atributo**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Verdadeiro      | **Esquema de atributo**                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de pesquisa**](a-searchflags.md)                                         | Falso     | **Esquema de atributo**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-refs**](a-subrefs.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de sistema**](a-systemflags.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                           | Falso     | **Esquema de atributo**                                 |
| [**USN alterado**](a-usnchanged.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado por USN**](a-usncreated.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**UsN-Intersite**](a-usnintersite.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Source**](a-usnsource.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Wbem-Path**](a-wbempath.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos conhecidos**](a-wellknownobjects.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando alterado**](a-whenchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando criado**](a-whencreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home Page**](a-wwwhomepage.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Page-Other**](a-url.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Categoria de objeto-padrão     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Padrão-ocultando valor        | 1                                      |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Superiores possíveis          | [**DMD**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2008-attributes"></a>Windows Atributos do servidor 2008

essa classe contém os seguintes atributos para o Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de                                         |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                          | Verdadeiro      | **Atributo-esquema**                                 |
| [**Atributo-Security-GUID**](a-attributesecurityguid.md)                     | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                  | Verdadeiro      | **Atributo-esquema**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição de classe**](a-classdisplayname.md)                               | Falso     | **Atributo-esquema**                                 |
| [**Nome comum**](a-cn.md)                                                    | Verdadeiro      | **Atributo-** [ **parte superior** do esquema](c-top.md)<br/> |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DSA-assinatura**](a-dsasignature.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Caracteres estendidos-permitidos**](a-extendedcharsallowed.md)                       | Falso     | **Atributo-esquema**                                 |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Flags**](a-flags.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É-extinto**](a-isdefunct.md)                                              | Falso     | **Atributo-esquema**                                 |
| [**É excluído**](a-isdeleted.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-efêmero**](a-isephemeral.md)                                          | Falso     | **Atributo-esquema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É membro-do-conjunto de atributos parciais**](a-ismemberofpartialattributeset.md)  | Falso     | **Atributo-esquema**                                 |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É de valor único**](a-issinglevalued.md)                                   | Verdadeiro      | **Atributo-esquema**                                 |
| [**Último-pai conhecido**](a-lastknownparent.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                 | Verdadeiro      | **Atributo-esquema**                                 |
| [**ID do link**](a-linkid.md)                                                    | Falso     | **Atributo-esquema**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                    | Falso     | **Atributo-esquema**                                 |
| [**Mestre por**](a-masteredby.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-inicial**](a-msds-intid.md)                                            | Falso     | **Atributo-esquema**                                 |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-ds-Schema-Extensions**](a-msds-schema-extensions.md)                    | Falso     | **Esquema de atributo**                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                       | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Categoria de objeto**](a-objectcategory.md)                                    | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe OM-Object**](a-omobjectclass.md)                                     | Falso     | **Esquema de atributo**                                 |
| [**Sintaxe do OM**](a-omsyntax.md)                                                | Verdadeiro      | **Esquema de atributo**                                 |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis inferiores**](a-possibleinferiors.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços proxy**](a-proxyaddresses.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo menor**](a-rangelower.md)                                            | Falso     | **Esquema de atributo**                                 |
| [**Intervalo superior**](a-rangeupper.md)                                            | Falso     | **Esquema de atributo**                                 |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Relatórios**](a-directreports.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Schema-Flags-Ex**](a-schemaflagsex.md)                                     | Falso     | **Esquema de atributo**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                       | Verdadeiro      | **Esquema de atributo**                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de pesquisa**](a-searchflags.md)                                          | Falso     | **Esquema de atributo**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-refs**](a-subrefs.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de sistema**](a-systemflags.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                            | Falso     | **Esquema de atributo**                                 |
| [**USN alterado**](a-usnchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado por USN**](a-usncreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**UsN-Intersite**](a-usnintersite.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos conhecidos**](a-wellknownobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando alterado**](a-whenchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando criado**](a-whencreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home Page**](a-wwwhomepage.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor ocultado padrão        | 1                                      |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Possíveis superiores          | [**Dmd**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| Descritor de segurança NT      | O:BAG:BAD:S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos do Server 2008 R2

Essa classe contém os seguintes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                         |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                            | Verdadeiro      | **Esquema de atributo**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                       | Falso     | **Esquema de atributo**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                    | Verdadeiro      | **Esquema de atributo**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                                 | Falso     | **Esquema de atributo**                                 |
| [**Common-Name**](a-cn.md)                                                      | Verdadeiro      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Assinatura DSA**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Extended-Chars-Allowed**](a-extendedcharsallowed.md)                         | Falso     | **Esquema de atributo**                                 |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Entrada de entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Defunct**](a-isdefunct.md)                                                | Falso     | **Esquema de atributo**                                 |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É efêmero**](a-isephemeral.md)                                            | Falso     | **Esquema de atributo**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Member-of-Partial-Attribute-Set**](a-ismemberofpartialattributeset.md)    | Falso     | **Esquema de atributo**                                 |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tem valor único**](a-issinglevalued.md)                                     | Verdadeiro      | **Esquema de atributo**                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                   | Verdadeiro      | **Esquema de atributo**                                 |
| [**ID do link**](a-linkid.md)                                                      | Falso     | **Esquema de atributo**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MAPI-ID**](a-mapiid.md)                                                      | Falso     | **Esquema de atributo**                                 |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-inicial**](a-msds-intid.md)                                              | Falso     | **Atributo-esquema**                                 |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Schema-Extensions**](a-msds-schema-extensions.md)                      | Falso     | **Atributo-esquema**                                 |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objeto-categoria**](a-objectcategory.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                            | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**OM-objeto-classe**](a-omobjectclass.md)                                       | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de OM**](a-omsyntax.md)                                                  | Verdadeiro      | **Atributo-esquema**                                 |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo-menor**](a-rangelower.md)                                              | Falso     | **Atributo-esquema**                                 |
| [**Intervalo-superior**](a-rangeupper.md)                                              | Falso     | **Atributo-esquema**                                 |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Esquema-sinalizadores-ex**](a-schemaflagsex.md)                                       | Falso     | **Atributo-esquema**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                         | Verdadeiro      | **Atributo-esquema**                                 |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Pesquisar-sinalizadores**](a-searchflags.md)                                            | Falso     | **Atributo-esquema**                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                              | Falso     | **Atributo-esquema**                                 |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------|
| System-Only                 | Falso                                  |
| Object-Category             | 1                                      |
| Categoria de objeto-padrão     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Padrão-ocultando valor        | 1                                      |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/> |
| Subclasse de                 | [**Início**](c-top.md)<br/>        |
| Superiores possíveis          | [**DMD**](c-dmd.md)                   |
| Classes Auxiliares           | \-                                     |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                           |
| Descritor de segurança padrão | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                                         |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ID do atributo**](a-attributeid.md)                                                        | Verdadeiro      | **Atributo-esquema**                                 |
| [**Atributo-Security-GUID**](a-attributesecurityguid.md)                                   | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de atributo**](a-attributesyntax.md)                                                | Verdadeiro      | **Esquema de atributo**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                                             | Falso     | **Esquema de atributo**                                 |
| [**Common-Name**](a-cn.md)                                                                  | Verdadeiro      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Assinatura DSA**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Extended-Chars-Allowed**](a-extendedcharsallowed.md)                                     | Falso     | **Esquema de atributo**                                 |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Entrada de entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo de instância**](a-instancetype.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Defunct**](a-isdefunct.md)                                                            | Falso     | **Esquema de atributo**                                 |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**É efêmero**](a-isephemeral.md)                                                        | Falso     | **Esquema de atributo**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Member-of-Partial-Attribute-Set**](a-ismemberofpartialattributeset.md)                | Falso     | **Esquema de atributo**                                 |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Is-Recycled**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tem valor único**](a-issinglevalued.md)                                                 | Verdadeiro      | **Esquema de atributo**                                 |
| [**Último pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                               | Verdadeiro      | **Esquema de atributo**                                 |
| [**ID do link**](a-linkid.md)                                                                  | Falso     | **Esquema de atributo**                                 |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MAPI-ID**](a-mapiid.md)                                                                  | Falso     | **Esquema de atributo**                                 |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                                          | Falso     | **Esquema de atributo**                                 |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Schema-Extensions**](a-msds-schema-extensions.md)                                  | Falso     | **Atributo-esquema**                                 |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objeto-categoria**](a-objectcategory.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**Classe de objeto**](a-objectclass.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                      |
| [**GUID do objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**OM-objeto-classe**](a-omobjectclass.md)                                                   | Falso     | **Atributo-esquema**                                 |
| [**Sintaxe de OM**](a-omsyntax.md)                                                              | Verdadeiro      | **Atributo-esquema**                                 |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Intervalo-menor**](a-rangelower.md)                                                          | Falso     | **Atributo-esquema**                                 |
| [**Intervalo superior**](a-rangeupper.md)                                                          | Falso     | **Esquema de atributo**                                 |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Schema-Flags-Ex**](a-schemaflagsex.md)                                                   | Falso     | **Esquema de atributo**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                                     | Verdadeiro      | **Esquema de atributo**                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de pesquisa**](a-searchflags.md)                                                        | Falso     | **Esquema de atributo**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sub-refs**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Sinalizadores de sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Somente sistema**](a-systemonly.md)                                                          | Falso     | **Esquema de atributo**                                 |
| [**USN alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Criado por USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/>                      |
| [**UsN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                      |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**Quando criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Home Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                      |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                      |



 

 





