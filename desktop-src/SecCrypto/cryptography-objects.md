---
description: Lista os objetos fornecidos pelo CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Objetos de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370643"
---
# <a name="cryptography-objects"></a>Objetos de criptografia

Os objetos de criptografia são categorizados de acordo com o uso da seguinte maneira:

-   [Objetos de repositório de certificados](#certificate-store-objects)
-   [Objetos de assinatura digital](#digital-signature-objects)
-   [Objetos de dados de envelope](#enveloped-data-objects)
-   [Objetos de criptografia de dados](#data-encryption-objects)
-   [Objetos auxiliares](#auxiliary-objects)
-   [Objetos de registro de certificado](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a>Objetos de repositório de certificados

Os objetos a seguir funcionam com [*repositórios de certificados*](../secgloss/c-gly.md) e os certificados nesses armazenamentos. O CAPICOM dá suporte ao uso do usuário atual, do computador local, da memória e dos repositórios de certificados Active Directory.



| Objeto                                             | Descrição                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificate**](certificate.md)                 | Um único certificado digital.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Uma coleção de objetos [**PolicyInformation**](policyinformation.md) .                                                 |
| [**Certificados**](certificates.md)               | Coleção de objetos de [**certificado**](certificate.md) .                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fornece informações de status sobre um certificado.                                                                           |
| [**Cadeia**](chain.md)                             | Cria e verifica uma cadeia de validação de certificado com base em um certificado digital.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Representa uma coleção de objetos [**Extended**](extendedproperty.md) .                                        |
| [**ExtendedProperty**](extendedproperties.md)     | Representa uma propriedade estendida da Microsoft.                                                                               |
| [**Extensão**](extension.md)                     | Representa uma única extensão de certificado.                                                                              |
| [**Extensões**](extensions.md)                   | Representa uma coleção de objetos de [**extensão**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Representa uma chave privada.                                                                                               |
| [**PublicKey**](publickey.md)                     | Representa uma chave pública em um objeto de [**certificado**](certificate.md) .                                                 |
| [**Repositório**](store.md)                             | Fornece as propriedades e os métodos para escolher, gerenciar e usar os repositórios de certificados e os certificados nesses armazenamentos. |
| [**Modelo**](template.md)                       | Representa o modelo de extensão de certificado do certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de assinatura digital

Os objetos a seguir são exportados para assinar dados digitalmente e para verificar assinaturas digitais.



| Objeto                           | Descrição                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Objeto usado para assinar o código com uma assinatura digital Authenticode e verificar a assinatura no código assinado. |
| [**SignedData**](signeddata.md) | Objeto usado para assinar dados e verificar a assinatura em dados assinados.                                        |
| [**Signatário**](signer.md)         | Informações sobre um único signatário de dados, incluindo o certificado do signatário.                                    |
| [**Signatários**](signers.md)       | Coleção de objetos de [**signatário**](signer.md) .                                                             |



 

## <a name="enveloped-data-objects"></a>Objetos de dados de envelope

Os seguintes objetos são exportados para criar mensagens de dados envelopadas para privacidade e para descriptografar dados em mensagens envelopadas.



| Objeto                                 | Descrição                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Objetos usados para criar, enviar e receber dados de envelopes. Os dados de envelope são criptografados para que somente os destinatários pretendidos possam descriptografá-los. |
| [**Destinatários**](recipients.md)       | Coleção dos objetos de [**certificado**](certificate.md) dos destinatários pretendidos de uma mensagem envelopada.                           |



 

## <a name="data-encryption-objects"></a>Objetos de criptografia de dados

O objeto a seguir é exportado para criptografar dados arbitrários para privacidade e para descriptografar dados criptografados.



| Objeto                                 | Descrição                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**EncryptedData**](encrypteddata.md) | Objetos usados para criptografar dados. Os dados criptografados em um objeto [**EncryptedData**](encrypteddata.md) podem ser descriptografados. |



 

## <a name="auxiliary-objects"></a>Objetos auxiliares

Os objetos a seguir são exportados para alterar os comportamentos padrão de outros objetos e para gerenciar certificados, repositórios de certificados e mensagens.



| Objeto                                         | Descrição                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](algorithm.md)                 | Define o algoritmo e o [*comprimento da chave*](../secgloss/k-gly.md) a serem usados em operações criptográficas. |
| [**Atributo**](attribute.md)                 | Fornece uma única parte das informações adicionadas sobre uma assinatura, como a hora da assinatura.                                                    |
| [**Atributos**](attributes.md)               | Coleção de objetos de [**atributo**](attribute.md) .                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Fornece acesso somente leitura a restrições básicas sobre os usos de um certificado.                                                                    |
| [**EKU**](eku.md)                             | Fornece acesso às propriedades EKU de certificados.                                                                                              |
| [**EKUs**](ekus.md)                           | Coleção de objetos [**EKU**](eku.md) .                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Representa um bloco de dados codificados.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Fornece acesso somente leitura às propriedades de uso estendido de chave de certificados.                                                                 |
| [**HashedData**](hasheddata.md)               | Fornece a funcionalidade para aplicar um algoritmo de hash a uma cadeia de caracteres.                                                                               |
| [**Uso de**](keyusage.md)                   | Fornece acesso somente leitura às principais propriedades de uso de certificados.                                                                              |
| [**NoticeNumbers**](noticenumbers.md)         | Representa uma coleção de objetos de [**extensão**](extension.md) .                                                                              |
| [**OIDs**](oid.md)                             | Representa um identificador de objeto que é usado por várias propriedades capicor.                                                                     |
| [**OID**](oids.md)                           | Representa uma coleção de objetos [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fornece acesso aos OIDs de política de uma extensão.                                                                                             |
| [**Qualificador**](qualifier.md)                 | Representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.                                                           |
| [**Qualificadores**](qualifiers.md)               | Representa uma coleção de qualificadores.                                                                                                          |
| [**Configurações**](settings.md)                   | Habilita ou desabilita as caixas de diálogo para solicitar a identidade do assinante ou do remetente se essa identidade não for especificada.                                     |
| [**Utilitários**](utilities.md)                 | Fornece funcionalidade para tarefas comuns.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Objetos de registro de certificado

O objeto a seguir é usado para registro de certificado.



| Objeto                     | Descrição                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objeto que representa o controle de registro de certificado. Ele é usado principalmente na programação em Visual Basic ou em outra linguagem de automação. |



 

 

 
