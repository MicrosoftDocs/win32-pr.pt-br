---
title: classe de objeto ms-DS-vinculável
description: Classe auxiliar para representar um objeto vinculável. Qualquer classe definida pelo usuário que representa uma entidade que pode ser usada para associar ao diretório (ou seja, um usuário) deve incluir essa classe auxiliar.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- ms-DS-vinculável-esquema de classe de objeto do AD
- Esquema de AD da classe do msDS-Vinculobject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b702a26c61920f5a3868ccc479b1f8578a3075907b5dc5bc2eb9d070321c91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680776"
---
# <a name="ms-ds-bindable-object-class"></a>classe de objeto ms-DS-vinculável

Classe auxiliar para representar um objeto vinculável. Qualquer classe definida pelo usuário que representa uma entidade que pode ser usada para associar ao diretório (ou seja, um usuário) deve incluir essa classe auxiliar.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-Vinculed-Object                |
| LDAP-Display-Name | msDS-Acopláobject                  |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Schema-ID-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementações

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)



| Entrada | Valor |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | Falso                                                        |
| Object-Category             | 3                                                            |
| Categoria de objeto-padrão     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Padrão-ocultando valor        | 1                                                            |
| RDN-ATT-ID                  | \-                                                           |
| Subclasse de                 | [**Segurança-principal**](c-securityprincipal.md)<br/> |
| Superiores possíveis          | \-                                                           |
| Classes Auxiliares           | \-                                                           |
| NT-Security-Descriptor      | O:BAG: INADEQUADO: S:                                                 |
| Descritor de segurança padrão | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Atributos do ADAM

Essa classe contém os seguintes atributos para ADAM:



| Atributo                                                                                      | Obrigatório | Derivado de                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Conta-expira**](a-accountexpires.md)                                                    | Falso     | **ms-DS-Vinculed-Object**                                                                    |
| [**Descrição do administrador**](a-admindescription.md)                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Administração – nome de exibição**](a-admindisplayname.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-atributos-efetivos**](a-allowedattributeseffective.md)                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classes filho permitidas**](a-allowedchildclasses.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Permitido-filho-classes-efetivas**](a-allowedchildclasseseffective.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Má-hora-senha**](a-badpasswordtime.md)                                                 | Falso     | **ms-DS-Vinculed-Object**                                                                    |
| [**Má-pwd-Count**](a-badpwdcount.md)                                                         | Falso     | **ms-DS-Vinculed-Object**                                                                    |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome canônico**](a-canonicalname.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome comum**](a-cn.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criação-carimbo de data/hora**](a-createtimestamp.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Descrição**](a-description.md)                                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Nome de exibição**](a-displayname.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DSA-assinatura**](a-dsasignature.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**DS-Core-propagação-data**](a-dscorepropagationdata.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Tipo de instância**](a-instancetype.md)                                                        | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Último pai conhecido**](a-lastknownparent.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Last-Logon-Timestamp**](a-lastlogontimestamp.md)                                           | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Tempo de bloqueio**](a-lockouttime.md)                                                          | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Objetos gerenciados**](a-managedobjects.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Modificar carimbo de data/hora**](a-modifytimestamp.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**ms-DS-User-Account-Auto-Locked**](a-ms-ds-useraccountautolocked.md)                        | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)            | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Disabled**](a-msds-useraccountdisabled.md)                              | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Dont-Expire-Password**](a-msds-userdontexpirepassword.md)                       | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Encrypted-Text-Password-Allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Expired**](a-msds-userpasswordexpired.md)                              | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Not-Required**](a-ms-ds-userpasswordnotrequired.md)                    | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Nt-Pwd-History**](a-ntpwdhistory.md)                                                       | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Descritor de segurança NT**](a-ntsecuritydescriptor.md)                                       | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Categoria de objeto**](a-objectcategory.md)                                                    | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Classe de objeto**](a-objectclass.md)                                                          | Verdadeiro      | [**Início**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sid de objeto**](a-objectsid.md)                                                              | Verdadeiro      | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Versão do objeto**](a-objectversion.md)                                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Outros objetos conhecidos**](a-otherwellknownobjects.md)                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parcial**](a-partialattributeset.md)                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Possíveis inferiores**](a-possibleinferiors.md)                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Endereços proxy**](a-proxyaddresses.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Pwd-Last-Set**](a-pwdlastset.md)                                                           | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                           | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Revisão**](a-revision.md)                                                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                 | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Classe Structural-Object**](a-structuralobjectclass.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Sub-refs**](a-subrefs.md)                                                                  | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Credenciais complementares**](a-supplementalcredentials.md)                                  | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Sinalizadores de sistema**](a-systemflags.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Grupos de tokens**](a-tokengroups.md)                                                          | Falso     | [**Entidade de segurança**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-Pwd**](a-unicodepwd.md)                                                            | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**USN alterado**](a-usnchanged.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Criado por USN**](a-usncreated.md)                                                            | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                     | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**UsN-Intersite**](a-usnintersite.md)                                                        | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                    | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                                              | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Objetos conhecidos**](a-wellknownobjects.md)                                               | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando alterado**](a-whenchanged.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**Quando criado**](a-whencreated.md)                                                          | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Home Page**](a-wwwhomepage.md)                                                         | Falso     | [**Início**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                                                | Falso     | [**Início**](c-top.md)<br/>                                                              |



 

 





