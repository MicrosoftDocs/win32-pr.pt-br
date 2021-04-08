---
title: classe de grupo
description: Armazena uma lista de nomes de usuário. Usado para aplicar entidades de segurança em recursos.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Esquema de classe de grupo do AD
- Esquema de classe de grupo do AD
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618adb97220f4cc1b1e4af7f42fd043c7bb1e6c5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086628"
---
# <a name="group-class"></a>classe de grupo

Armazena uma lista de nomes de usuário. Usado para aplicar entidades de segurança em recursos.



| Entrada | Valor |
|-------------------|------------------------------------------------|
| CN                | Grupo                                          |
| LDAP-Display-Name | group                                          |
| Privilégio de atualização  | Esse valor é definido pelo administrador de domínio. |
| Frequência de atualização  | \-                                             |
| Schema-ID-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Direitos estendidos](#windows-2000-server-extended-rights)
-   [Gravações validadas](#windows-2000-server-validated-writes)
-   [Conjuntos de propriedades](#windows-2000-server-property-sets)



| Entrada | Valor |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                   |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                                                              |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                     |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)a [**unidade organizacional**](c-organizationalunit.md)do DNS [**BuiltIn-contêiner de domínio**](c-builtindomain.md)[](c-container.md)                                       |
| Classes Auxiliares           | [**Segurança-principal**](c-securityprincipal.md) (sistema)[**email-destinatário**](c-mailrecipient.md) (sistema)                                                                                        |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                        |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Atributos do Windows 2000 Server

Essa classe contém os seguintes atributos para o Windows 2000 Server:



| Atributo                                                                    | Obrigatório | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nome da conta-histórico**](a-accountnamehistory.md)                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Conta de administrador**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                    |
| [**Descrição do administrador**](a-admindescription.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Administração – nome de exibição**](a-admindisplayname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Alt-segurança-identidades**](a-altsecurityidentities.md)                   | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome canônico**](a-canonicalname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Comentário**](a-info.md)                                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Nome comum**](a-cn.md)                                                  | True      | [**Início**](c-top.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/>         |
| [**Controle-acesso-direitos**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                    |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Descrição**](a-description.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Perfil de desktop**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                    |
| [**Nome de exibição**](a-displayname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DSA-assinatura**](a-dsasignature.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Email-endereços**](a-mail.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Nome da extensão**](a-extensionname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Flags**](a-flags.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                    |
| [**Grupo-Associação-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | True      | **Grupo**                                                                                    |
| [**Tipo de instância**](a-instancetype.md)                                      | True      | [**Início**](c-top.md)<br/>                                                              |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**É excluído**](a-isdeleted.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Último-pai conhecido**](a-lastknownparent.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Gerenciado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                    |
| [**Objetos gerenciados**](a-managedobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mestre por**](a-masteredby.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                    |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                    |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-categoria**](a-objectcategory.md)                                  | True      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                        | True      | [**Início**](c-top.md)<br/>                                                              |
| [**GUID do objeto**](a-objectguid.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-Sid**](a-objectsid.md)                                            | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Versão do objeto**](a-objectversion.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Operador-contagem**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                    |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Token de grupo primário**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                    |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços de proxy**](a-proxyaddresses.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Consulta-política-BL**](a-querypolicybl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Relatórios**](a-directreports.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Representantes-de**](a-repsfrom.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Revisão**](a-revision.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Eliminá**](a-rid.md)                                                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-tipo de conta**](a-samaccounttype.md)                                 | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Identificador de segurança**](a-securityidentifier.md)                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Histórico de SID**](a-sidhistory.md)                                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sub-referências**](a-subrefs.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)                | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Número de telefone**](a-telephonenumber.md)                                | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-groups-global-e-universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-groups-no-GC-aceitável**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Certificado de usuário**](a-usercert.md)                                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**USN-alterado**](a-usnchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criado pelo USN**](a-usncreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-entre sites**](a-usnintersite.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-fonte**](a-usnsource.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WBEM-caminho**](a-wbempath.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando-alterado**](a-whenchanged.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando-criado**](a-whencreated.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-página-outro**](a-url.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Direitos estendidos do Windows 2000 Server

Essa classe contém os seguintes direitos estendidos para o Windows 2000 Server:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Gravações validadas do Windows 2000 Server

Essa classe contém as seguintes gravações validadas para o Windows 2000 Server:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Conjuntos de propriedades do Windows 2000 Server

Essa classe contém os seguintes conjuntos de propriedades para o Windows 2000 Server:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Direitos estendidos](#windows-server-2003-extended-rights)
-   [Gravações validadas](#windows-server-2003-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2003-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md)do DNS [**BuiltIn-**](c-builtindomain.md)[**contêiner**](c-container.md)de domínio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**Segurança-principal**](c-securityprincipal.md) (sistema)[**email-destinatário**](c-mailrecipient.md) (sistema)                                                                                                                                                                                                     |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Atributos do Windows Server 2003

Essa classe contém os seguintes atributos para o Windows Server 2003:



| Atributo                                                                    | Obrigatório | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nome da conta-histórico**](a-accountnamehistory.md)                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Conta de administrador**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                    |
| [**Descrição do administrador**](a-admindescription.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Administração – nome de exibição**](a-admindisplayname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Alt-segurança-identidades**](a-altsecurityidentities.md)                   | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome canônico**](a-canonicalname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Comentário**](a-info.md)                                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Nome comum**](a-cn.md)                                                  | True      | [**Início**](c-top.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/>         |
| [**Controle-acesso-direitos**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                    |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Descrição**](a-description.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Perfil de desktop**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                    |
| [**Nome de exibição**](a-displayname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DSA-assinatura**](a-dsasignature.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Email-endereços**](a-mail.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Nome da extensão**](a-extensionname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Flags**](a-flags.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                    |
| [**Grupo-Associação-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | True      | **Grupo**                                                                                    |
| [**Tipo de instância**](a-instancetype.md)                                      | True      | [**Início**](c-top.md)<br/>                                                              |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**É excluído**](a-isdeleted.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Último-pai conhecido**](a-lastknownparent.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Gerenciado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                    |
| [**Objetos gerenciados**](a-managedobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mestre por**](a-masteredby.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                    |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Grupo**                                                                                    |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-não-membros**](a-msds-nonmembers.md)                               | Falso     | **Grupo**                                                                                    |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                    |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-categoria**](a-objectcategory.md)                                  | True      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                        | True      | [**Início**](c-top.md)<br/>                                                              |
| [**GUID do objeto**](a-objectguid.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-Sid**](a-objectsid.md)                                            | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Versão do objeto**](a-objectversion.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Operador-contagem**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                    |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Token de grupo primário**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                    |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços de proxy**](a-proxyaddresses.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Consulta-política-BL**](a-querypolicybl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Relatórios**](a-directreports.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Representantes-de**](a-repsfrom.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Revisão**](a-revision.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Eliminá**](a-rid.md)                                                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**SAM-tipo de conta**](a-samaccounttype.md)                                 | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**secretário**](a-secretary.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Identificador de segurança**](a-securityidentifier.md)                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Histórico de SID**](a-sidhistory.md)                                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sub-referências**](a-subrefs.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)                | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Número de telefone**](a-telephonenumber.md)                                | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-groups-global-e-universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-groups-no-GC-aceitável**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Certificado de usuário**](a-usercert.md)                                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |
| [**USN-alterado**](a-usnchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criado pelo USN**](a-usncreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-entre sites**](a-usnintersite.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-fonte**](a-usnsource.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WBEM-caminho**](a-wbempath.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando-alterado**](a-whenchanged.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando-criado**](a-whencreated.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-página-outro**](a-url.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Direitos estendidos do Windows Server 2003

Essa classe contém os seguintes direitos estendidos para o Windows Server 2003:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Gravações validadas do Windows Server 2003

Essa classe contém as seguintes gravações validadas para o Windows Server 2003:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Conjuntos de propriedades do Windows Server 2003

Essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2003:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)
-   [Gravações validadas](#adam-validated-writes)
-   [Conjuntos de propriedades](#adam-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Categoria de objeto-padrão     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Padrão-ocultando valor        | 0                                                                                                                    |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                               |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                      |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**contêiner**](c-container.md) da [**unidade organizacional**](c-organizationalunit.md)do DNS |
| Classes Auxiliares           | [**Segurança-principal**](c-securityprincipal.md) (sistema)                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                         |
| Descritor de segurança padrão | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Atributos do ADAM

Essa classe contém os seguintes atributos para ADAM:



| Atributo                                                                   | Obrigatório | Derivado de                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome comum**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Perfil de desktop**](a-desktopprofile.md)                                 | Falso     | **Grupo**                                                                                    |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Tipo de grupo**](a-grouptype.md)                                           | True      | **Grupo**                                                                                    |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | [**Início**](c-top.md)<br/>                                                              |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                  | Falso     | **Grupo**                                                                                    |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | [**Início**](c-top.md)<br/>                                                              |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-Sid**](a-objectsid.md)                                           | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Token de grupo primário**](a-primarygrouptoken.md)                          | Falso     | **Grupo**                                                                                    |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)               | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Grupos de tokens**](a-tokengroups.md)                                       | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Gravações validadas pelo ADAM

