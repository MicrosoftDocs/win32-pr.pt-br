---
title: Classe Organizational-Person
description: Essa classe é usada para objetos que contêm informações organizacionais sobre um usuário, como o número do funcionário, departamento, gerente, título, endereço do Office e assim por diante.
ms.assetid: dbcecb0d-e7ab-4005-82ad-5ffe9b06a380
ms.tgt_platform: multiple
keywords:
- Esquema de AD de classe de Organizational-Person
- Esquema de AD da classe organizationalPerson
topic_type:
- apiref
api_name:
- Organizational-Person
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0f12e1a82f2386f213246c99b9f63570f14d00a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086586"
---
# <a name="organizational-person-class"></a>Classe Organizational-Person

Essa classe é usada para objetos que contêm informações organizacionais sobre um usuário, como o número do funcionário, departamento, gerente, título, endereço do Office e assim por diante.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Organizational-Person                |
| LDAP-Display-Name | organizationalPerson                 |
| Privilégio de atualização  | Qualquer pessoa pode atualizar este objeto.       |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | bf967aa4-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 2                                                                                            |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 2.5.6.7                                                                                      |
| Padrão-ocultando valor        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Pessoa**](c-person.md)<br/>                                                        |
| Superiores possíveis          | [**Contêiner**](c-container.md)                                                             |
| Classes Auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Atributos do Windows 2000 Server

Essa classe contém os seguintes atributos para o Windows 2000 Server:



| Atributo                                                                 | Obrigatório | Derivado de                                                          |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Endereço**](a-streetaddress.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Endereço-página inicial**](a-homepostaladdress.md)                               | Falso     | **Organizational-Person**                                             |
| [**Descrição do administrador**](a-admindescription.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Administração – nome de exibição**](a-admindisplayname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md) | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Assistant**](a-assistant.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome canônico**](a-canonicalname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome comum**](a-cn.md)                                               | True      | [**Pessoa**](c-person.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Código do país**](a-countrycode.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Nome do país**](a-c.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Inteiros**](a-department.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Descrição**](a-description.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Destino-indicador**](a-destinationindicator.md)                   | Falso     | **Organizational-Person**                                             |
| [**Nome de exibição**](a-displayname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Divisão**](a-division.md)                                            | Falso     | **Organizational-Person**                                             |
| [**DSA-assinatura**](a-dsasignature.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Email-endereços**](a-mail.md)                                        | Falso     | **Organizational-Person**                                             |
| [**ID do funcionário**](a-employeeid.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome da extensão**](a-extensionname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)          | Falso     | **Organizational-Person**                                             |
| [**Flags**](a-flags.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**De entrada**](a-fromentry.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Qualificador de geração**](a-generationqualifier.md)                     | Falso     | **Organizational-Person**                                             |
| [**Nome fornecido**](a-givenname.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Iniciais**](a-initials.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Tipo de instância**](a-instancetype.md)                                   | True      | [**Início**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | **Organizational-Person**                                             |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É excluído**](a-isdeleted.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Último-pai conhecido**](a-lastknownparent.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Localidade-nome**](a-l.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Logotipo**](a-thumbnaillogo.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Objetos gerenciados**](a-managedobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Mestre por**](a-masteredby.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MHS-ou-address**](a-mhsoraddress.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | [**Início**](c-top.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objeto-categoria**](a-objectcategory.md)                               | True      | [**Início**](c-top.md)<br/>                                       |
| [**Classe de objeto**](a-objectclass.md)                                     | True      | [**Início**](c-top.md)<br/>                                       |
| [**GUID do objeto**](a-objectguid.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Versão do objeto**](a-objectversion.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome da unidade organizacional**](a-ou.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Nome da organização**](a-o.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Outros-caixa de correio**](a-othermailbox.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Outro nome**](a-middlename.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md) | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Título pessoal**](a-personaltitle.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-fax-outro**](a-otherfacsimiletelephonenumber.md)                | Falso     | **Organizational-Person**                                             |
| [**Telefone-casa-outro**](a-otherhomephone.md)                              | Falso     | **Organizational-Person**                                             |
| [**Telefone-residência-primário**](a-homephone.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-outro**](a-otheripphone.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-primário**](a-ipphone.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-outro**](a-othermobile.md)                               | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-primário**](a-mobile.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Telefone-escritório-outro**](a-othertelephone.md)                            | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-outro**](a-otherpager.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-primário**](a-pager.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Entrega física-nome do escritório**](a-physicaldeliveryofficename.md)     | Falso     | **Organizational-Person**                                             |
| [**Imagem**](a-thumbnailphoto.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço postal**](a-postaladdress.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Código postal**](a-postalcode.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Caixa Post-Office**](a-postofficebox.md)                                | Falso     | **Organizational-Person**                                             |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)            | Falso     | **Organizational-Person**                                             |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereços de proxy**](a-proxyaddresses.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulta-política-BL**](a-querypolicybl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço registrado**](a-registeredaddress.md)                         | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Relatórios**](a-directreports.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Representantes-de**](a-repsfrom.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Revisão**](a-revision.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulte-também**](a-seealso.md)                                             | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Estado-ou-província-nome**](a-st.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Endereço da rua**](a-street.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Sub-referências**](a-subrefs.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sobrenome**](a-sn.md)                                                   | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Número de telefone**](a-telephonenumber.md)                             | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)        | Falso     | **Organizational-Person**                                             |
| [**Número de telex**](a-telexnumber.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telex-primário**](a-primarytelexnumber.md)                             | Falso     | **Organizational-Person**                                             |
| [**Texto-país**](a-co.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Título**](a-title.md)                                                  | Falso     | **Organizational-Person**                                             |
| [**Comentário do usuário**](a-comment.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Usuário-senha**](a-userpassword.md)                                   | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Criado pelo USN**](a-usncreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-entre sites**](a-usnintersite.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-fonte**](a-usnsource.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WBEM-caminho**](a-wbempath.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-alterado**](a-whenchanged.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-criado**](a-whencreated.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-página-outro**](a-url.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**X121-endereço**](a-x121address.md)                                     | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Valor |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Padrão-ocultando valor        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                    |
| Subclasse de                 | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Superiores possíveis          | [**Unidade organizacional**](c-organizationalunit.md) da [**organização**](c-organization.md)de [**contêineres**](c-container.md) |
| Classes Auxiliares           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                              |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-attributes"></a>Atributos do Windows Server 2003

