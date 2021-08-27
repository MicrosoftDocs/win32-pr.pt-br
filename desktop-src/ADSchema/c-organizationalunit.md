---
title: Classe Organizational-Unit
description: Um contêiner para armazenar usuários, computadores e outros objetos de conta.
ms.assetid: a5a99dc7-9000-478c-9545-473cfb6ddf6c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de classe de Organizational-Unit
- Esquema de AD da classe organizationalUnit
topic_type:
- apiref
api_name:
- Organizational-Unit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79807cc71f5e7690aca04b80f0d5560399b8b5415fc1d7f3cf9654884b7b9c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065286"
---
# <a name="organizational-unit-class"></a>Classe Organizational-Unit

Um contêiner para armazenar usuários, computadores e outros objetos de conta.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Organizational-Unit                  |
| LDAP-Display-Name | organizationalUnit                   |
| Privilégio de atualização  | Qualquer pessoa pode atualizar este objeto.       |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | bf967aa5-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                        |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                       |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                  |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                        |
| RDN-ATT-ID                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                                                                                                                                                                                                      |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                          |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**organização**](c-organization.md) da **unidade organizacional** do DNS                                                                                                                                                                                                           |
| Classes Auxiliares           | \-                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                             |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO) (OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO) (OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO) (OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                               |



## <a name="windows-2000-server-attributes"></a>Windows atributos do servidor 2000

essa classe contém os seguintes atributos para Windows servidor 2000:



| Atributo                                                                 | Obrigatório | Derivado de                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Administração – nome de exibição**](a-admindisplayname.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de negócios**](a-businesscategory.md)                           | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome comum**](a-cn.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Código do país**](a-countrycode.md)                                     | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                               | Falso     | **Unidade organizacional**         |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                   | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de desktop**](a-desktopprofile.md)                               | Falso     | **Unidade organizacional**         |
| [**Destino-indicador**](a-destinationindicator.md)                   | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**DSA-assinatura**](a-dsasignature.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da extensão**](a-extensionname.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)          | Falso     | **Unidade organizacional**         |
| [**Flags**](a-flags.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**De entrada**](a-fromentry.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**GP-link**](a-gplink.md)                                               | Falso     | **Unidade organizacional**         |
| [**GP-opções**](a-gpoptions.md)                                         | Falso     | **Unidade organizacional**         |
| [**Tipo de instância**](a-instancetype.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | **Unidade organizacional**         |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**É excluído**](a-isdeleted.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Último-pai conhecido**](a-lastknownparent.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Localidade-nome**](a-l.md)                                              | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                           | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                         | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Mestre por**](a-masteredby.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Objeto-categoria**](a-objectcategory.md)                               | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**GUID do objeto**](a-objectguid.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                  | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)     | Falso     | **Unidade organizacional**         |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                 | Falso     | **Unidade organizacional**         |
| [**Código postal**](a-postalcode.md)                                       | Falso     | **Unidade organizacional**         |
| [**caixa de Office**](a-postofficebox.md)                                | Falso     | **Unidade organizacional**         |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)            | Falso     | **Unidade organizacional**         |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços de proxy**](a-proxyaddresses.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Consulta-política-BL**](a-querypolicybl.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                         | Falso     | **Unidade organizacional**         |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Relatórios**](a-directreports.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Representantes-de**](a-repsfrom.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Guia de pesquisa**](a-searchguide.md)                                     | Falso     | **Unidade organizacional**         |
| [**Consulte-também**](a-seealso.md)                                             | Falso     | **Unidade organizacional**         |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)            | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Estado-ou-província-nome**](a-st.md)                                    | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                        | Falso     | **Unidade organizacional**         |
| [**Sub-refs**](a-subrefs.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores de sistema**](a-systemflags.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                             | Falso     | **Unidade organizacional**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | **Unidade organizacional**         |
| [**Telex-Number**](a-telexnumber.md)                                     | Falso     | **Unidade organizacional**         |
| [**País de texto**](a-co.md)                                              | Falso     | **Unidade organizacional**         |
| [**Sufixos UPN**](a-upnsuffixes.md)                                     | Falso     | **Unidade organizacional**         |
| [**Senha do usuário**](a-userpassword.md)                                   | Falso     | **Unidade organizacional**         |
| [**USN alterado**](a-usnchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado por USN**](a-usncreated.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**Início**](c-top.md)<br/> |
| [**UsN-Intersite**](a-usnintersite.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos conhecidos**](a-wellknownobjects.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando alterado**](a-whenchanged.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando criado**](a-whencreated.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home Page**](a-wwwhomepage.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço X121**](a-x121address.md)                                     | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Direitos Estendidos](#windows-server-2003-extended-rights)



| Entrada | Valor |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valor ocultado padrão        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possíveis superiores          | [**País da organização**](c-domaindns.md)**da unidade organizacional** do DNS [**do**](c-organization.md)[**domínio**](c-country.md)                                                                                                                                                                                                                                                    |
| Classes Auxiliares           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Windows Atributos do Server 2003

Essa classe contém os seguintes atributos para Windows Server 2003:



| Atributo                                                                   | Obrigatório | Derivado de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de negócios**](a-businesscategory.md)                             | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome comum**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Código do país**](a-countrycode.md)                                       | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                                 | Falso     | **Unidade organizacional**         |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                     | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de desktop**](a-desktopprofile.md)                                 | Falso     | **Unidade organizacional**         |
| [**Destino-indicador**](a-destinationindicator.md)                     | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)            | Falso     | **Unidade organizacional**         |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**GP-link**](a-gplink.md)                                                 | Falso     | **Unidade organizacional**         |
| [**GP-opções**](a-gpoptions.md)                                           | Falso     | **Unidade organizacional**         |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unidade organizacional**         |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Localidade-nome**](a-l.md)                                                | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falso     | **Unidade organizacional**         |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Objeto-categoria**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unidade organizacional**         |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | **Unidade organizacional**         |
| [**Código postal**](a-postalcode.md)                                         | Falso     | **Unidade organizacional**         |
| [**caixa de Office**](a-postofficebox.md)                                  | Falso     | **Unidade organizacional**         |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)              | Falso     | **Unidade organizacional**         |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | **Unidade organizacional**         |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Guia de pesquisa**](a-searchguide.md)                                       | Falso     | **Unidade organizacional**         |
| [**Consulte-também**](a-seealso.md)                                               | Falso     | **Unidade organizacional**         |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Estado-ou-província-nome**](a-st.md)                                      | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                          | Falso     | **Unidade organizacional**         |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Sub-refs**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores de sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | **Unidade organizacional**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unidade organizacional**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Unidade organizacional**         |
| [**País de texto**](a-co.md)                                                | Falso     | **Unidade organizacional**         |
| [**Sufixos UPN**](a-upnsuffixes.md)                                       | Falso     | **Unidade organizacional**         |
| [**Senha do usuário**](a-userpassword.md)                                     | Falso     | **Unidade organizacional**         |
| [**USN alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado por USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**UsN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço X121**](a-x121address.md)                                       | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2003-extended-rights"></a>Windows Direitos Estendidos do Server 2003

