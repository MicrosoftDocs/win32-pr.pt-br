---
title: Mapeamento de tipo de dados entre Active Directory e LDAP
description: A tabela a seguir mapeia o nome de sintaxe amigável para a OID de sintaxe LDAP correspondente e o valor ADSTYPEENUM.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- mapeamento de tipo de dados entre Active Directory e ADSI LDAP
- ADSI do provedor de serviços LDAP, mapeamento de tipo de dados entre Active Directory e LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45157fb7cefe1a993e6e16dffe28f101bc73759b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754854"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Mapeamento de tipo de dados entre Active Directory e LDAP

A tabela a seguir mapeia o nome de sintaxe amigável para a OID de sintaxe LDAP correspondente e o valor [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) .



| Nome de sintaxe amigável              | OID de sintaxe LDAP               | Tipo de dados ADSTYPEENUM                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Áudio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| Binário                            | 1.3.6.1.4.1.1466.115.121.1.5  | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE \_ booliano**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **\_cadeia de \_ caracteres exata do caso de ADSTYPE \_**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Certificado                       | 1.3.6.1.4.1.1466.115.121.1.8  | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| País/Região                    | 1.3.6.1.4.1.1466.115.121.1.11 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Directorystring                   | 1.3.6.1.4.1.1466.115.121.1.15 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **\_cadeia de \_ caracteres DN ADSTYPE**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ \_ hora UTC**                |
| Tempo (somente o servidor do site faz isso) | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ \_ hora UTC**                |
| Guia                             | 1.3.6.1.4.1.1466.115.121.1.25 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **ADSTYPE \_ inteiro**                  |
| INTEGER8 (não está em LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **\_inteiro grande \_ ADSTYPE**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **\_cadeia de \_ caracteres numérica ADSTYPE**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Octetstring (não em RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| Imenablestring                   | 1.3.6.1.4.1.1466.115.121.1.44 | **\_cadeia de caracteres imprimível do ADSTYPE \_**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **\_ \_ descritor de segurança do ADSTYPE NT \_** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**     |
| UTCTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **ADSTYPE \_ \_ hora UTC**                |



 

 

 




