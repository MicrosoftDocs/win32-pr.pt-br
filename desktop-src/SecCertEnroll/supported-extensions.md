---
description: Você pode usar a interface IX509Extension para definir uma extensão arbitrária.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensões com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0362bc289e8f0631520a7d9d56ff4bed1af2c698c721db703b27b0ecee5a1629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101105"
---
# <a name="supported-extensions"></a>Extensões com suporte

Você pode usar a interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir uma extensão arbitrária. A API de Registro de Certificado também fornece interfaces derivadas de **IX509Extension** para permitir que você crie facilmente qualquer uma das extensões mais comuns. A lista a seguir identifica as extensões comuns com suporte das autoridades de certificação da Microsoft e os identificadores de objeto e interfaces que você pode usar para criar.

## <a name="alternativenames"></a>AlternativeNames

A extensão de nomes alternativos pode ser usada para definir um ou mais formulários de nome alternativos para o assunto da solicitação de certificado. Dentre os exemplos de formas alternativas incluem-se endereços de email, nomes DNS, endereços IP e URIs.

**Interface:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN \_ OID \_ SUBJECT ALT \_ \_ NAME2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

A extensão de acesso a informações de autoridade identifica como acessar informações e serviços de AC. O valor da extensão contém uma sequência de URIs.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ AUTHORITY INFO ACCESS \_ \_ (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

A extensão do identificador de chave de autoridade permite a identificação da chave pública da AC que corresponde à chave privada da AC que assinou um certificado emitido. Ele é usado pelo caminho do certificado criando software em um servidor Windows para encontrar o certificado de AC. Quando uma AC emite um certificado, o valor da extensão é definido como igual à extensão **SubjectKeyIdentifier** no certificado de assinatura da AC. O valor normalmente é um hash SHA-1 da chave pública.

**Interface:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** XCN \_ OID \_ AUTHORITY KEY \_ \_ IDENTIFIER2 (2.5.29.35)

## <a name="basicconstraints"></a>BasicConstraints

A extensão de restrições básicas pode ser usada para identificar se a entidade pode ser usada como uma AC (autoridade de certificação) e, nesse caso, o número de AAs subordinadas que podem existir abaixo dela na cadeia de certificados.

**Interface:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** RESTRIÇÕES \_ \_ \_ BÁSICAS XCN OID2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

A extensão de políticas de certificado pode ser usada para identificar as políticas sob as quais o certificado foi emitido e as finalidades para ele podem ser usadas. Eles são identificados por uma coleção de OIDs (identificadores de objeto). As políticas são personalizadas para os requisitos de uma organização.

**Interface:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** POLÍTICAS DE CERTIFICADO OID XCN \_ \_ \_ (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

A extensão de pontos de distribuição da CRL (lista de certificados revogados) contém o URI da CRL (lista de certificados revogados) base.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** PONTOS \_ DIST DA \_ CRL \_ OID XCN \_ (2.5.29.31)

## <a name="enhancedkeyusage"></a>EnhancedKeyUsage

A extensão de uso de chave aprimorada pode ser usada para definir um ou mais usos da chave pública contida no certificado.

**Interface:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** USO APRIMORADO DE CHAVE XCN \_ OID \_ \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

A extensão de CRL mais recente contém o URI da CRL delta. A mesma sintaxe ASN.1 é usada para essa extensão e a **extensão CrlDistributionPoints.**

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ FRESHEST \_ CRL (2.5.29.46)

## <a name="keyusage"></a>KeyUsage

A extensão de uso de chave pode ser usada para definir restrições nas operações que podem ser executadas pela chave pública contida no certificado. Por exemplo, você pode especificar que a chave pública seja usada apenas para criar uma assinatura digital, assinar uma CRL (lista de certificados revogados) ou criptografar outra chave.

**Interface:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** USO DE CHAVE OID XCN \_ \_ \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

A extensão de políticas de aplicativo da Microsoft pode ser usada por um aplicativo para filtrar certificados com base no uso permitido. Os usos permitidos são identificados por OIDs. Essa extensão é semelhante à **extensão EnhancedKeyUsage,** mas com semântica mais estrita aplicada à AC pai. A extensão é específica da Microsoft.

**Interface:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** POLÍTICAS \_ DE CERTIFICADO DE APLICATIVO XCN OID \_ \_ \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

A extensão de restrições de nome é usada para identificar o namespace no qual todos os nomes de assunto de certificados em uma hierarquia de certificados devem estar localizados. A extensão é usada somente em um certificado de AC.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** RESTRIÇÕES DE NOME OID XCN \_ \_ \_ (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

A extensão de restrições de política é adicionada aos certificados de autoridade de certificação para restringir a validação de caminho, proibindo o mapeamento de política ou exigindo que cada certificado na hierarquia contenha um identificador de política aceitável.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** RESTRIÇÕES DE POLÍTICA OID XCN \_ \_ \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

A extensão de mapeamentos de política é usada para identificar as políticas em uma AC subordinada que correspondem às políticas na AC em emissão. O valor da extensão contém uma sequência de mapeamentos de política de AC subordinada e ac de emissão representados por identificadores de objeto.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** MAPEAMENTOS DE POLÍTICA OID XCN \_ \_ \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

A extensão de período de uso da chave privada é usada para especificar um período de validade diferente para a chave privada do que para o certificado ao qual a chave está associada.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** PERÍODO DE USO DE PRIVATEKEY DO XCN \_ OID \_ \_ \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

A extensão de funcionalidades S/MIME (Secure/Multipurpose Internet Mail Extensions) pode ser usada para relatar os recursos de descriptografia de um destinatário de email ao remetente da mensagem de email para que o remetente possa escolher o algoritmo de criptografia mais seguro com suporte de ambas as partes. O valor da extensão contém uma coleção de OIDs de algoritmo de criptografia simétrica e uma força de criptografia opcional para cada um.

**Interface:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

A extensão de atributos de diretório da entidade pode ser usada para transmitir atributos de identificação, como a nacionalidade da entidade do certificado. O valor da extensão é uma sequência de pares de valores OID.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ SUBJECT DIR \_ \_ ATTRS (2.5.29.9)

## <a name="subjectkeyidentifier"></a>Subjectkeyidentifier

A extensão do identificador de chave de assunto pode ser usada para diferenciar entre várias chaves públicas mantidas pela pessoa do certificado. O valor da extensão é geralmente um hash SHA-1 da chave.

**Interface:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** XCN \_ OID \_ SUBJECT KEY \_ \_ IDENTIFIER (2.5.29.14)

## <a name="template"></a>Modelo

A extensão de modelo pode ser usada para identificar o modelo da versão 2 a ser usado ao emissão ou renovação de um certificado. O valor da extensão contém o OID do modelo e as informações de versão opcionais. A extensão é específica da Microsoft.

**Interface:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** MODELO DE CERTIFICADO OID XCN \_ \_ \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>Templatename

A extensão de nome de modelo pode ser usada para identificar o modelo da versão 1 a ser usado ao emmissão ou renovação de um certificado. O valor da extensão contém o nome do modelo. A extensão é específica da Microsoft.

**Interface:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** \_ \_ \_ Extensão certtype de registro \_ do XCN OID (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Extensões](extensions.md)
</dt> </dl>

 

 



