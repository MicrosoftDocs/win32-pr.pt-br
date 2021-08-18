---
title: classe de grupo
description: Armazena uma lista de nomes de usuário. Usado para aplicar entidades de segurança em recursos.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Esquema do AD da classe de grupo
- classe de grupo Esquema do AD
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae33b53eff8305fee4698c5aed2bb072f3fa5b90a5922d0099e40e90f9b3fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021904"
---
# <a name="group-class"></a>classe de grupo

Armazena uma lista de nomes de usuário. Usado para aplicar entidades de segurança em recursos.



| Entrada | Valor |
|-------------------|------------------------------------------------|
| CN                | Agrupar                                          |
| Ldap-Display-Name | group                                          |
| Privilégio de atualização  | Esse valor é definido pelo administrador de domínio. |
| Frequência de atualização  | \-                                             |
| Schema-Id-Guid    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Direitos Estendidos](#windows-2000-server-extended-rights)
-   [Gravações validadas](#windows-2000-server-validated-writes)
-   [Conjuntos de propriedades](#windows-2000-server-property-sets)



| Entrada | Valor |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Valor ocultado padrão        | 0                                                                                                                                                                                                   |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                              |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                     |
| Possíveis superiores          | [**Contêiner de domínio de**](c-domaindns.md)unidade [**de domínio**](c-organizationalunit.md)de [**unidade organizacional**](c-builtindomain.md)[**DNS**](c-container.md)                                       |
| Classes Auxiliares           | [**Destinatário de email**](c-securityprincipal.md) da entidade de [**segurança (sistema)**](c-mailrecipient.md) (sistema)                                                                                        |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                        |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Windows atributos de servidor do Windows 2000

Essa classe contém os seguintes atributos para Windows 2000 Server:



| Atributo                                                                    | Obrigatório | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Histórico de nomes da conta**](a-accountnamehistory.md)                         | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Contagem de administradores**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                    |
| [**Descrição do administrador**](a-admindescription.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome canônico**](a-canonicalname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Comentário**](a-info.md)                                                    | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Common-Name**](a-cn.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                    |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Descrição**](a-description.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                    |
| [**Nome de exibição**](a-displayname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Assinatura DSA**](a-dsasignature.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços de email**](a-mail.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Nome da extensão**](a-extensionname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sinalizadores**](a-flags.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Entrada de entrada**](a-fromentry.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Período de coleta de lixo**](a-garbagecollperiod.md)                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                    |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | Verdadeiro      | **Grupo**                                                                                    |
| [**Tipo de instância**](a-instancetype.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Último pai conhecido**](a-lastknownparent.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Gerenciado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                    |
| [**Objetos gerenciados**](a-managedobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                    |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Não membro de segurança**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                    |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                    |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                     | Verdadeiro      | [**Início**](c-top.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Categoria de objeto**](a-objectcategory.md)                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sid de objeto**](a-objectsid.md)                                            | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Versão do objeto**](a-objectversion.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Contagem de operadores**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                    |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Possíveis inferiores**](a-possibleinferiors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços proxy**](a-proxyaddresses.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Relatórios**](a-directreports.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Revisão**](a-revision.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Livrar**](a-rid.md)                                                         | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Name**](a-samaccountname.md)                                 | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Tipo de conta SAM**](a-samaccounttype.md)                                 | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Identificador de segurança**](a-securityidentifier.md)                          | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
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



## <a name="windows-2000-server-extended-rights"></a>direitos estendidos do Windows Server 2000

essa classe contém os seguintes direitos estendidos para o Windows Server 2000:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Windows de gravações validadas do servidor 2000

essa classe contém as seguintes gravações validadas para o Windows Server 2000:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Windows conjuntos de propriedades do servidor 2000

essa classe contém os seguintes conjuntos de propriedades para Windows servidor 2000:



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



## <a name="windows-server-2003-attributes"></a>Windows Atributos do servidor 2003

