---
title: Mapeamento entre propriedades IADsUser e atributos do Active Directory
description: Quando aplicável, uma propriedade do objeto de usuário ADSI é mapeada para um atributo apropriado do Active Directory. As propriedades do objeto de usuário ADSI são associadas aos métodos de propriedade IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Mapeamento entre propriedades IADsUser e ADSI de atributos do Active Directory
- ADSI do provedor LDAP, objeto de usuário, Mapeamento entre as propriedades IADsUser e atributos do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e659c6325457b2654ad5cfeef964975949150232c4ae3376fac640c51c41aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839476"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Mapeamento entre propriedades IADsUser e atributos do Active Directory

Quando aplicável, uma propriedade do objeto de usuário ADSI é mapeada para um atributo apropriado do Active Directory. As propriedades do objeto de usuário ADSI são associadas aos métodos de propriedade [**IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser)

A tabela a seguir lista o mapeamento entre as [**propriedades IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) para o provedor LDAP e o atributo do Active Directory correspondente.



| Propriedade IADsUser                                           | Atributo do Active Directory                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **ADS \_ SinalizadorMENTE \_ ACCOUNTDISABLE** no [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Sem suporte.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Departamento**](iadsuser-property-methods.md)             | [**Departamento**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Descrição**](iadsuser-property-methods.md)            | [**Descrição**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Divisão**](iadsuser-property-methods.md)               | [**Divisão**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**Emailaddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**EmployeeID**](iadsuser-property-methods.md)             | [**Employeeid**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**FaxNumber**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**Nome**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**displayName**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Sem suporte.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Sem suporte.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Homepage**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**Lockouttime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Idiomas**](iadsuser-property-methods.md)              | Sem suporte.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**Sn**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Gerente**](iadsuser-property-methods.md)                | [**manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | Sem suporte.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Definir usando o Política de Grupo Editor                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Definir usando o Política de Grupo Editor                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **ADS \_ Sinalizador \_ \_ NOTREQD DE UF PASSWD** no [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol) |
| [**Imagem**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**CepCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Perfil**](iadsuser-property-methods.md)                | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Definir usando o Política de Grupo Editor                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**Móvel**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**Telephonenumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Título**](iadsuser-property-methods.md)                  | [**Título**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 