Essa classe contém as seguintes gravações validadas para ADAM:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Conjuntos de propriedades do ADAM

Essa classe contém os seguintes conjuntos de propriedades para ADAM:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Direitos estendidos](#windows-server-2003-r2-extended-rights)
-   [Gravações validadas](#windows-server-2003-r2-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2003-r2-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md)do DNS [**BuiltIn-**](c-builtindomain.md)[**contêiner**](c-container.md)de domínio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**email de caixa**](c-mailrecipient.md) de [**segurança de objeto**](c-securityprincipal.md) [**POSIX**](c-posixgroup.md)(sistema) – destinatário (sistema)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Atributos do Windows Server 2003 R2

Essa classe contém os seguintes atributos para o Windows Server 2003 R2:



| Atributo                                                                    | Obrigatório | Derivado de                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome da conta-histórico**](a-accountnamehistory.md)                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Conta de administrador**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Administração – nome de exibição**](a-admindisplayname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-segurança-identidades**](a-altsecurityidentities.md)                   | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comum**](a-cn.md)                                                  | True      | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> |
| [**Controle-acesso-direitos**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                                                          |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Descrição**](a-description.md)                                         | Falso     | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de desktop**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                                                          |
| [**Nome de exibição**](a-displayname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DSA-assinatura**](a-dsasignature.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Email-endereços**](a-mail.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Nome da extensão**](a-extensionname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Flags**](a-flags.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**Grupo-Associação-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                            | True      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                      | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É excluído**](a-isdeleted.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Último-pai conhecido**](a-lastknownparent.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Gerenciado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**Objetos gerenciados**](a-managedobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mestre por**](a-masteredby.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-não-membros**](a-msds-nonmembers.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                       | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-domínio**](a-mssfu30nisdomain.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member**](a-mssfu30posixmember.md)                        | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoria**](a-objectcategory.md)                                  | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                        | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**GUID do objeto**](a-objectguid.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-Sid**](a-objectsid.md)                                            | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Versão do objeto**](a-objectversion.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Operador-contagem**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo primário**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Endereços de proxy**](a-proxyaddresses.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Consulta-política-BL**](a-querypolicybl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Relatórios**](a-directreports.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Representantes-de**](a-repsfrom.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Revisão**](a-revision.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Eliminá**](a-rid.md)                                                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-tipo de conta**](a-samaccounttype.md)                                 | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**secretário**](a-secretary.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de segurança**](a-securityidentifier.md)                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Histórico de SID**](a-sidhistory.md)                                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sub-referências**](a-subrefs.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)                | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sinalizadores do sistema**](a-systemflags.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Número de telefone**](a-telephonenumber.md)                                | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-global-e-universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-no-GC-aceitável**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuário**](a-usercert.md)                                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Usuário-senha**](a-userpassword.md)                                      | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-alterado**](a-usnchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Criado pelo USN**](a-usncreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-entre sites**](a-usnintersite.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-fonte**](a-usnsource.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WBEM-caminho**](a-wbempath.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-alterado**](a-whenchanged.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-criado**](a-whencreated.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-outro**](a-url.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Direitos estendidos do Windows Server 2003 R2

Essa classe contém os seguintes direitos estendidos para o Windows Server 2003 R2:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Gravações validadas do Windows Server 2003 R2

Essa classe contém as seguintes gravações validadas para o Windows Server 2003 R2:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Conjuntos de propriedades do Windows Server 2003 R2

Essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2003 R2:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Direitos estendidos](#windows-server-2008-extended-rights)
-   [Gravações validadas](#windows-server-2008-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2008-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md)do DNS [**BuiltIn-**](c-builtindomain.md)[**contêiner**](c-container.md)de domínio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**email de caixa**](c-mailrecipient.md) de [**segurança de objeto**](c-securityprincipal.md) [**POSIX**](c-posixgroup.md)(sistema) – destinatário (sistema)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Atributos do Windows Server 2008

Essa classe contém os seguintes atributos para o Windows Server 2008:



| Atributo                                                                        | Obrigatório | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome da conta-histórico**](a-accountnamehistory.md)                             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Conta de administrador**](a-admincount.md)                                              | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-segurança-identidades**](a-altsecurityidentities.md)                       | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                        | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comum**](a-cn.md)                                                      | True      | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> |
| [**Controle-acesso-direitos**](a-controlaccessrights.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de desktop**](a-desktopprofile.md)                                      | Falso     | **Grupo**                                                                                                                          |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DSA-assinatura**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Email-endereços**](a-mail.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Flags**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                               | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Grupo-Associação-SAM**](a-groupmembershipsam.md)                             | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | True      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                          | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É excluído**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Último-pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Gerenciado por**](a-managedby.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mestre por**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Generic-data**](a-msds-azgenericdata.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Last-imported-biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-não-membros**](a-msds-nonmembers.md)                                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-domínio**](a-mssfu30nisdomain.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member**](a-mssfu30posixmember.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoria**](a-objectcategory.md)                                      | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                            | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-Sid**](a-objectsid.md)                                                | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Operador-contagem**](a-operatorcount.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo primário**](a-primarygrouptoken.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Eliminá**](a-rid.md)                                                             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-tipo de conta**](a-samaccounttype.md)                                     | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**secretário**](a-secretary.md)                                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de segurança**](a-securityidentifier.md)                              | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Histórico de SID**](a-sidhistory.md)                                              | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)                    | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Número de telefone**](a-telephonenumber.md)                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                        | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-global-e-universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-no-GC-aceitável**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuário**](a-usercert.md)                                                  | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Usuário-senha**](a-userpassword.md)                                          | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                         | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Direitos estendidos do Windows Server 2008

