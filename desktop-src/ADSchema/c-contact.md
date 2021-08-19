---
title: Classe Contact
description: Essa classe contém informações sobre uma pessoa ou empresa que talvez você precise entrar em contato regularmente.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- Esquema do AD de classe de contato
- Esquema do AD de classe de contato
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b54d5929e11382c1680090adf376f670d8610fd767a193e349a31f54c1f2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021884"
---
# <a name="contact-class"></a>Classe Contact

Essa classe contém informações sobre uma pessoa ou empresa que talvez você precise entrar em contato regularmente.



| Entrada | Valor |
|-------------------|------------------------------------------------|
| CN                | Contact                                        |
| LDAP-Display-Name | contact                                        |
| Privilégio de atualização  | Esse valor é definido pelo administrador de domínio. |
| Frequência de atualização  | \-                                             |
| Schema-ID-GUID    | 5cb41ed0-0e4c-11d0-a286-00aa003049e2           |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)
-   [Conjuntos de propriedades](#windows-2000-server-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Padrão-ocultando valor        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional** DNS](c-organizationalunit.md)         |
| Classes Auxiliares           | [**Destinatário de email**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows atributos do servidor 2000

essa classe contém os seguintes atributos para Windows servidor 2000:



| Atributo                                                                 | Obrigatório | Derivado de                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informações adicionais**](a-notes.md)                                 | Falso     | **Contact**                                                                                                                            |
| [**Endereço**](a-streetaddress.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço-página inicial**](a-homepostaladdress.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição do administrador**](a-admindescription.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Administração – nome de exibição**](a-admindisplayname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Assistant**](a-assistant.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome canônico**](a-canonicalname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Comentário**](a-info.md)                                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nome comum**](a-cn.md)                                               | Verdadeiro      |  [ **Pessoa** de contato](c-person.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**Início**](c-top.md)<br/> |
| [**Corporativa**](a-company.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código do país**](a-countrycode.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome do país**](a-c.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição**](a-description.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Destino-indicador**](a-destinationindicator.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome de exibição**](a-displayname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Divisão**](a-division.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Email-endereços**](a-mail.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID do funcionário**](a-employeeid.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da extensão**](a-extensionname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Flags**](a-flags.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                        | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificador de geração**](a-generationqualifier.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome fornecido**](a-givenname.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciais**](a-initials.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instância**](a-instancetype.md)                                   | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É excluído**](a-isdeleted.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Último-pai conhecido**](a-lastknownparent.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidade-nome**](a-l.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mestre por**](a-masteredby.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-address**](a-mhsoraddress.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Obj-dist-Name**](a-distinguishedname.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoria**](a-objectcategory.md)                               | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classe de objeto**](a-objectclass.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**GUID do objeto**](a-objectguid.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Versão do objeto**](a-objectversion.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome da unidade organizacional**](a-ou.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da organização**](a-o.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros-caixa de correio**](a-othermailbox.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outro nome**](a-middlename.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Título pessoal**](a-personaltitle.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Fax-outro**](a-otherfacsimiletelephonenumber.md)                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-outro**](a-otherhomephone.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-principal**](a-homephone.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-outro**](a-otheripphone.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-primário**](a-ipphone.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-outro**](a-othermobile.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-primário**](a-mobile.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Office-outro**](a-othertelephone.md)                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-outro**](a-otherpager.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-primário**](a-pager.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagem**](a-thumbnailphoto.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço postal**](a-postaladdress.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**caixa de Office**](a-postofficebox.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de proxy**](a-proxyaddresses.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Consulta-política-BL**](a-querypolicybl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço registrado**](a-registeredaddress.md)                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Relatórios**](a-directreports.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Representantes-de**](a-repsfrom.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Revisão**](a-revision.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Consulte-também**](a-seealso.md)                                             | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Estado-ou-província-nome**](a-st.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço da rua**](a-street.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Sub-referências**](a-subrefs.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sobrenome**](a-sn.md)                                                   | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Número de telefone**](a-telephonenumber.md)                             | Falso     | [**Pessoa**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País de texto**](a-co.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado do usuário**](a-usercert.md)                                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentário do usuário**](a-comment.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Senha do usuário**](a-userpassword.md)                                   | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                  | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN alterado**](a-usnchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Criado por USN**](a-usncreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**UsN-Intersite**](a-usnintersite.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objetos conhecidos**](a-wellknownobjects.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando alterado**](a-whenchanged.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando criado**](a-whencreated.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Home Page**](a-wwwhomepage.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço X121**](a-x121address.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado X509**](a-usercertificate.md)                                    | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>Windows de propriedades do servidor 2000

