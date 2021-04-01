---
description: Você pode usar a interface IX509Extension para definir uma extensão arbitrária.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensões com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647315"
---
# <a name="supported-extensions"></a>Extensões com suporte

Você pode usar a interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir uma extensão arbitrária. A API de registro de certificado também fornece interfaces derivadas de **IX509Extension** para permitir que você crie facilmente qualquer uma das extensões mais comuns. A lista a seguir identifica as extensões comuns com suporte pelas autoridades de certificação da Microsoft e os identificadores de objeto e as interfaces que você pode usar para criá-las.

## <a name="alternativenames"></a>Alternativos

A extensão de nomes alternativos pode ser usada para definir um ou mais formulários de nome alternativo para o assunto da solicitação de certificado. Dentre os exemplos de formas alternativas incluem-se endereços de email, nomes DNS, endereços IP e URIs.

**Interface:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN \_ OID \_ Subject \_ ALT \_ nome2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

A extensão de acesso a informações de autoridade identifica como acessar informações e serviços de autoridade de certificação. O valor da extensão contém uma sequência de URIs.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ Authority \_ info \_ Access (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

A extensão do identificador de chave de autoridade permite a identificação da chave pública da CA que corresponde à chave privada da AC que assinou um certificado emitido. Ele é usado pelo caminho de certificado que cria software em um Windows Server para localizar o certificado de autoridade de certificação. Quando uma CA emite um certificado, o valor da extensão é definido como igual à extensão **SubjectKeyIdentifier** no certificado de autenticação da autoridade de certificação. O valor normalmente é um hash SHA-1 da chave pública.

**Interface:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** \_ \_ 2.5.29.35 (XCN OID Authority \_ Key \_ IDENTIFIER2)

## <a name="basicconstraints"></a>BasicConstraints

A extensão de restrições básicas pode ser usada para identificar se a entidade pode ser usada como uma autoridade de certificação (CA) e, em caso afirmativo, o número de CAs subordinadas que podem existir abaixo dela na cadeia de certificados.

**Interface:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** XCN \_ OID \_ básico \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

A extensão de políticas de certificado pode ser usada para identificar as políticas sob as quais o certificado foi emitido e os fins para ele podem ser usados. Elas são identificadas por uma coleção de identificadores de objeto (OIDs). As políticas são personalizadas para os requisitos de uma organização.

**Interface:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** \_ \_ \_ Políticas de certificado de OID XCN (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

A extensão dos pontos de distribuição da CRL (lista de certificados revogados) contém o URI da CRL (lista de certificados revogados) base.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ CRL \_ dist \_ Points (2.5.29.31)

## <a name="enhancedkeyusage"></a>EnhancedKeyUsage

A extensão uso avançado de chave pode ser usada para definir um ou mais usos da chave pública contida no certificado.

**Interface:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** XCN \_ OID \_ Enhanced \_ Key \_ Usage (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

A extensão de CRL mais recente contém o URI da CRL delta. A mesma sintaxe ASN. 1 é usada para essa extensão e a extensão **CrlDistributionPoints** .

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_CRL mais \_ recente do XCN OID \_ (2.5.29.46)

## <a name="keyusage"></a>Uso de

A extensão de uso de chave pode ser usada para definir restrições nas operações que podem ser executadas pela chave pública contida no certificado. Por exemplo, você pode especificar que a chave pública seja usada somente para criar uma assinatura digital, assinar uma CRL (lista de certificados revogados) ou criptografar outra chave.

**Interface:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** \_Uso da \_ chave de OID XCN \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

A extensão de políticas de aplicativo da Microsoft pode ser usada por um aplicativo para filtrar certificados com base no uso permitido. Os usos permitidos são identificados pelos OIDs. Essa extensão é semelhante à extensão **EnhancedKeyUsage** , mas com semântica mais estrita aplicada à autoridade de certificação pai. A extensão é específica da Microsoft.

**Interface:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** \_ \_ \_ Políticas de certificado de aplicativo XCN OID \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

A extensão de restrições de nome é usada para identificar o namespace no qual todos os nomes de entidade de certificados em uma hierarquia de certificado devem ser localizados. A extensão é usada somente em um certificado de AC.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_ \_ \_ Restrições de nome de OID XCN (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

A extensão de restrições de política é adicionada aos certificados de autoridade de certificação para restringir a validação de caminho, proibindo o mapeamento de política ou exigindo que cada certificado na hierarquia contenha um identificador de política aceitável.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_ \_ \_ Restrições de política de OID XCN (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

A extensão de mapeamentos de política é usada para identificar as políticas em uma autoridade de certificação subordinada que correspondem às políticas na AC emissora. O valor de extensão contém uma sequência de emissão de CA e mapeamentos de política de autoridade de certificação subordinados representados por identificadores de objeto.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_ \_ \_ Mapeamentos de política de OID XCN (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

A extensão do período de uso de chave privada é usada para especificar um período de validade diferente para a chave privada do que para o certificado ao qual a chave está associada.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_ \_ \_ Período de uso do XCN OID PRIVATEKEY \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

A extensão de recursos de extensões S/MIME (Internet Mail Extensions) segura/multipropósito pode ser usada para relatar os recursos de descriptografia de um destinatário de email ao remetente da mensagem de email para que o remetente possa escolher o algoritmo de criptografia mais seguro com suporte de ambas as partes. O valor de extensão contém uma coleção de OIDs de algoritmo de criptografia simétrica e um nível de criptografia opcional para cada um.

**Interface:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

A extensão de atributos de diretório de assunto pode ser usada para transmitir atributos de identificação, como a nacionalidade da entidade do certificado. O valor da extensão é uma sequência de pares de valores OID.

**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ Subject \_ dir \_ ATTRS (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

A extensão do identificador de chave da entidade pode ser usada para diferenciar várias chaves públicas mantidas pela entidade do certificado. O valor da extensão é geralmente um hash SHA-1 da chave.

**Interface:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** \_ \_ \_ Identificador de chave de entidade XCN OID \_ (2.5.29.14)

## <a name="template"></a>Modelo

A extensão do modelo pode ser usada para identificar o modelo da versão 2 a ser usado ao emitir ou renovar um certificado. O valor da extensão contém a OID do modelo e as informações de versão opcionais. A extensão é específica da Microsoft.

**Interface:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** \_ \_ Modelo de certificado OID XCN \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

A extensão do nome do modelo pode ser usada para identificar o modelo da versão 1 a ser usado ao emitir ou renovar um certificado. O valor da extensão contém o nome do modelo. A extensão é específica da Microsoft.

**Interface:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** \_ \_ \_ Extensão certtype de registro \_ do XCN OID (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Extensões](extensions.md)
</dt> </dl>

 

 