Essa classe contém os seguintes atributos para o Windows Server 2003:



| Atributo                                                                   | Obrigatório | Derivado de                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Endereço**](a-streetaddress.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Endereço-página inicial**](a-homepostaladdress.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Assistant**](a-assistant.md)                                            | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome comum**](a-cn.md)                                                 | True      | [**Pessoa**](c-person.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Código do país**](a-countrycode.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome do país**](a-c.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Inteiros**](a-department.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Destino-indicador**](a-destinationindicator.md)                     | Falso     | **Organizational-Person**                                             |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Divisão**](a-division.md)                                              | Falso     | **Organizational-Person**                                             |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Email-endereços**](a-mail.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ID do funcionário**](a-employeeid.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Qualificador de geração**](a-generationqualifier.md)                       | Falso     | **Organizational-Person**                                             |
| [**Nome fornecido**](a-givenname.md)                                           | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | **Organizational-Person**                                             |
| [**Iniciais**](a-initials.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | [**Início**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Localidade-nome**](a-l.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MHS-ou-address**](a-mhsoraddress.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | **Organizational-Person**                                             |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Início**](c-top.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | [**Início**](c-top.md)<br/>                                       |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | [**Início**](c-top.md)<br/>                                       |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Nome da organização**](a-o.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Outros-caixa de correio**](a-othermailbox.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Outro nome**](a-middlename.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Título pessoal**](a-personaltitle.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-fax-outro**](a-otherfacsimiletelephonenumber.md)                  | Falso     | **Organizational-Person**                                             |
| [**Telefone-casa-outro**](a-otherhomephone.md)                                | Falso     | **Organizational-Person**                                             |
| [**Telefone-residência-primário**](a-homephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-outro**](a-otheripphone.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-primário**](a-ipphone.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-outro**](a-othermobile.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-primário**](a-mobile.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefone-escritório-outro**](a-othertelephone.md)                              | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-outro**](a-otherpager.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-primário**](a-pager.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Entrega física-nome do escritório**](a-physicaldeliveryofficename.md)       | Falso     | **Organizational-Person**                                             |
| [**Imagem**](a-thumbnailphoto.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Código postal**](a-postalcode.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Caixa Post-Office**](a-postofficebox.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)              | Falso     | **Organizational-Person**                                             |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulte-também**](a-seealso.md)                                               | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Número de série**](a-serialnumber.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Estado-ou-província-nome**](a-st.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Endereço da rua**](a-street.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sobrenome**](a-sn.md)                                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)          | Falso     | **Organizational-Person**                                             |
| [**Número de telex**](a-telexnumber.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telex-primário**](a-primarytelexnumber.md)                               | Falso     | **Organizational-Person**                                             |
| [**Texto-país**](a-co.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Título**](a-title.md)                                                    | Falso     | **Organizational-Person**                                             |
| [**Comentário do usuário**](a-comment.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Usuário-senha**](a-userpassword.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**X121-endereço**](a-x121address.md)                                       | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Valor |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Padrão-ocultando valor        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                    |
| Subclasse de                 | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Superiores possíveis          | [**Unidade organizacional**](c-organizationalunit.md) da [**organização**](c-organization.md)de [**contêineres**](c-container.md) |
| Classes Auxiliares           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                              |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-r2-attributes"></a>Atributos do Windows Server 2003 R2