Essa classe contém os seguintes direitos estendidos para o Windows Server 2008:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Gravações validadas do Windows Server 2008

Essa classe contém as seguintes gravações validadas para o Windows Server 2008:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Conjuntos de propriedades do Windows Server 2008

Essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2008:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Direitos estendidos](#windows-server-2008-r2-extended-rights)
-   [Gravações validadas](#windows-server-2008-r2-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2008-r2-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md)do DNS [**BuiltIn-**](c-builtindomain.md)[**contêiner**](c-container.md)de domínio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**email de caixa**](c-mailrecipient.md) de [**segurança de objeto**](c-securityprincipal.md) [**POSIX**](c-posixgroup.md)(sistema) – destinatário (sistema)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Atributos do Windows Server 2008 R2

Essa classe contém os seguintes atributos para o Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome da conta-histórico**](a-accountnamehistory.md)                             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Conta de administrador**](a-admincount.md)                                              | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-segurança-identidades**](a-altsecurityidentities.md)                       | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                        | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comum**](a-cn.md)                                                      | True      | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> |
| [**Controle-acesso-direitos**](a-controlaccessrights.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de desktop**](a-desktopprofile.md)                                      | Falso     | **Grupo**                                                                                                                          |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DSA-assinatura**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Email-endereços**](a-mail.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Flags**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                               | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Grupo-Associação-SAM**](a-groupmembershipsam.md)                             | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | True      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                          | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É excluído**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É reciclado**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Último-pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Gerenciado por**](a-managedby.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mestre por**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Generic-data**](a-msds-azgenericdata.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Last-imported-biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-não-membros**](a-msds-nonmembers.md)                                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-domínio**](a-mssfu30nisdomain.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member**](a-mssfu30posixmember.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoria**](a-objectcategory.md)                                      | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                            | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-Sid**](a-objectsid.md)                                                | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Operador-contagem**](a-operatorcount.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo primário**](a-primarygrouptoken.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Eliminá**](a-rid.md)                                                             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-tipo de conta**](a-samaccounttype.md)                                     | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**secretário**](a-secretary.md)                                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de segurança**](a-securityidentifier.md)                              | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Histórico de SID**](a-sidhistory.md)                                              | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)                    | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Número de telefone**](a-telephonenumber.md)                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                        | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-global-e-universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-no-GC-aceitável**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuário**](a-usercert.md)                                                  | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Usuário-senha**](a-userpassword.md)                                          | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                         | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Direitos estendidos do Windows Server 2008 R2