Essa classe contém os seguintes conjuntos de propriedades para Windows 2000 Server:



| Nome comum                                            |
|--------------------------------------------------------|
| [**Informações pessoais**](r-personal-information.md) |
| [**Informações da Web**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Conjuntos de propriedades](#windows-server-2003-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor ocultado padrão        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Possíveis superiores          | [**Unidade organizacional do DNS**](c-domaindns.md)[**do domínio**](c-organizationalunit.md)         |
| Classes Auxiliares           | [**Destinatário de email**](c-mailrecipient.md) (sistema)                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Atributos do Server 2003

Essa classe contém os seguintes atributos para Windows Server 2003:



| Atributo                                                                   | Obrigatório | Derivado de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informações adicionais**](a-notes.md)                                   | Falso     | **Contact**                                                                                                                            |
| [**Endereço**](a-streetaddress.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço -Home**](a-homepostaladdress.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Assistente**](a-assistant.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Comentário**](a-info.md)                                                   | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | Verdadeiro      | **Pessoa de** [ **contato**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código-país**](a-countrycode.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome do país**](a-c.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Divisão**](a-division.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Assinatura DSA**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de email**](a-mail.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID do funcionário**](a-employeeid.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificador de geração**](a-generationqualifier.md)                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome fornecido**](a-givenname.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciais**](a-initials.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidade-nome**](a-l.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-address**](a-mhsoraddress.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Categoria de objeto**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da organização**](a-o.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outra caixa de correio**](a-othermailbox.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outro nome**](a-middlename.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Título pessoal**](a-personaltitle.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Fax-outro**](a-otherfacsimiletelephonenumber.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-outro**](a-otherhomephone.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-principal**](a-homephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-outro**](a-otheripphone.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-primário**](a-ipphone.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-outro**](a-othermobile.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-primário**](a-mobile.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Office-outro**](a-othertelephone.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-outro**](a-otherpager.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-primário**](a-pager.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagem**](a-thumbnailphoto.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**caixa de Office**](a-postofficebox.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**secretário**](a-secretary.md)                                            | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte-também**](a-seealso.md)                                               | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Número de série**](a-serialnumber.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                         | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Estado-ou-província-nome**](a-st.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço da rua**](a-street.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sobrenome**](a-sn.md)                                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | [**Pessoa**](c-person.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primário**](a-primarytelexnumber.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto-país**](a-co.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                   | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuário**](a-usercert.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentário do usuário**](a-comment.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Usuário-senha**](a-userpassword.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Home Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço X121**](a-x121address.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado X509**](a-usercertificate.md)                                      | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Windows Conjuntos de propriedades do Server 2003

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2003:



