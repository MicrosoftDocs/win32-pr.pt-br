---
description: A API de Registro de Certificado dá suporte aos seguintes atributos. Você pode criar um atributo individual usando a interface correspondente identificada em cada uma das seções a seguir.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Atributos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8c7945113e764d835a685251adaec9149527b2d8f2d535a5dd24f26a5623bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774409"
---
# <a name="supported-attributes"></a>Atributos com suporte

A API de Registro de Certificado dá suporte aos seguintes atributos. Você pode criar um atributo individual usando a interface correspondente identificada em cada uma das seções a seguir.

## <a name="clientid"></a>ClientId

A interface [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) pode ser usada para definir um atributo que contém informações sobre o computador cliente que enviou a solicitação de certificado. As informações podem ser usadas para diagnóstico.

**Aplica-se a:** Solicitação PKCS \# 10 ou CMC.

**OID:** XCN \_ OID \_ REQUEST CLIENT INFO \_ \_ (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Extensões

A interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) pode ser usada para definir um conjunto de extensões de certificado X.509 versão 3. Há suporte para as extensões a seguir. Para obter mais informações, consulte o tópico Interfaces de extensão.



| Extensão              | Descrição                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | Contém uma ou mais formas de nome alternativos do emissor associado ao certificado.                                                                                                                                       |
| AuthorityKeyIdentifier | Contém um identificador de chave exclusivo para diferenciar entre várias chaves de assinatura de certificado da AC [*(autoridade de certificação).*](/windows/desktop/SecGloss/c-gly) |
| BasicConstraints       | Indica se o assunto pode agir como uma AC.                                                                                                                                                                                   |
| CertificatePolicies    | Identifica as políticas e as informações de qualificador opcionais associadas ao certificado.                                                                                                                                      |
| MSApplicationPolicies  | Identifica um ou mais usos para o certificado. Essa extensão é semelhante à extensão EnhancedKeyUsage, mas é definida pela Microsoft.                                                                                           |
| EnhancedKeyUsage       | Identifica um ou mais usos da chave pública contida no certificado. A extensão de uso de chave aprimorada pode ser usada além ou no lugar da extensão de uso de chave.                                                  |
| KeyUsage               | Identifica restrições nas operações que podem ser executadas pela chave pública contida no certificado.                                                                                                                  |
| SmimeCapabilities      | Relata os recursos de descriptografia de um destinatário de email para o remetente do email para permitir que o remetente escolha o algoritmo simétrico mais seguro com suporte de ambas as partes.                                                      |
| Subjectkeyidentifier   | Contém um identificador de chave exclusivo que pode ser usado para diferenciar entre várias chaves de assinatura associadas ao proprietário do certificado.                                                                                          |
| Modelo               | Identifica o modelo a ser usado ao emissão ou renovação de um certificado. A extensão contém o OID (identificador de objeto) do modelo.                                                                                       |
| Templatename           | Identifica o modelo a ser usado ao emissão ou renovação de um certificado. A extensão contém o nome do modelo.                                                                                                          |



 

**Aplica-se a:** Solicitação PKCS \# 10.

**OID:** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>ArchiveKey

A interface [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) pode ser usada para definir um atributo que contém uma chave privada criptografada enviada a uma AC para arquivamento.

**Aplica-se a:** Solicitação do CMC.

**OID:** XCN \_ OID \_ ARCHIVED \_ KEY \_ ATTR (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>ArchiveKeyHash

A interface [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) pode ser usada para definir um hash da chave privada contida no atributo **ArchiveKey.**

**Aplica-se a:** Solicitação do CMC.

**OID:** \_XCN OID \_ ENCRYPTED \_ KEY HASH \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>CspProvider

A interface [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) pode ser usada para definir um atributo que contém informações sobre o CSP [*(provedor*](/windows/desktop/SecGloss/c-gly) de serviços de criptografia) usado pelo solicitante para operações criptográficas.

**Aplica-se a:** Solicitação PKCS \# 10. Esse atributo é criado automaticamente quando você cria um [**objeto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)

**OID:** PROVEDOR \_ CSP DE REGISTRO XCN OID \_ \_ \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

A interface [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) pode ser usada para criar um atributo que contém informações de versão sobre o sistema operacional cliente. As informações podem ser usadas pela AC para determinar o tipo de processamento a ser aplicado ao criar o certificado.

**Aplica-se a:** Solicitação PKCS \# 10 ou CMC.

**OID:** VERSÃO \_ DO SISTEMA OPERACIONAL XCN OID \_ \_ (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>RenewalCertificate

A interface [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) pode ser usada para criar um atributo que contém o certificado que está sendo renovado.

**Aplica-se a:** Solicitação PKCS \# 10. Esse atributo será criado automaticamente se você criar uma solicitação PKCS 10 iniciando-a \# com o certificado sendo renovado.

**OID:** CERTIFICADO \_ DE RENOVAÇÃO OID XCN \_ \_ (1.3.6.1.4.1.311.13.1)

 

 