Essa classe contém os seguintes atributos para o Windows Server 2003 R2:



| Atributo                                                                   | Obrigatório | Derivado de                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Endereço**](a-streetaddress.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Endereço-página inicial**](a-homepostaladdress.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Administração – nome de exibição**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Assistant**](a-assistant.md)                                            | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome comum**](a-cn.md)                                                 | True      | [**Pessoa**](c-person.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Código do país**](a-countrycode.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome do país**](a-c.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Inteiros**](a-department.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Destino-indicador**](a-destinationindicator.md)                     | Falso     | **Organizational-Person**                                             |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Divisão**](a-division.md)                                              | Falso     | **Organizational-Person**                                             |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Email-endereços**](a-mail.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ID do funcionário**](a-employeeid.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Qualificador de geração**](a-generationqualifier.md)                       | Falso     | **Organizational-Person**                                             |
| [**Nome fornecido**](a-givenname.md)                                           | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | **Organizational-Person**                                             |
| [**Iniciais**](a-initials.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Tipo de instância**](a-instancetype.md)                                     | True      | [**Início**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Localidade-nome**](a-l.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MHS-ou-address**](a-mhsoraddress.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | **Organizational-Person**                                             |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Início**](c-top.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objeto-categoria**](a-objectcategory.md)                                 | True      | [**Início**](c-top.md)<br/>                                       |
| [**Classe de objeto**](a-objectclass.md)                                       | True      | [**Início**](c-top.md)<br/>                                       |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Nome da organização**](a-o.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Outros-caixa de correio**](a-othermailbox.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Outro nome**](a-middlename.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Título pessoal**](a-personaltitle.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-fax-outro**](a-otherfacsimiletelephonenumber.md)                  | Falso     | **Organizational-Person**                                             |
| [**Telefone-casa-outro**](a-otherhomephone.md)                                | Falso     | **Organizational-Person**                                             |
| [**Telefone-residência-primário**](a-homephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-outro**](a-otheripphone.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-primário**](a-ipphone.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-outro**](a-othermobile.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-primário**](a-mobile.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefone-escritório-outro**](a-othertelephone.md)                              | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-outro**](a-otherpager.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-primário**](a-pager.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Entrega física-nome do escritório**](a-physicaldeliveryofficename.md)       | Falso     | **Organizational-Person**                                             |
| [**Imagem**](a-thumbnailphoto.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Código postal**](a-postalcode.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Caixa Post-Office**](a-postofficebox.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)              | Falso     | **Organizational-Person**                                             |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulte-também**](a-seealso.md)                                               | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Número de série**](a-serialnumber.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Estado-ou-província-nome**](a-st.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Endereço da rua**](a-street.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sobrenome**](a-sn.md)                                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)          | Falso     | **Organizational-Person**                                             |
| [**Número de telex**](a-telexnumber.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telex-primário**](a-primarytelexnumber.md)                               | Falso     | **Organizational-Person**                                             |
| [**Texto-país**](a-co.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Título**](a-title.md)                                                    | Falso     | **Organizational-Person**                                             |
| [**Comentário do usuário**](a-comment.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Usuário-senha**](a-userpassword.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**X121-endereço**](a-x121address.md)                                       | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Valor |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Padrão-ocultando valor        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                    |
| Subclasse de                 | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Superiores possíveis          | [**Unidade organizacional**](c-organizationalunit.md) da [**organização**](c-organization.md)de [**contêineres**](c-container.md) |
| Classes Auxiliares           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                              |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-attributes"></a>Atributos do Windows Server 2008