| Nome comum                                            |
|--------------------------------------------------------|
| [**Informações pessoais**](r-personal-information.md) |
| [**Informações da Web**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Conjuntos de propriedades](#windows-server-2003-r2-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor ocultado padrão        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Possíveis superiores          | [**Unidade organizacional do DNS**](c-domaindns.md)[**do domínio**](c-organizationalunit.md)         |
| Classes Auxiliares           | [**Destinatário de email**](c-mailrecipient.md) (sistema)                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos do Server 2003 R2

Essa classe contém os seguintes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Obrigatório | Derivado de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informações adicionais**](a-notes.md)                                   | Falso     | **Contact**                                                                                                                            |
| [**Endereço**](a-streetaddress.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço -Home**](a-homepostaladdress.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição do administrador**](a-admindescription.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Assistente**](a-assistant.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome canônico**](a-canonicalname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Comentário**](a-info.md)                                                   | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | Verdadeiro      | **Pessoa de** [ **contato**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código do país**](a-countrycode.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome do país**](a-c.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição**](a-description.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Destino-indicador**](a-destinationindicator.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome de exibição**](a-displayname.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome de exibição-imprimível**](a-displaynameprintable.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Divisão**](a-division.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Email-endereços**](a-mail.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID do funcionário**](a-employeeid.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da extensão**](a-extensionname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Flags**](a-flags.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificador de geração**](a-generationqualifier.md)                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome fornecido**](a-givenname.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciais**](a-initials.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instância**](a-instancetype.md)                                     | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É excluído**](a-isdeleted.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último-pai conhecido**](a-lastknownparent.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidade-nome**](a-l.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mestre por**](a-masteredby.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-address**](a-mhsoraddress.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Obj-dist-Name**](a-distinguishedname.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoria**](a-objectcategory.md)                                 | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classe de objeto**](a-objectclass.md)                                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**GUID do objeto**](a-objectguid.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Versão do objeto**](a-objectversion.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome da unidade organizacional**](a-ou.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da organização**](a-o.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros-caixa de correio**](a-othermailbox.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outro nome**](a-middlename.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Título pessoal**](a-personaltitle.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Fax-outro**](a-otherfacsimiletelephonenumber.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-outro**](a-otherhomephone.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-principal**](a-homephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-outro**](a-otheripphone.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-primário**](a-ipphone.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-outro**](a-othermobile.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-primário**](a-mobile.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Office-outro**](a-othertelephone.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-outro**](a-otherpager.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-primário**](a-pager.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagem**](a-thumbnailphoto.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço postal**](a-postaladdress.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**caixa de Office**](a-postofficebox.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Consulta-política-BL**](a-querypolicybl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço registrado**](a-registeredaddress.md)                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Relatórios**](a-directreports.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Representantes-de**](a-repsfrom.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Revisão**](a-revision.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**secretário**](a-secretary.md)                                            | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte-também**](a-seealso.md)                                               | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Número de série**](a-serialnumber.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                         | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Estado-ou-província-nome**](a-st.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço da rua**](a-street.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sub-referências**](a-subrefs.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sobrenome**](a-sn.md)                                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Sinalizadores do sistema**](a-systemflags.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Número de telefone**](a-telephonenumber.md)                               | Falso     | [**Pessoa**](c-person.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-identificador de terminal**](a-teletexterminalidentifier.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-primário**](a-primarytelexnumber.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto-país**](a-co.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto-codificado ou endereço**](a-textencodedoraddress.md)                   | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuário**](a-usercert.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentário do usuário**](a-comment.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Usuário-senha**](a-userpassword.md)                                     | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Usuário-SMIME-certificado**](a-usersmimecertificate.md)                    | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-alterado**](a-usnchanged.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Criado pelo USN**](a-usncreated.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removido**](a-usndsalastobjremoved.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-entre sites**](a-usnintersite.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-fonte**](a-usnsource.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WBEM-caminho**](a-wbempath.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objetos bem conhecidos**](a-wellknownobjects.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando-alterado**](a-whenchanged.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando-criado**](a-whencreated.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-outro**](a-url.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**X121-endereço**](a-x121address.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Conjuntos de propriedades do servidor 2003 R2

essa classe contém os seguintes conjuntos de propriedades para o Windows Server 2003 R2:



| Nome comum                                            |
|--------------------------------------------------------|
| [**Pessoal-informações**](r-personal-information.md) |
| [**Web-informações**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Conjuntos de propriedades](#windows-server-2008-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Categoria de objeto-padrão     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Padrão-ocultando valor        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nome comum**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Superiores possíveis          | [**Domínio-**](c-domaindns.md)[**unidade organizacional** DNS](c-organizationalunit.md)         |
| Classes Auxiliares           | [**Destinatário de email**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                                                 |
| Descritor de segurança padrão | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos do servidor 2008

essa classe contém os seguintes atributos para o Windows Server 2008:



| Atributo                                                                      | Obrigatório | Derivado de                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informações adicionais**](a-notes.md)                                      | Falso     | **Contact**                                                                                                                            |
| [**Endereço**](a-streetaddress.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço -Home**](a-homepostaladdress.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição do administrador**](a-admindescription.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Assistente**](a-assistant.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome canônico**](a-canonicalname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Comentário**](a-info.md)                                                      | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                    | Verdadeiro      | **Pessoa de** [ **contato**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código-país**](a-countrycode.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome do país**](a-c.md)                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição**](a-description.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome de exibição**](a-displayname.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Divisão**](a-division.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Assinatura DSA**](a-dsasignature.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de email**](a-mail.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID do funcionário**](a-employeeid.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da extensão**](a-extensionname.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Sinalizadores**](a-flags.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Entrada de entrada**](a-fromentry.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificador de geração**](a-generationqualifier.md)                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome fornecido**](a-givenname.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciais**](a-initials.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instância**](a-instancetype.md)                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É excluído**](a-isdeleted.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                             | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último-pai conhecido**](a-lastknownparent.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                               | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidade-nome**](a-l.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mestre por**](a-masteredby.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-address**](a-mhsoraddress.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-userlink**](a-mscom-userlink.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-permitido-para-delegar para**](a-msds-allowedtodelegateto.md)             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-filho-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-HAB-senioridade-índice**](a-msds-habseniorityindex.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-full-Replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-is-partial-Replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Masterd-by**](a-msds-masteredby.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-cursores**](a-msds-ncreplcursors.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Neighbors-Bounds**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-repl-Bound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-fonética-Company-Name**](a-msds-phoneticcompanyname.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-fonético-Department**](a-msds-phoneticdepartment.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-principal-Name**](a-msds-principalname.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-aplicado**](a-msds-psoapplied.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-repl-Value-meta-data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-revelados-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-revelado-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Ms-Exch-Assistant-Name**](a-msexchassistantname.md)                        | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                               | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-membro de**](a-mssfu30posixmemberof.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Não Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Obj-dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoria**](a-objectcategory.md)                                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classe de objeto**](a-objectclass.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**GUID do objeto**](a-objectguid.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Versão do objeto**](a-objectversion.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome da unidade organizacional**](a-ou.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da organização**](a-o.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros-caixa de correio**](a-othermailbox.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outro nome**](a-middlename.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Título pessoal**](a-personaltitle.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Fax-outro**](a-otherfacsimiletelephonenumber.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-outro**](a-otherhomephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-principal**](a-homephone.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-outro**](a-otheripphone.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-primário**](a-ipphone.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-outro**](a-othermobile.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-primário**](a-mobile.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Office-outro**](a-othertelephone.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-outro**](a-otherpager.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-primário**](a-pager.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagem**](a-thumbnailphoto.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço postal**](a-postaladdress.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços proxy**](a-proxyaddresses.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço registrado**](a-registeredaddress.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Relatórios**](a-directreports.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Revisão**](a-revision.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**secretário**](a-secretary.md)                                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte também**](a-seealso.md)                                                  | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Número de série**](a-serialnumber.md)                                        | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                            | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço da rua**](a-street.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sub-refs**](a-subrefs.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sobrenome**](a-sn.md)                                                        | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Número de telefone**](a-telephonenumber.md)                                  | Falso     | [**Pessoa**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País de texto**](a-co.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                      | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado do usuário**](a-usercert.md)                                                | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentário do usuário**](a-comment.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Senha do usuário**](a-userpassword.md)                                        | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                       | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN alterado**](a-usnchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Criado por USN**](a-usncreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**UsN-Intersite**](a-usnintersite.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objetos conhecidos**](a-wellknownobjects.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando alterado**](a-whenchanged.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando criado**](a-whencreated.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Home Page**](a-wwwhomepage.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço X121**](a-x121address.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado X509**](a-usercertificate.md)                                         | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Windows Conjuntos de propriedades do Server 2008

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2008:



| Nome comum                                            |
|--------------------------------------------------------|
| [**Informações pessoais**](r-personal-information.md) |
| [**Informações da Web**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Conjuntos de propriedades](#windows-server-2008-r2-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor ocultado padrão        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Possíveis superiores          | [**Unidade organizacional do DNS**](c-domaindns.md)[**do domínio**](c-organizationalunit.md)         |
| Classes Auxiliares           | [**Destinatário de email**](c-mailrecipient.md) (sistema)                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos do Server 2008 R2

Essa classe contém os seguintes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Obrigatório | Derivado de                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informações adicionais**](a-notes.md)                                        | Falso     | **Contact**                                                                                                                            |
| [**Endereço**](a-streetaddress.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço -Home**](a-homepostaladdress.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição do administrador**](a-admindescription.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Assistente**](a-assistant.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome canônico**](a-canonicalname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Comentário**](a-info.md)                                                        | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                      | Verdadeiro      | **Pessoa de** [ **contato**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código-país**](a-countrycode.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome do país**](a-c.md)                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição**](a-description.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome de exibição**](a-displayname.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Divisão**](a-division.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Assinatura DSA**](a-dsasignature.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de email**](a-mail.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID do funcionário**](a-employeeid.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da extensão**](a-extensionname.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Sinalizadores**](a-flags.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Entrada de entrada**](a-fromentry.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Período de coleta de lixo**](a-garbagecollperiod.md)                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificador de geração**](a-generationqualifier.md)                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome determinado**](a-givenname.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciais**](a-initials.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instância**](a-instancetype.md)                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último pai conhecido**](a-lastknownparent.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Gerente**](a-manager.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS- LTD-Seniority-Index**](a-msds-habseniorityindex.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                         | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Categoria de objeto**](a-objectcategory.md)                                      | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classe de objeto**](a-objectclass.md)                                            | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Versão do objeto**](a-objectversion.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome da unidade organizacional**](a-ou.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da organização**](a-o.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outra caixa de correio**](a-othermailbox.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outro nome**](a-middlename.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Título pessoal**](a-personaltitle.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Fax-Other**](a-otherfacsimiletelephonenumber.md)                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-Other**](a-otherhomephone.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-Primary**](a-homephone.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-Other**](a-otheripphone.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-Primary**](a-ipphone.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Mobile-Other**](a-othermobile.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Mobile-Primary**](a-mobile.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Office-outro**](a-othertelephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-outro**](a-otherpager.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-primário**](a-pager.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagem**](a-thumbnailphoto.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço postal**](a-postaladdress.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**caixa de Office**](a-postofficebox.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Consulta-política-BL**](a-querypolicybl.md)                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço registrado**](a-registeredaddress.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-vector**](a-repluptodatevector.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Relatórios**](a-directreports.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Representantes-de**](a-repsfrom.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-to**](a-repsto.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Revisão**](a-revision.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SD-direitos-efetivos**](a-sdrightseffective.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**secretário**](a-secretary.md)                                                 | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte-também**](a-seealso.md)                                                    | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Número de série**](a-serialnumber.md)                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referência-BL**](a-serverreferencebl.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Mostrar catálogo de endereços**](a-showinaddressbook.md)                              | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar-in-avançado-somente exibição**](a-showinadvancedviewonly.md)                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Estado-ou-província-nome**](a-st.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço da rua**](a-street.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Classe de objeto estrutural**](a-structuralobjectclass.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sub-referências**](a-subrefs.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sobrenome**](a-sn.md)                                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Número de telefone**](a-telephonenumber.md)                                    | Falso     | [**Pessoa**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País de texto**](a-co.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado do usuário**](a-usercert.md)                                                  | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentário do usuário**](a-comment.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Senha do usuário**](a-userpassword.md)                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN alterado**](a-usnchanged.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Criado por USN**](a-usncreated.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**UsN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando alterado**](a-whenchanged.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando criado**](a-whencreated.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Home Page**](a-wwwhomepage.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço X121**](a-x121address.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado X509**](a-usercertificate.md)                                           | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Conjuntos de propriedades do Server 2008 R2

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2008 R2:



| Nome comum                                            |
|--------------------------------------------------------|
| [**Informações pessoais**](r-personal-information.md) |
| [**Informações da Web**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Conjuntos de propriedades](#windows-server-2012-property-sets)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Pessoa**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor ocultado padrão        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclasse de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Possíveis superiores          | [**Unidade organizacional do DNS**](c-domaindns.md)[**do domínio**](c-organizationalunit.md)         |
| Classes Auxiliares           | [**Destinatário de email**](c-mailrecipient.md) (sistema)                                           |
| Descritor de segurança NT      | O:BAG:BAD:S:                                                                                 |
| Descritor de segurança padrão | D:(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Essa classe contém os seguintes atributos para Windows Server 2012:



| Atributo                                                                                              | Obrigatório | Derivado de                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informações adicionais**](a-notes.md)                                                              | Falso     | **Contact**                                                                                                                            |
| [**Endereço**](a-streetaddress.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço -Home**](a-homepostaladdress.md)                                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição do administrador**](a-admindescription.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Assistente**](a-assistant.md)                                                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome canônico**](a-canonicalname.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Comentário**](a-info.md)                                                                              | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                                            | Verdadeiro      | **Pessoa de** [ **contato**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Início**](c-top.md)<br/> |
| [**Empresa**](a-company.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código-país**](a-countrycode.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome do país**](a-c.md)                                                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Criar carimbo de data/hora**](a-createtimestamp.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descrição**](a-description.md)                                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome de exibição**](a-displayname.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome de exibição imprimível**](a-displaynameprintable.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Divisão**](a-division.md)                                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-assinatura**](a-dsasignature.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Email-endereços**](a-mail.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID do funcionário**](a-employeeid.md)                                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da extensão**](a-extensionname.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de telefone**](a-facsimiletelephonenumber.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Flags**](a-flags.md)                                                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**FSMO-função-proprietário**](a-fsmoroleowner.md)                                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Lixo-Coll-period**](a-garbagecollperiod.md)                                                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificador de geração**](a-generationqualifier.md)                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome fornecido**](a-givenname.md)                                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciais**](a-initials.md)                                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instância**](a-instancetype.md)                                                                | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**É-crítico-System-Object**](a-iscriticalsystemobject.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É excluído**](a-isdeleted.md)                                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É com proprietário de privilégio**](a-isprivilegeholder.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**É reciclado**](a-isrecycled.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                                                     | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último-pai conhecido**](a-lastknownparent.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                                       | Falso     | [**Destinatário de email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidade-nome**](a-l.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos gerenciados**](a-managedobjects.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mestre por**](a-masteredby.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-address**](a-mhsoraddress.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar-carimbo de data/hora**](a-modifytimestamp.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Act-On-Behalf-of-Other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-GeoCoordinates-Altitude**](a-msds-geocoordinatesaltitude.md)                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-GeoCoordinates-Latitude**](a-msds-geocoordinateslatitude.md)                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-GeoCoordinates-Longitude**](a-msds-geocoordinateslongitude.md)                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS- LTD-Seniority-Index**](a-msds-habseniorityindex.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Full-Replica-for**](a-msds-isfullreplicafor.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Partial-Replica-for**](a-msds-ispartialreplicafor.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Tipo ms-DS-NC**](a-msds-nctype.md)                                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                                | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                                       | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                                               | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Categoria de objeto**](a-objectcategory.md)                                                            | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Classe de objeto**](a-objectclass.md)                                                                  | Verdadeiro      | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Versão do objeto**](a-objectversion.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Nome da unidade organizacional**](a-ou.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome da organização**](a-o.md)                                                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros-caixa de correio**](a-othermailbox.md)                                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outro nome**](a-middlename.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Outros objetos bem conhecidos**](a-otherwellknownobjects.md)                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Parcial-atributo-exclusão-lista**](a-partialattributedeletionlist.md)                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciais**](a-partialattributeset.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Título pessoal**](a-personaltitle.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Fax-outro**](a-otherfacsimiletelephonenumber.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-outro**](a-otherhomephone.md)                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Home-principal**](a-homephone.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-outro**](a-otheripphone.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Ip-primário**](a-ipphone.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-ISDN-primário**](a-primaryinternationalisdnnumber.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-outro**](a-othermobile.md)                                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-celular-primário**](a-mobile.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Office-outro**](a-othertelephone.md)                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-outro**](a-otherpager.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telefone-Pager-primário**](a-pager.md)                                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**físico-entrega-Office-Name**](a-physicaldeliveryofficename.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagem**](a-thumbnailphoto.md)                                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possíveis-inferiores**](a-possibleinferiors.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço postal**](a-postaladdress.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**caixa de Office**](a-postofficebox.md)                                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferencial-entrega-método**](a-preferreddeliverymethod.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nome-do-objeto-proxy**](a-proxiedobjectname.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereços de proxy**](a-proxyaddresses.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Consulta-política-BL**](a-querypolicybl.md)                                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço registrado**](a-registeredaddress.md)                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-meta-data**](a-replpropertymetadata.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Relatórios**](a-directreports.md)                                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Revisão**](a-revision.md)                                                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**secretário**](a-secretary.md)                                                                       | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte também**](a-seealso.md)                                                                          | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Número de série**](a-serialnumber.md)                                                                | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                                                    | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**State-or-Province-Name**](a-st.md)                                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Endereço da rua**](a-street.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sub-refs**](a-subrefs.md)                                                                          | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Sobrenome**](a-sn.md)                                                                                | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**Sinalizadores de sistema**](a-systemflags.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Número de telefone**](a-telephonenumber.md)                                                          | Falso     | [**Pessoa**](c-person.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País de texto**](a-co.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                                              | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado do usuário**](a-usercert.md)                                                                        | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentário do usuário**](a-comment.md)                                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Senha do usuário**](a-userpassword.md)                                                                | Falso     | [**Pessoa**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                               | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN alterado**](a-usnchanged.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Criado por USN**](a-usncreated.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**UsN-Intersite**](a-usnintersite.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                                                      | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando alterado**](a-whenchanged.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Quando criado**](a-whencreated.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Home Page**](a-wwwhomepage.md)                                                                 | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                                        | Falso     | [**Início**](c-top.md)<br/>                                                                                                        |
| [**Endereço X121**](a-x121address.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado X509**](a-usercertificate.md)                                                                 | Falso     | [**Destinatário do email**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Conjuntos de propriedades

Essa classe contém os seguintes conjuntos de propriedades para Windows Server 2012:



| Nome comum                                            |
|--------------------------------------------------------|
| [**Informações pessoais**](r-personal-information.md) |
| [**Informações da Web**](r-web-information.md)           |



 

 