essa classe contém os seguintes atributos para o Windows Server 2003:



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
| [**Nome comum**](a-cn.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/>         |
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
| [**Sinalizadores**](a-flags.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Entrada de entrada**](a-fromentry.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Período de coleta de lixo**](a-garbagecollperiod.md)                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                    |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | Verdadeiro      | **Grupo**                                                                                    |
| [**Tipo de instância**](a-instancetype.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Último pai conhecido**](a-lastknownparent.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Gerenciado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                    |
| [**Objetos gerenciados**](a-managedobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                    |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Grupo**                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falso     | **Grupo**                                                                                    |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Não membro de segurança**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                    |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                    |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                     | Verdadeiro      | [**Início**](c-top.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Categoria de objeto**](a-objectcategory.md)                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sid de objeto**](a-objectsid.md)                                            | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Versão do objeto**](a-objectversion.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Contagem de operadores**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                    |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Possíveis inferiores**](a-possibleinferiors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços proxy**](a-proxyaddresses.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Relatórios**](a-directreports.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Revisão**](a-revision.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Livrar**](a-rid.md)                                                         | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Name**](a-samaccountname.md)                                 | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Tipo de conta SAM**](a-samaccounttype.md)                                 | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**secretário**](a-secretary.md)                                             | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Identificador de segurança**](a-securityidentifier.md)                          | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Histórico de SID**](a-sidhistory.md)                                          | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sub-refs**](a-subrefs.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Credenciais complementares**](a-supplementalcredentials.md)                | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Sinalizadores de sistema**](a-systemflags.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Número de telefone**](a-telephonenumber.md)                                | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Certificado do usuário**](a-usercert.md)                                              | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                         |
| [**USN alterado**](a-usnchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criado por USN**](a-usncreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
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



## <a name="windows-server-2003-extended-rights"></a>Windows Direitos estendidos do servidor 2003

essa classe contém os seguintes direitos estendidos para o Windows Server 2003:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows Gravações validadas do servidor 2003

essa classe contém as seguintes gravações validadas para o Windows Server 2003:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Windows Conjuntos de propriedades do servidor 2003

essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2003:



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
| [**Tipo de grupo**](a-grouptype.md)                                           | Verdadeiro      | **Grupo**                                                                                    |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
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
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-categoria**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objeto-Sid**](a-objectsid.md)                                           | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                 |
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
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objetos conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Home Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Gravações validadas pelo ADAM

Essa classe contém as seguintes gravações validadas para ADAM:



| Nome comum                                  |
|----------------------------------------------|
| [**Autoa associação**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Conjuntos de propriedades ADAM

Essa classe contém os seguintes conjuntos de propriedades para ADAM:



| Nome comum                                      |
|--------------------------------------------------|
| [**Informações de email**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Direitos Estendidos](#windows-server-2003-r2-extended-rights)
-   [Gravações validadas](#windows-server-2003-r2-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2003-r2-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor ocultado padrão        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possíveis superiores          | [**Contêiner**](c-domaindns.md)[](c-organizationalunit.md)de unidade organizacional de domínio DNS [**builtin-domain**](c-builtindomain.md)[](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**PosixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos do Server 2003 R2

Essa classe contém os seguintes atributos para Windows Server 2003 R2:



| Atributo                                                                    | Obrigatório | Derivado de                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Histórico de nomes da conta**](a-accountnamehistory.md)                         | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Contagem de administradores**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comum**](a-cn.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> |
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
| [**Tipo de grupo**](a-grouptype.md)                                            | Verdadeiro      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
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
| [**memberUid**](a-memberuid.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                       | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                        | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não-segurança-membro**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Verdadeiro      | [**Início**](c-top.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoria**](a-objectcategory.md)                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**GUID do objeto**](a-objectguid.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-Sid**](a-objectsid.md)                                            | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
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
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
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



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Direitos estendidos do Server 2003 R2

essa classe contém os seguintes direitos estendidos para o Windows Server 2003 R2:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Windows Gravações validadas do Server 2003 R2

Essa classe contém as seguintes gravações validadas para Windows Server 2003 R2:



| Nome comum                                  |
|----------------------------------------------|
| [**Autoa associação**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Conjuntos de propriedades do Server 2003 R2

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2003 R2:



| Nome comum                                      |
|--------------------------------------------------|
| [**Informações de email**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Direitos Estendidos](#windows-server-2008-extended-rights)
-   [Gravações validadas](#windows-server-2008-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2008-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor ocultado padrão        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possíveis superiores          | [**Contêiner**](c-domaindns.md)[](c-organizationalunit.md)de unidade organizacional de domínio DNS [**builtin-domain**](c-builtindomain.md)[](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**PosixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Atributos do Server 2008

Essa classe contém os seguintes atributos para Windows Server 2008:



| Atributo                                                                        | Obrigatório | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Histórico de nomes da conta**](a-accountnamehistory.md)                             | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Contagem de administradores**](a-admincount.md)                                              | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                       | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                        | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                      | Falso     | **Grupo**                                                                                                                          |
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
| [**Tipo de grupo**](a-grouptype.md)                                                | Verdadeiro      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
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
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não membro de segurança**](a-nonsecuritymember.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                         | Verdadeiro      | [**Início**](c-top.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Categoria de objeto**](a-objectcategory.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                            | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sid de objeto**](a-objectsid.md)                                                | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Contagem de operadores**](a-operatorcount.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Endereços proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Eliminá**](a-rid.md)                                                             | Falso     | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
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
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Certificado X509**](a-usercertificate.md)                                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Windows Direitos Estendidos do Server 2008

Essa classe contém os seguintes direitos estendidos para Windows Server 2008:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows Gravações validadas do Servidor 2008

Essa classe contém as seguintes gravações validadas para Windows Server 2008:



| Nome comum                                  |
|----------------------------------------------|
| [**Autoa associação**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Windows Conjuntos de propriedades do Server 2008

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2008:



| Nome comum                                      |
|--------------------------------------------------|
| [**Informações de email**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Direitos Estendidos](#windows-server-2008-r2-extended-rights)
-   [Gravações validadas](#windows-server-2008-r2-validated-writes)
-   [Conjuntos de propriedades](#windows-server-2008-r2-property-sets)



| Entrada | Valor |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor ocultado padrão        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possíveis superiores          | [**Contêiner**](c-domaindns.md)[](c-organizationalunit.md)de unidade organizacional de domínio DNS [**builtin-domain**](c-builtindomain.md)[](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classes Auxiliares           | [**PosixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos do Server 2008 R2

Essa classe contém os seguintes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Histórico de nomes da conta**](a-accountnamehistory.md)                             | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Contagem de administradores**](a-admincount.md)                                              | Falso     | **Grupo**                                                                                                                          |
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                       | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Comentário**](a-info.md)                                                        | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                      | Falso     | **Grupo**                                                                                                                          |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Assinatura DSA**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Endereços de email**](a-mail.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sinalizadores**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Entrada de entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Período de coleta de lixo**](a-garbagecollperiod.md)                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Gidnumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                             | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | Verdadeiro      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Último pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
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
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não membro de segurança**](a-nonsecuritymember.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                         | Verdadeiro      | [**Início**](c-top.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoria**](a-objectcategory.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                            | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objeto-Sid**](a-objectsid.md)                                                | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
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
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
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
| [**Sub-refs**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Credenciais complementares**](a-supplementalcredentials.md)                    | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Sinalizadores de sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Número de telefone**](a-telephonenumber.md)                                    | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado do usuário**](a-usercert.md)                                                  | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**Senha do usuário**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**USN alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Criado por USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**UsN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Quando criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Certificado X509**](a-usercertificate.md)                                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Direitos Estendidos do Servidor 2008 R2