Essa classe contém os seguintes atributos para o Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de                                                          |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Endereço**](a-streetaddress.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Endereço-página inicial**](a-homepostaladdress.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Administração – nome de exibição**](a-admindisplayname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Assistant**](a-assistant.md)                                               | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome comum**](a-cn.md)                                                    | True      | [**Pessoa**](c-person.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Código do país**](a-countrycode.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Nome do país**](a-c.md)                                                    | Falso     | **Organizational-Person**                                             |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Inteiros**](a-department.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Descrição**](a-description.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Destino-indicador**](a-destinationindicator.md)                        | Falso     | **Organizational-Person**                                             |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Divisão**](a-division.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**DSA-assinatura**](a-dsasignature.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Email-endereços**](a-mail.md)                                             | Falso     | **Organizational-Person**                                             |
| [**ID do funcionário**](a-employeeid.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)               | Falso     | **Organizational-Person**                                             |
| [**Flags**](a-flags.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**De entrada**](a-fromentry.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Qualificador de geração**](a-generationqualifier.md)                          | Falso     | **Organizational-Person**                                             |
| [**Nome fornecido**](a-givenname.md)                                              | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Iniciais**](a-initials.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Tipo de instância**](a-instancetype.md)                                        | True      | [**Início**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | **Organizational-Person**                                             |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É excluído**](a-isdeleted.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Último-pai conhecido**](a-lastknownparent.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Localidade-nome**](a-l.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Logotipo**](a-thumbnaillogo.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Mestre por**](a-masteredby.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MHS-ou-address**](a-mhsoraddress.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)             | Falso     | **Organizational-Person**                                             |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-HAB-senioridade-índice**](a-msds-habseniorityindex.md)                  | Falso     | **Organizational-Person**                                             |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-fonética-Company-Name**](a-msds-phoneticcompanyname.md)              | Falso     | **Organizational-Person**                                             |
| [**ms-DS-fonético-Department**](a-msds-phoneticdepartment.md)                 | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | Falso     | **Organizational-Person**                                             |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | [**Início**](c-top.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objeto-categoria**](a-objectcategory.md)                                    | True      | [**Início**](c-top.md)<br/>                                       |
| [**Classe de objeto**](a-objectclass.md)                                          | True      | [**Início**](c-top.md)<br/>                                       |
| [**GUID do objeto**](a-objectguid.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome da unidade organizacional**](a-ou.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome da organização**](a-o.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Outros-caixa de correio**](a-othermailbox.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Outro nome**](a-middlename.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Título pessoal**](a-personaltitle.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefone-fax-outro**](a-otherfacsimiletelephonenumber.md)                     | Falso     | **Organizational-Person**                                             |
| [**Telefone-casa-outro**](a-otherhomephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-residência-primário**](a-homephone.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-outro**](a-otheripphone.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-primário**](a-ipphone.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-outro**](a-othermobile.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-primário**](a-mobile.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefone-escritório-outro**](a-othertelephone.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-outro**](a-otherpager.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-primário**](a-pager.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Entrega física-nome do escritório**](a-physicaldeliveryofficename.md)          | Falso     | **Organizational-Person**                                             |
| [**Imagem**](a-thumbnailphoto.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço postal**](a-postaladdress.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Código postal**](a-postalcode.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Caixa Post-Office**](a-postofficebox.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                 | Falso     | **Organizational-Person**                                             |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereços de proxy**](a-proxyaddresses.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulta-política-BL**](a-querypolicybl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço registrado**](a-registeredaddress.md)                              | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Relatórios**](a-directreports.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Representantes-de**](a-repsfrom.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Revisão**](a-revision.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulte-também**](a-seealso.md)                                                  | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Número de série**](a-serialnumber.md)                                        | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Estado-ou-província-nome**](a-st.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Endereço da rua**](a-street.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sub-referências**](a-subrefs.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sobrenome**](a-sn.md)                                                        | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Número de telefone**](a-telephonenumber.md)                                  | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)             | Falso     | **Organizational-Person**                                             |
| [**Número de telex**](a-telexnumber.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Telex-primário**](a-primarytelexnumber.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Texto-país**](a-co.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Título**](a-title.md)                                                       | Falso     | **Organizational-Person**                                             |
| [**Comentário do usuário**](a-comment.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Usuário-senha**](a-userpassword.md)                                        | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Criado pelo USN**](a-usncreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-entre sites**](a-usnintersite.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-fonte**](a-usnsource.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WBEM-caminho**](a-wbempath.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-alterado**](a-whenchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-criado**](a-whencreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-página-outro**](a-url.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**X121-endereço**](a-x121address.md)                                          | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Valor |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Padrão-ocultando valor        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                    |
| Subclasse de                 | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Superiores possíveis          | [**Unidade organizacional**](c-organizationalunit.md) da [**organização**](c-organization.md)de [**contêineres**](c-container.md) |
| Classes Auxiliares           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                              |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-r2-attributes"></a>Atributos do Windows Server 2008 R2