Essa classe contém os seguintes direitos estendidos para Windows Server 2003:



| Nome comum                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="adam"></a>Adam

-   [Atributos](#adam-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                      |
| Object-Category             | 1                                                                                                                          |
| Default-Object-Category     | \-                                                                                                                         |
| Governs-Id                  | 2.5.6.5                                                                                                                    |
| Valor ocultado padrão        | 0                                                                                                                          |
| Rdn-Att-Id                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                        |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                            |
| Possíveis superiores          | [**País da organização**](c-domaindns.md)**da unidade organizacional** do DNS [**do**](c-organization.md)[**domínio**](c-country.md) |
| Classes Auxiliares           | \-                                                                                                                         |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                               |
| Descritor de segurança padrão | D:S:                                                                                                                       |
| System-Flags                | 0x00000010                                                                                                                 |



## <a name="adam-attributes"></a>Atributos do ADAM

Essa classe contém os seguintes atributos para ADAM:



| Atributo                                                                   | Obrigatório | Derivado de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de negócios**](a-businesscategory.md)                             | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome comum**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Código do país**](a-countrycode.md)                                       | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                                 | Falso     | **Unidade organizacional**         |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                     | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de desktop**](a-desktopprofile.md)                                 | Falso     | **Unidade organizacional**         |
| [**Destino-indicador**](a-destinationindicator.md)                     | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)            | Falso     | **Unidade organizacional**         |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unidade organizacional**         |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Localidade-nome**](a-l.md)                                                | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de objeto**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unidade organizacional**         |
| [**Possíveis inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | **Unidade organizacional**         |
| [**Cep**](a-postalcode.md)                                         | Falso     | **Unidade organizacional**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Unidade organizacional**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falso     | **Unidade organizacional**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | **Unidade organizacional**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                       | Falso     | **Unidade organizacional**         |
| [**Consulte também**](a-seealso.md)                                               | Falso     | **Unidade organizacional**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                          | Falso     | **Unidade organizacional**         |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Sub-refs**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores de sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | **Unidade organizacional**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unidade organizacional**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Unidade organizacional**         |
| [**País de texto**](a-co.md)                                                | Falso     | **Unidade organizacional**         |
| [**Sufixos UPN**](a-upnsuffixes.md)                                       | Falso     | **Unidade organizacional**         |
| [**Senha do usuário**](a-userpassword.md)                                     | Falso     | **Unidade organizacional**         |
| [**USN alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado por USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**UsN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço X121**](a-x121address.md)                                       | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Direitos Estendidos](#windows-server-2003-r2-extended-rights)



| Entrada | Valor |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valor ocultado padrão        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possíveis superiores          | [**País da organização**](c-domaindns.md)**da unidade organizacional** do DNS [**do**](c-organization.md)[**domínio**](c-country.md)                                                                                                                                                                                                                                                    |
| Classes Auxiliares           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos do Server 2003 R2

Essa classe contém os seguintes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Obrigatório | Derivado de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria comercial**](a-businesscategory.md)                             | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Código-país**](a-countrycode.md)                                       | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                                 | Falso     | **Unidade organizacional**         |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                     | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                 | Falso     | **Unidade organizacional**         |
| [**Indicador de destino**](a-destinationindicator.md)                     | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Assinatura DSA**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | **Unidade organizacional**         |
| [**Sinalizadores**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Entrada de entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                 | Falso     | **Unidade organizacional**         |
| [**Opções de GP**](a-gpoptions.md)                                           | Falso     | **Unidade organizacional**         |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unidade organizacional**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Último pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                           | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falso     | **Unidade organizacional**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de objeto**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unidade organizacional**         |
| [**Possíveis inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | **Unidade organizacional**         |
| [**Cep**](a-postalcode.md)                                         | Falso     | **Unidade organizacional**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Unidade organizacional**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falso     | **Unidade organizacional**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | **Unidade organizacional**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Search-Guide**](a-searchguide.md)                                       | Falso     | **Unidade organizacional**         |
| [**Consulte também**](a-seealso.md)                                               | Falso     | **Unidade organizacional**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                          | Falso     | **Unidade organizacional**         |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Sub-refs**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores de sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | **Unidade organizacional**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unidade organizacional**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Unidade organizacional**         |
| [**País de texto**](a-co.md)                                                | Falso     | **Unidade organizacional**         |
| [**Sufixos UPN**](a-upnsuffixes.md)                                       | Falso     | **Unidade organizacional**         |
| [**Senha do usuário**](a-userpassword.md)                                     | Falso     | **Unidade organizacional**         |
| [**USN alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado por USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**UsN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço X121**](a-x121address.md)                                       | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Direitos Estendidos do Servidor 2003 R2

Essa classe contém os seguintes direitos estendidos para Windows Server 2003 R2:



| Nome comum                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Direitos Estendidos](#windows-server-2008-extended-rights)



| Entrada | Valor |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valor ocultado padrão        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possíveis superiores          | [**País da organização**](c-domaindns.md)**da unidade organizacional** do DNS [**do**](c-organization.md)[**domínio**](c-country.md)                                                                                                                                                                                                                                                    |
| Classes Auxiliares           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Windows Atributos do Server 2008

Essa classe contém os seguintes atributos para Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria comercial**](a-businesscategory.md)                                | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Código-país**](a-countrycode.md)                                          | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                                    | Falso     | **Unidade organizacional**         |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                        | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                    | Falso     | **Unidade organizacional**         |
| [**Indicador de destino**](a-destinationindicator.md)                        | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Assinatura DSA**](a-dsasignature.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falso     | **Unidade organizacional**         |
| [**Sinalizadores**](a-flags.md)                                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Entrada de entrada**](a-fromentry.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                    | Falso     | **Unidade organizacional**         |
| [**Opções de GP**](a-gpoptions.md)                                              | Falso     | **Unidade organizacional**         |
| [**Tipo de instância**](a-instancetype.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | **Unidade organizacional**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Último pai conhecido**](a-lastknownparent.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                   | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                                | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                              | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)            | Falso     | **Unidade organizacional**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Início**](c-top.md)<br/> |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                       | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Objeto-categoria**](a-objectcategory.md)                                    | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**GUID do objeto**](a-objectguid.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                       | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)          | Falso     | **Unidade organizacional**         |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                      | Falso     | **Unidade organizacional**         |
| [**Código postal**](a-postalcode.md)                                            | Falso     | **Unidade organizacional**         |
| [**caixa de Office**](a-postofficebox.md)                                     | Falso     | **Unidade organizacional**         |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                 | Falso     | **Unidade organizacional**         |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços de proxy**](a-proxyaddresses.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Consulta-política-BL**](a-querypolicybl.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                              | Falso     | **Unidade organizacional**         |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Relatórios**](a-directreports.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Representantes-de**](a-repsfrom.md)                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Guia de pesquisa**](a-searchguide.md)                                          | Falso     | **Unidade organizacional**         |
| [**Consulte-também**](a-seealso.md)                                                  | Falso     | **Unidade organizacional**         |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Estado-ou-província-nome**](a-st.md)                                         | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                             | Falso     | **Unidade organizacional**         |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Sub-referências**](a-subrefs.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores do sistema**](a-systemflags.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                                  | Falso     | **Unidade organizacional**         |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)             | Falso     | **Unidade organizacional**         |
| [**Número de telex**](a-telexnumber.md)                                          | Falso     | **Unidade organizacional**         |
| [**Texto-país**](a-co.md)                                                   | Falso     | **Unidade organizacional**         |
| [**Sufixos de UPN**](a-upnsuffixes.md)                                          | Falso     | **Unidade organizacional**         |
| [**Usuário-senha**](a-userpassword.md)                                        | Falso     | **Unidade organizacional**         |
| [**USN-alterado**](a-usnchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado pelo USN**](a-usncreated.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-entre sites**](a-usnintersite.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-fonte**](a-usnsource.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**WBEM-caminho**](a-wbempath.md)                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando-alterado**](a-whenchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando-criado**](a-whencreated.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-página-outro**](a-url.md)                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**X121-endereço**](a-x121address.md)                                          | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2008-extended-rights"></a>Windows Direitos estendidos do servidor 2008