Essa classe contém os seguintes direitos estendidos para Windows Server 2008 R2:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Windows Gravações validadas do Servidor 2008 R2

Essa classe contém as seguintes gravações validadas para Windows Server 2008 R2:



| Nome comum                                  |
|----------------------------------------------|
| [**Autoa associação**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Conjuntos de propriedades do Server 2008 R2

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2008 R2:



| Nome comum                                      |
|--------------------------------------------------|
| [**Informações de email**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Direitos Estendidos](#windows-server-2012-extended-rights)
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



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



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
| [**Nome comum**](a-cn.md)                                                                  | Verdadeiro      | [**Início**](c-top.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> |
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
| [**Tipo de grupo**](a-grouptype.md)                                                            | Verdadeiro      | **Grupo**                                                                                                                          |
| [**Tipo de instância**](a-instancetype.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
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
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Primary-Computer**](a-msds-primarycomputer.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Não membro de segurança**](a-nonsecuritymember.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                                 | Falso     | **Grupo**                                                                                                                          |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Categoria de objeto**](a-objectcategory.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Classe de objeto**](a-objectclass.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Sid de objeto**](a-objectsid.md)                                                            | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                                                       |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                    |
| [**Contagem de operadores**](a-operatorcount.md)                                                    | Falso     | **Grupo**                                                                                                                          |
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
| [**SAM-Account-Name**](a-samaccountname.md)                                                 | Verdadeiro      | [**Segurança-principal**](c-securityprincipal.md)<br/>                                                                       |
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



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Direitos estendidos

Essa classe contém os seguintes direitos estendidos para Windows Server 2012:



| Nome comum                  |
|------------------------------|
| [**Enviar para**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Gravações validadas

Essa classe contém as seguintes gravações validadas para Windows Server 2012:



| Nome comum                                  |
|----------------------------------------------|
| [**Associação automática**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Conjuntos de propriedades

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2012:



| Nome comum                                      |
|--------------------------------------------------|
| [**Email-informações**](r-email-information.md) |



 

 