Essa classe contém os seguintes atributos para o Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                                          |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Endereço**](a-streetaddress.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Endereço-página inicial**](a-homepostaladdress.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Assistant**](a-assistant.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome comum**](a-cn.md)                                                      | True      | [**Pessoa**](c-person.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Código do país**](a-countrycode.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Nome do país**](a-c.md)                                                      | Falso     | **Organizational-Person**                                             |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Inteiros**](a-department.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Destino-indicador**](a-destinationindicator.md)                          | Falso     | **Organizational-Person**                                             |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Divisão**](a-division.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**DSA-assinatura**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Email-endereços**](a-mail.md)                                               | Falso     | **Organizational-Person**                                             |
| [**ID do funcionário**](a-employeeid.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)                 | Falso     | **Organizational-Person**                                             |
| [**Flags**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**De entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Qualificador de geração**](a-generationqualifier.md)                            | Falso     | **Organizational-Person**                                             |
| [**Nome fornecido**](a-givenname.md)                                                | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Iniciais**](a-initials.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Tipo de instância**](a-instancetype.md)                                          | True      | [**Início**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | **Organizational-Person**                                             |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É excluído**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É reciclado**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Último-pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Localidade-nome**](a-l.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Logotipo**](a-thumbnaillogo.md)                                                  | Falso     | **Organizational-Person**                                             |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Mestre por**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MHS-ou-address**](a-mhsoraddress.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)               | Falso     | **Organizational-Person**                                             |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-HAB-senioridade-índice**](a-msds-habseniorityindex.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-fonética-Company-Name**](a-msds-phoneticcompanyname.md)                | Falso     | **Organizational-Person**                                             |
| [**ms-DS-fonético-Department**](a-msds-phoneticdepartment.md)                   | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | Falso     | **Organizational-Person**                                             |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | Falso     | **Organizational-Person**                                             |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Início**](c-top.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objeto-categoria**](a-objectcategory.md)                                      | True      | [**Início**](c-top.md)<br/>                                       |
| [**Classe de objeto**](a-objectclass.md)                                            | True      | [**Início**](c-top.md)<br/>                                       |
| [**GUID do objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome da unidade organizacional**](a-ou.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Nome da organização**](a-o.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Outros-caixa de correio**](a-othermailbox.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Outro nome**](a-middlename.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Título pessoal**](a-personaltitle.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Telefone-fax-outro**](a-otherfacsimiletelephonenumber.md)                       | Falso     | **Organizational-Person**                                             |
| [**Telefone-casa-outro**](a-otherhomephone.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telefone-residência-primário**](a-homephone.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-outro**](a-otheripphone.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-primário**](a-ipphone.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-outro**](a-othermobile.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-primário**](a-mobile.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Telefone-escritório-outro**](a-othertelephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-outro**](a-otherpager.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-primário**](a-pager.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Entrega física-nome do escritório**](a-physicaldeliveryofficename.md)            | Falso     | **Organizational-Person**                                             |
| [**Imagem**](a-thumbnailphoto.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço postal**](a-postaladdress.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Código postal**](a-postalcode.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Caixa Post-Office**](a-postofficebox.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                   | Falso     | **Organizational-Person**                                             |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço registrado**](a-registeredaddress.md)                                | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulte-também**](a-seealso.md)                                                    | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Número de série**](a-serialnumber.md)                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Estado-ou-província-nome**](a-st.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Endereço da rua**](a-street.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sobrenome**](a-sn.md)                                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Número de telefone**](a-telephonenumber.md)                                    | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)               | Falso     | **Organizational-Person**                                             |
| [**Número de telex**](a-telexnumber.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Telex-primário**](a-primarytelexnumber.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Texto-país**](a-co.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Título**](a-title.md)                                                         | Falso     | **Organizational-Person**                                             |
| [**Comentário do usuário**](a-comment.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Usuário-senha**](a-userpassword.md)                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Criado pelo USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-entre sites**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-fonte**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WBEM-caminho**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-página-outro**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**X121-endereço**](a-x121address.md)                                            | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Padrão-ocultando valor        | 1                                                                                                                         |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                                                    |
| Subclasse de                 | [**Pessoa**](c-person.md)<br/>                                                                                     |
| Superiores possíveis          | [**Unidade organizacional**](c-organizationalunit.md) da [**organização**](c-organization.md)de [**contêineres**](c-container.md) |
| Classes Auxiliares           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                                              |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2012-attributes"></a>Atributos do Windows Server 2012