essa classe contém os seguintes direitos estendidos para o Windows Server 2008:



| Nome comum                                                |
|------------------------------------------------------------|
| [**Gerar-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Gerar-RSoP-log**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Direitos estendidos](#windows-server-2008-r2-extended-rights)



| Entrada | Valor |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**país**](c-country.md) da [**organização**](c-organization.md)da **unidade organizacional** DNS                                                                                                                                                                                                                                                    |
| Classes Auxiliares           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos do Server 2008 R2

Essa classe contém os seguintes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria comercial**](a-businesscategory.md)                                  | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Código-país**](a-countrycode.md)                                            | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                                      | Falso     | **Unidade organizacional**         |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                          | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                      | Falso     | **Unidade organizacional**         |
| [**Indicador de destino**](a-destinationindicator.md)                          | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Assinatura DSA**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falso     | **Unidade organizacional**         |
| [**Sinalizadores**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Entrada de entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                      | Falso     | **Unidade organizacional**         |
| [**Opções de GP**](a-gpoptions.md)                                                | Falso     | **Unidade organizacional**         |
| [**Tipo de instância**](a-instancetype.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | **Unidade organizacional**         |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**É excluído**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**É reciclado**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Último-pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Localidade-nome**](a-l.md)                                                     | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                                  | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                                | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Mestre por**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)              | Falso     | **Unidade organizacional**         |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/> |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                         | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de objeto**](a-objectcategory.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                            | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                         | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falso     | **Unidade organizacional**         |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                        | Falso     | **Unidade organizacional**         |
| [**Código postal**](a-postalcode.md)                                              | Falso     | **Unidade organizacional**         |
| [**caixa de Office**](a-postofficebox.md)                                       | Falso     | **Unidade organizacional**         |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                   | Falso     | **Unidade organizacional**         |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                                | Falso     | **Unidade organizacional**         |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Guia de pesquisa**](a-searchguide.md)                                            | Falso     | **Unidade organizacional**         |
| [**Consulte-também**](a-seealso.md)                                                    | Falso     | **Unidade organizacional**         |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Estado-ou-província-nome**](a-st.md)                                           | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                               | Falso     | **Unidade organizacional**         |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                                    | Falso     | **Unidade organizacional**         |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)               | Falso     | **Unidade organizacional**         |
| [**Número de telex**](a-telexnumber.md)                                            | Falso     | **Unidade organizacional**         |
| [**Texto-país**](a-co.md)                                                     | Falso     | **Unidade organizacional**         |
| [**Sufixos de UPN**](a-upnsuffixes.md)                                            | Falso     | **Unidade organizacional**         |
| [**Usuário-senha**](a-userpassword.md)                                          | Falso     | **Unidade organizacional**         |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**X121-endereço**](a-x121address.md)                                            | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Direitos estendidos do Server 2008 R2

