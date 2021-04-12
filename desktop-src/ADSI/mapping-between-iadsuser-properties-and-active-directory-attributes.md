---
title: Mapeamento entre propriedades de IADsUser e atributos de Active Directory
description: Quando aplicável, uma propriedade do objeto de usuário ADSI é mapeada para um atributo de Active Directory apropriado. As propriedades do objeto usuário ADSI são associadas aos métodos de propriedade IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Mapeamento entre as propriedades IADsUser e os atributos de Active Directory ADSI
- Provedor LDAP ADSI, objeto de usuário, mapeamento entre Propriedades IADsUser e atributos de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b817a8c56e2c74c846e1343e0ed7803427f4a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366711"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Mapeamento entre propriedades de IADsUser e atributos de Active Directory

Quando aplicável, uma propriedade do objeto de usuário ADSI é mapeada para um atributo de Active Directory apropriado. As propriedades do objeto usuário ADSI são associadas aos métodos de propriedade [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

A tabela a seguir lista o mapeamento entre as propriedades [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) para o provedor LDAP e o atributo de Active Directory correspondente.



| Propriedade IADsUser                                           | Active Directory atributo                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **Anúncios \_ do UF \_ ACCOUNTDISABLE** Flag no atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Sem suporte.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Inteiros**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Descrição**](iadsuser-property-methods.md)            | [**ndescrição**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Divisão**](iadsuser-property-methods.md)               | [**Divisão**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**Funcionário**](iadsuser-property-methods.md)             | [**Funcionário**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**FaxNumber**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**displayName**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Sem suporte.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Sem suporte.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Principal**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Idiomas**](iadsuser-property-methods.md)              | Sem suporte.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**SN**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userestações de trabalho**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Manager**](iadsuser-property-methods.md)                | [**Manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | Sem suporte.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**Outro**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Definir usando o editor de Política de Grupo                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Definir usando o editor de Política de Grupo                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **Anúncios \_ do O sinalizador UF \_ passwd \_ NOTREQD** no atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) . |
| [**Imagem**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**PostalCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Perfil**](iadsuser-property-methods.md)                | [**profilepath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Definir usando o editor de Política de Grupo                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**móveis**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**pager**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Título**](iadsuser-property-methods.md)                  | [**título**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 