Essa classe contém os seguintes atributos para o Windows Server 2012:



| Atributo                                                                                              | Obrigatório | Derivado de                                                          |
|--------------------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Endereço**](a-streetaddress.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Endereço-página inicial**](a-homepostaladdress.md)                                                            | Falso     | **Organizational-Person**                                             |
| [**Descrição do administrador**](a-admindescription.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Atributos permitidos**](a-allowedattributes.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Assistant**](a-assistant.md)                                                                       | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome canônico**](a-canonicalname.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome comum**](a-cn.md)                                                                            | True      | [**Pessoa**](c-person.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Código do país**](a-countrycode.md)                                                                  | Falso     | **Organizational-Person**                                             |
| [**Nome do país**](a-c.md)                                                                            | Falso     | **Organizational-Person**                                             |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Inteiros**](a-department.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Descrição**](a-description.md)                                                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Destino-indicador**](a-destinationindicator.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Nome de exibição**](a-displayname.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Divisão**](a-division.md)                                                                         | Falso     | **Organizational-Person**                                             |
| [**DSA-assinatura**](a-dsasignature.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Email-endereços**](a-mail.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**ID do funcionário**](a-employeeid.md)                                                                    | Falso     | **Organizational-Person**                                             |
| [**Nome da extensão**](a-extensionname.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Flags**](a-flags.md)                                                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**De entrada**](a-fromentry.md)                                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Qualificador de geração**](a-generationqualifier.md)                                                  | Falso     | **Organizational-Person**                                             |
| [**Nome fornecido**](a-givenname.md)                                                                      | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | Falso     | **Organizational-Person**                                             |
| [**Iniciais**](a-initials.md)                                                                         | Falso     | **Organizational-Person**                                             |
| [**Tipo de instância**](a-instancetype.md)                                                                | True      | [**Início**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | Falso     | **Organizational-Person**                                             |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É excluído**](a-isdeleted.md)                                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Is-member-of-DL**](a-memberof.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**É reciclado**](a-isrecycled.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Último-pai conhecido**](a-lastknownparent.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Localidade-nome**](a-l.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Logotipo**](a-thumbnaillogo.md)                                                                        | Falso     | **Organizational-Person**                                             |
| [**Objetos gerenciados**](a-managedobjects.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Mestre por**](a-masteredby.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MHS-ou-address**](a-mhsoraddress.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-allowed-to-Act-on-of-from-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | Falso     | **Organizational-Person**                                             |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)                                     | Falso     | **Organizational-Person**                                             |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Claim-shares-possíveis-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-habilitado-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-HAB-senioridade-índice**](a-msds-habseniorityindex.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-is-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-local-efetivo-hora de exclusão**](a-msds-localeffectivedeletiontime.md)                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-local-efetivo-recicl-time**](a-msds-localeffectiverecycletime.md)                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-fonética-Company-Name**](a-msds-phoneticcompanyname.md)                                      | Falso     | **Organizational-Person**                                             |
| [**ms-DS-fonético-Department**](a-msds-phoneticdepartment.md)                                         | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | Falso     | **Organizational-Person**                                             |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-egresso-BL**](a-msds-tdoegressbl.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | True      | [**Início**](c-top.md)<br/>                                       |
| [**Obj-dist-Name**](a-distinguishedname.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objeto-categoria**](a-objectcategory.md)                                                            | True      | [**Início**](c-top.md)<br/>                                       |
| [**Classe de objeto**](a-objectclass.md)                                                                  | True      | [**Início**](c-top.md)<br/>                                       |
| [**GUID do objeto**](a-objectguid.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Versão do objeto**](a-objectversion.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Nome da unidade organizacional**](a-ou.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Nome da organização**](a-o.md)                                                                       | Falso     | **Organizational-Person**                                             |
| [**Outros-caixa de correio**](a-othermailbox.md)                                                                | Falso     | **Organizational-Person**                                             |
| [**Outro nome**](a-middlename.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Título pessoal**](a-personaltitle.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Telefone-fax-outro**](a-otherfacsimiletelephonenumber.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Telefone-casa-outro**](a-otherhomephone.md)                                                           | Falso     | **Organizational-Person**                                             |
| [**Telefone-residência-primário**](a-homephone.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-outro**](a-otheripphone.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Telefone-IP-primário**](a-ipphone.md)                                                                  | Falso     | **Organizational-Person**                                             |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-outro**](a-othermobile.md)                                                            | Falso     | **Organizational-Person**                                             |
| [**Telefone-celular-primário**](a-mobile.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Telefone-escritório-outro**](a-othertelephone.md)                                                         | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-outro**](a-otherpager.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Telefone-pager-primário**](a-pager.md)                                                                 | Falso     | **Organizational-Person**                                             |
| [**Entrega física-nome do escritório**](a-physicaldeliveryofficename.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Imagem**](a-thumbnailphoto.md)                                                                    | Falso     | **Organizational-Person**                                             |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço postal**](a-postaladdress.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Código postal**](a-postalcode.md)                                                                    | Falso     | **Organizational-Person**                                             |
| [**Caixa Post-Office**](a-postofficebox.md)                                                             | Falso     | **Organizational-Person**                                             |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Endereço registrado**](a-registeredaddress.md)                                                      | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Relatórios**](a-directreports.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Representantes-de**](a-repsfrom.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Reps-to**](a-repsto.md)                                                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Revisão**](a-revision.md)                                                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Consulte-também**](a-seealso.md)                                                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Número de série**](a-serialnumber.md)                                                                | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Estado-ou-província-nome**](a-st.md)                                                                 | Falso     | **Organizational-Person**                                             |
| [**Endereço da rua**](a-street.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sub-referências**](a-subrefs.md)                                                                          | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Sobrenome**](a-sn.md)                                                                                | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Sinalizadores do sistema**](a-systemflags.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Número de telefone**](a-telephonenumber.md)                                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Número de telex**](a-telexnumber.md)                                                                  | Falso     | **Organizational-Person**                                             |
| [**Telex-primário**](a-primarytelexnumber.md)                                                          | Falso     | **Organizational-Person**                                             |
| [**Texto-país**](a-co.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Título**](a-title.md)                                                                               | Falso     | **Organizational-Person**                                             |
| [**Comentário do usuário**](a-comment.md)                                                                      | Falso     | **Organizational-Person**                                             |
| [**Usuário-senha**](a-userpassword.md)                                                                | Falso     | [**Pessoa**](c-person.md)<br/>                                 |
| [**USN-alterado**](a-usnchanged.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Criado pelo USN**](a-usncreated.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-entre sites**](a-usnintersite.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**USN-fonte**](a-usnsource.md)                                                                      | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WBEM-caminho**](a-wbempath.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-alterado**](a-whenchanged.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**Quando-criado**](a-whencreated.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                                 | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**WWW-página-outro**](a-url.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                       |
| [**X121-endereço**](a-x121address.md)                                                                  | Falso     | **Organizational-Person**                                             |



 

 