essa classe contém os seguintes direitos estendidos para o Windows Server 2008 R2:



| Nome comum                                                |
|------------------------------------------------------------|
| [**Gerar-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Gerar-RSoP-log**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Direitos estendidos](#windows-server-2012-extended-rights)



| Entrada | Valor |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Categoria de objeto-padrão     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Padrão-ocultando valor        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-ATT-ID                  | [**Nome da unidade organizacional**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Subclasse de                 | [**Início**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**país**](c-country.md) da [**organização**](c-organization.md)da **unidade organizacional** DNS                                                                                                                                                                                                                                                    |
| Classes Auxiliares           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO) (OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO) (OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO) (OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU) (A;; LCRPLORC;;; ED) (OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                    | Obrigatório | Derivado de                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrição do administrador**](a-admindescription.md)                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de negócios**](a-businesscategory.md)                                              | Falso     | **Unidade organizacional**         |
| [**Nome canônico**](a-canonicalname.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Código-país**](a-countrycode.md)                                                        | Falso     | **Unidade organizacional**         |
| [**Nome do país**](a-c.md)                                                                  | Falso     | **Unidade organizacional**         |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Grupo padrão**](a-defaultgroup.md)                                                      | Falso     | **Unidade organizacional**         |
| [**Descrição**](a-description.md)                                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Perfil de Área de Trabalho**](a-desktopprofile.md)                                                  | Falso     | **Unidade organizacional**         |
| [**Indicador de destino**](a-destinationindicator.md)                                      | Falso     | **Unidade organizacional**         |
| [**Nome de exibição**](a-displayname.md)                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Assinatura DSA**](a-dsasignature.md)                                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da extensão**](a-extensionname.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                             | Falso     | **Unidade organizacional**         |
| [**Sinalizadores**](a-flags.md)                                                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Entrada de entrada**](a-fromentry.md)                                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**GP-Link**](a-gplink.md)                                                                  | Falso     | **Unidade organizacional**         |
| [**Opções de GP**](a-gpoptions.md)                                                            | Falso     | **Unidade organizacional**         |
| [**Tipo de instância**](a-instancetype.md)                                                      | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                               | Falso     | **Unidade organizacional**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Is-Recycled**](a-isrecycled.md)                                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Último pai conhecido**](a-lastknownparent.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                                 | Falso     | **Unidade organizacional**         |
| [**Logotipo**](a-thumbnaillogo.md)                                                              | Falso     | **Unidade organizacional**         |
| [**Gerenciado por**](a-managedby.md)                                                            | Falso     | **Unidade organizacional**         |
| [**Objetos gerenciados**](a-managedobjects.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Mestre por**](a-masteredby.md)                                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)                          | Falso     | **Unidade organizacional**         |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Início**](c-top.md)<br/> |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Início**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Início**](c-top.md)<br/> |
| [**Categoria de objeto**](a-objectcategory.md)                                                  | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Classe de objeto**](a-objectclass.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Versão do objeto**](a-objectversion.md)                                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Nome da unidade organizacional**](a-ou.md)                                                     | Verdadeiro      | **Unidade organizacional**         |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                        | Falso     | **Unidade organizacional**         |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço postal**](a-postaladdress.md)                                                    | Falso     | **Unidade organizacional**         |
| [**Cep**](a-postalcode.md)                                                          | Falso     | **Unidade organizacional**         |
| [**Post-Office-Box**](a-postofficebox.md)                                                   | Falso     | **Unidade organizacional**         |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                               | Falso     | **Unidade organizacional**         |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Endereço registrado**](a-registeredaddress.md)                                            | Falso     | **Unidade organizacional**         |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                    | Falso     | [**Início**](c-top.md)<br/> |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                                         | Falso     | [**Início**](c-top.md)<br/> |
| [**Relatórios**](a-directreports.md)                                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Representantes-de**](a-repsfrom.md)                                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Reps-to**](a-repsto.md)                                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**Revisão**](a-revision.md)                                                               | Falso     | [**Início**](c-top.md)<br/> |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Guia de pesquisa**](a-searchguide.md)                                                        | Falso     | **Unidade organizacional**         |
| [**Consulte-também**](a-seealso.md)                                                                | Falso     | **Unidade organizacional**         |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                                           | Falso     | [**Início**](c-top.md)<br/> |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                               | Falso     | [**Início**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Início**](c-top.md)<br/> |
| [**Estado-ou-província-nome**](a-st.md)                                                       | Falso     | **Unidade organizacional**         |
| [**Endereço da rua**](a-street.md)                                                           | Falso     | **Unidade organizacional**         |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**Sub-referências**](a-subrefs.md)                                                                | Falso     | [**Início**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Sinalizadores do sistema**](a-systemflags.md)                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Número de telefone**](a-telephonenumber.md)                                                | Falso     | **Unidade organizacional**         |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)                           | Falso     | **Unidade organizacional**         |
| [**Número de telex**](a-telexnumber.md)                                                        | Falso     | **Unidade organizacional**         |
| [**Texto-país**](a-co.md)                                                                 | Falso     | **Unidade organizacional**         |
| [**Sufixos de UPN**](a-upnsuffixes.md)                                                        | Falso     | **Unidade organizacional**         |
| [**Usuário-senha**](a-userpassword.md)                                                      | Falso     | **Unidade organizacional**         |
| [**USN-alterado**](a-usnchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**Criado pelo USN**](a-usncreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                                   | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-entre sites**](a-usnintersite.md)                                                      | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**Início**](c-top.md)<br/> |
| [**USN-fonte**](a-usnsource.md)                                                            | Falso     | [**Início**](c-top.md)<br/> |
| [**WBEM-caminho**](a-wbempath.md)                                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                             | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando-alterado**](a-whenchanged.md)                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**Quando-criado**](a-whencreated.md)                                                        | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**Início**](c-top.md)<br/> |
| [**WWW-página-outro**](a-url.md)                                                              | Falso     | [**Início**](c-top.md)<br/> |
| [**X121-endereço**](a-x121address.md)                                                        | Falso     | **Unidade organizacional**         |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Direitos estendidos

Essa classe contém os seguintes direitos estendidos para Windows Server 2012:



| Nome comum                                                |
|------------------------------------------------------------|
| [**Gerar-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Gerar-RSoP-log**](r-generate-rsop-logging.md)   |



 

 





