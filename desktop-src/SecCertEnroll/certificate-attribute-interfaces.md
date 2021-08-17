---
description: As interfaces a seguir podem ser usadas para criar atributos de certificado.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfaces de atributo de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63cbd7b5e80fbb787a0d2aadcfb1617cb7972d7eed200da9184607ad0598031e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902919"
---
# <a name="certificate-attribute-interfaces"></a>Interfaces de atributo de certificado

As interfaces a seguir podem ser usadas para criar atributos de certificado.



| Interface                                                                    | Descrição                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | Representa um atributo criptográfico em uma solicitação de certificado.                                                                              |
| [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | Gerencia uma coleção de [**objetos ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | Representa um atributo em uma solicitação de certificado PKCS \# 7, PKCS \# 10 ou CMC.                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | Representa um atributo que pode ser usado para identificar o cliente que gerou uma solicitação de certificado.                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | Representa as extensões de certificado em uma solicitação de certificado.                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | Representa um atributo que contém uma chave privada criptografada a ser arquivada por uma autoridade de certificação.                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | Representa um atributo que contém um hash SHA-1 da chave privada criptografada a ser arquivada por uma autoridade de certificação.                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | Representa um atributo que identifica o provedor criptográfico usado pela entidade que solicita o certificado.                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | Representa um atributo que contém informações de versão sobre o sistema operacional cliente no qual a solicitação de certificado foi gerada. |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | Representa um atributo que contém o certificado que está sendo renovado.                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | Gerencia uma coleção de [**objetos IX509Attribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | Representa um par nome-valor genérico.                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | Gerencia uma coleção de [**objetos IX509NameValuePair.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