Essa classe contém os seguintes direitos estendidos para o Windows Server 2008 R2:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Gravações validadas do Windows Server 2008 R2

Essa classe contém as seguintes gravações validadas para o Windows Server 2008 R2:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Conjuntos de propriedades do Windows Server 2008 R2

Essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2008 R2:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Direitos estendidos](#windows-server-2012-extended-rights)
-   [Gravações validadas](#windows-server-2012-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2012-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional**](c-organizationalunit.md)do DNS [**BuiltIn-**](c-builtindomain.md)[**contêiner**](c-container.md)de domínio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**email de caixa**](c-mailrecipient.md) de [**segurança de objeto**](c-securityprincipal.md) [**POSIX**](c-posixgroup.md)(sistema) – destinatário (sistema)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Atributos do Windows Server 2012

Essa classe contém os seguintes atributos para o Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome da conta-histórico**](a-accountnamehistory.md)                                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Conta de administrador**](a-admincount.md)                                                          | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-segurança-identidades**](a-altsecurityidentities.md)                                   | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comum**](a-cn.md)                                                                  | True      | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> |
| [**Controle-acesso-direitos**](a-controlaccessrights.md)                                       | Falso     | **Grupo**                                                                                                                          |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de desktop**](a-desktopprofile.md)                                                  | Falso     | **Grupo**                                                                                                                          |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DSA-assinatura**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Email-endereços**](a-mail.md)                                                           | Falso     | **Grupo**                                                                                                                          |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Flags**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**Grupo-Associação-SAM**](a-groupmembershipsam.md)                                         | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                            | True      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                                      | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É excluído**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**É reciclado**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Último-pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Gerenciado por**](a-managedby.md)                                                            | Falso     | **Grupo**                                                                                                                          |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mestre por**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                                   | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Generic-data**](a-msds-azgenericdata.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Last-imported-biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                                          | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-geocoordinations-altitude**](a-msds-geocoordinatesaltitude.md)                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-geocoordinations-latitude**](a-msds-geocoordinateslatitude.md)                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-geocoordinations-longitude**](a-msds-geocoordinateslongitude.md)                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-keyversionnumber**](a-msds-keyversionnumber.md)                                    | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-não-membros**](a-msds-nonmembers.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Primary-Computer**](a-msds-primarycomputer.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-egresso-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-domínio**](a-mssfu30nisdomain.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member**](a-mssfu30posixmember.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                                 | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoria**](a-objectcategory.md)                                                  | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                                        | True      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**GUID do objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-Sid**](a-objectsid.md)                                                            | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Operador-contagem**](a-operatorcount.md)                                                    | Falso     | **Grupo**                                                                                                                          |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo primário**](a-primarygrouptoken.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Representantes-de**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Eliminá**](a-rid.md)                                                                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                                 | True      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-tipo de conta**](a-samaccounttype.md)                                                 | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**secretário**](a-secretary.md)                                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de segurança**](a-securityidentifier.md)                                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Histórico de SID**](a-sidhistory.md)                                                          | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sub-referências**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Suplementos-credenciais**](a-supplementalcredentials.md)                                | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Sinalizadores do sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Número de telefone**](a-telephonenumber.md)                                                | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                                        | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-global-e-universal**](a-tokengroupsglobalanduniversal.md)                 | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-groups-no-GC-aceitável**](a-tokengroupsnogcacceptable.md)                         | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuário**](a-usercert.md)                                                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Usuário-senha**](a-userpassword.md)                                                      | Falso     | [**o POSIX**](c-posixgroup.md)<br/>                                                                                      |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Criado pelo USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-entre sites**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-fonte**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WBEM-caminho**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Direitos estendidos do Windows Server 2012

Essa classe contém os seguintes direitos estendidos para o Windows Server 2012:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Gravações validadas do Windows Server 2012

Essa classe contém as seguintes gravações validadas para o Windows Server 2012:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Conjuntos de propriedades do Windows Server 2012

Essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2012:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



 

 





