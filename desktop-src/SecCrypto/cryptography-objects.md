---
description: Lista os objetos fornecidos pelo CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Objetos de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff5e9495d64c38272bac54ffac03d1d087b9286887b4e4e520c6a447765efac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768368"
---
# <a name="cryptography-objects"></a>Objetos de criptografia

Os objetos de criptografia são categorizados de acordo com o uso da seguinte forma:

-   [Objetos do Armazenamento de Certificados](#certificate-store-objects)
-   [Objetos de assinatura digital](#digital-signature-objects)
-   [Objetos de dados envelhados](#enveloped-data-objects)
-   [Objetos de criptografia de dados](#data-encryption-objects)
-   [Objetos auxiliares](#auxiliary-objects)
-   [Objetos de registro de certificado](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a>Objetos do Armazenamento de Certificados

Os objetos a seguir funcionam [*com os armazenamentos de*](../secgloss/c-gly.md) certificados e os certificados nesses armazenamentos. O CAPICOM dá suporte ao uso de armazenamentos de certificados do Active Directory, da máquina local, da memória e do Usuário Atual.



| Objeto                                             | Descrição                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificado**](certificate.md)                 | Um único certificado digital.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Uma coleção de [**objetos PolicyInformation.**](policyinformation.md)                                                 |
| [**Certificados**](certificates.md)               | Coleção de [**objetos certificate.**](certificate.md)                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fornece informações de status sobre um certificado.                                                                           |
| [**Cadeia**](chain.md)                             | Cria e verifica uma cadeia de validação de certificado com base em um certificado digital.                                       |
| [**Extendedproperties**](extendedproperties.md)   | Representa uma coleção de [**objetos ExtendedProperty.**](extendedproperty.md)                                        |
| [**Extendedproperty**](extendedproperties.md)     | Representa uma propriedade estendida da Microsoft.                                                                               |
| [**Extensão**](extension.md)                     | Representa uma única extensão de certificado.                                                                              |
| [**Extensões**](extensions.md)                   | Representa uma coleção de objetos [**Extension.**](extension.md)                                                      |
| [**Privatekey**](privatekey.md)                   | Representa uma chave privada.                                                                                               |
| [**Publickey**](publickey.md)                     | Representa uma chave pública em um [**objeto Certificate.**](certificate.md)                                                 |
| [**Store**](store.md)                             | Fornece as propriedades e os métodos para escolher, gerenciar e usar os armazenamentos de certificados e os certificados nesses armazenamentos. |
| [**Modelo**](template.md)                       | Representa o modelo de extensão de certificado do certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de assinatura digital

Os objetos a seguir são exportados para assinar dados digitalmente e verificar assinaturas digitais.



| Objeto                           | Descrição                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Objeto usado para assinar código com uma assinatura digital Authenticode e verificar a assinatura no código assinado. |
| [**SignedData**](signeddata.md) | Objeto usado para assinar dados e verificar a assinatura em dados assinados.                                        |
| [**Signatário**](signer.md)         | Informações sobre um único signante de dados, incluindo o certificado do signante.                                    |
| [**Signatários**](signers.md)       | Coleção de [**objetos Signer.**](signer.md)                                                             |



 

## <a name="enveloped-data-objects"></a>Objetos de dados envelhados

Os objetos a seguir são exportados para criar mensagens de dados enveloadas para privacidade e descriptografar dados em mensagens enveloadas.



| Objeto                                 | Descrição                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Objetos usados para criar, enviar e receber dados envelopes. Os dados envelotados são criptografados para que somente os destinatários pretendido possam descriptografá-los. |
| [**Destinatários**](recipients.md)       | Coleção dos [**objetos De**](certificate.md) certificado dos destinatários pretendido de uma mensagem envelocada.                           |



 

## <a name="data-encryption-objects"></a>Objetos de criptografia de dados

O objeto a seguir é exportado para criptografar dados arbitrários para privacidade e descriptografar dados criptografados.



| Objeto                                 | Descrição                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Encrypteddata**](encrypteddata.md) | Objetos usados para criptografar dados. Os dados criptografados em [**um objeto EncryptedData**](encrypteddata.md) podem ser descriptografados. |



 

## <a name="auxiliary-objects"></a>Objetos auxiliares

Os objetos a seguir são exportados para alterar comportamentos padrão de outros objetos e gerenciar certificados, armazenamentos de certificados e mensagens.



| Objeto                                         | Descrição                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](algorithm.md)                 | Define o algoritmo e [*o comprimento da chave*](../secgloss/k-gly.md) a serem usados em operações criptográficas. |
| [**Atributo**](attribute.md)                 | Fornece uma única parte das informações adicionadas sobre uma assinatura, como a hora da assinatura.                                                    |
| [**Atributos**](attributes.md)               | Coleção de [**objetos Attribute.**](attribute.md)                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Fornece acesso somente leitura a restrições básicas sobre os usos de um certificado.                                                                    |
| [**EKU**](eku.md)                             | Fornece acesso às propriedades de EKU de certificados.                                                                                              |
| [**EKUs**](ekus.md)                           | Coleção de [**objetos EKU.**](eku.md)                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Representa um bloco de dados codificados.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Fornece acesso somente leitura às propriedades de uso estendido de chave de certificados.                                                                 |
| [**HashedData**](hasheddata.md)               | Fornece funcionalidade para aplicar um algoritmo de hash a uma cadeia de caracteres.                                                                               |
| [**KeyUsage**](keyusage.md)                   | Fornece acesso somente leitura às propriedades de uso de chave de certificados.                                                                              |
| [**NoticeNumbers**](noticenumbers.md)         | Representa uma coleção de objetos [**Extension.**](extension.md)                                                                              |
| [**Oid**](oid.md)                             | Representa um identificador de objeto que é usado por várias propriedades CAPICOM.                                                                     |
| [**OIDs**](oids.md)                           | Representa uma coleção de [**objetos OID.**](oid.md)                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fornece acesso aos OIDs de política de uma extensão.                                                                                             |
| [**Qualificador**](qualifier.md)                 | Representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.                                                           |
| [**Qualificadores**](qualifiers.md)               | Representa uma coleção de qualificadores.                                                                                                          |
| [**Configurações**](settings.md)                   | Habilita ou desabilita as caixas de diálogo para solicitar a identidade do assinante ou do remetente se essa identidade não for especificada.                                     |
| [**Utilitários**](utilities.md)                 | Fornece funcionalidade para tarefas comuns.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Objetos de registro de certificado

O objeto a seguir é usado para registro de certificado.



| Objeto                     | Descrição                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objeto que representa o controle de registro de certificado. ele é usado principalmente na programação em Visual Basic ou em outra linguagem de automação. |



 

 

 
