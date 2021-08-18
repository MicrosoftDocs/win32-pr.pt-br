---
description: Fornece serviços que permitem que os desenvolvedores de aplicativos adicionem segurança baseada em criptografia a aplicativos.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Referência de CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94bd7f8c2052f53b4dc1e244251ba76c1b10e349e0f43434a926db6dbeb9190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772107"
---
# <a name="capicom-reference"></a>Referência de CAPICOM

\[CAPICOM é um componente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)\]

O cliente COM CAPICOM fornece serviços que permitem que os desenvolvedores de aplicativos adicionem segurança com base [*na criptografia aos*](../secgloss/c-gly.md) aplicativos. O CryptoAPI inclui a funcionalidade para autenticação usando [*assinaturas digitais*](../secgloss/d-gly.md), para envelopar mensagens e para criptografar e descriptografar dados.



| Categoria                    | Descrição                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Objetos do Armazenamento de Certificados   | Objetos disponíveis para usar os armazenamentos de certificados e os certificados nesses armazenamentos.                                       |
| Objetos de assinatura digital   | Objetos usados para assinar dados digitalmente e verificar assinaturas digitais.                                                      |
| Objetos de dados envelhados      | Objetos usados para criar mensagens de dados enveloadas para privacidade e para descriptografar dados em mensagens enveloadas.                      |
| Objetos de criptografia de dados     | Objetos usados para criptografar dados e descriptografar dados criptografados.                                                                |
| Objetos auxiliares           | Objetos usados para alterar comportamentos padrão e para gerenciar certificados, armazenamentos de certificados e mensagens de interface do usuário. |
| Interfaces de interoperabilidade | Interfaces que permitem que derivações de CryptoAPI funcionem em conjunto com CAPICOM 2.0.                                          |
| Tipos de enumeração           | Tipos de enumeração usados com CAPICOM.                                                                                       |



 

## <a name="certificate-store-objects"></a>Objetos do Armazenamento de Certificados

Os objetos a seguir funcionam [*com os armazenamentos de*](../secgloss/c-gly.md) certificados e os certificados nesses armazenamentos. O CAPICOM dá suporte ao uso de armazenamentos de certificados do Usuário Atual, Computador Local, Memória e Active Directory.



| Objeto                                             | Descrição                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificado**](certificate.md)                 | Um único certificado digital.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Uma coleção de [**objetos PolicyInformation.**](policyinformation.md)                                                 |
| [**Certificados**](certificates.md)               | Coleção de [**objetos certificate.**](certificate.md)                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fornece informações de status sobre um certificado.                                                                           |
| [**Cadeia**](chain.md)                             | Cria e verifica uma cadeia de validação de certificado com base em um certificado digital.                                       |
| [**Extendedproperties**](extendedproperties.md)   | Representa uma coleção de [**objetos ExtendedProperty.**](extendedproperty.md)                                        |
| [**Extendedproperty**](extendedproperty.md)       | Representa uma propriedade estendida da Microsoft.                                                                               |
| [**Extensão**](extension.md)                     | Representa uma única extensão de certificado.                                                                              |
| [**Extensões**](extensions.md)                   | Representa uma coleção de objetos [**Extension.**](extension.md)                                                      |
| [**Privatekey**](privatekey.md)                   | Representa uma chave privada.                                                                                               |
| [**Publickey**](publickey.md)                     | Representa uma chave pública em um [**objeto Certificate.**](certificate.md)                                                 |
| [**Store**](store.md)                             | Fornece as propriedades e os métodos para escolher, gerenciar e usar os armazenamentos de certificados e os certificados nesses armazenamentos. |
| [**Modelo**](template.md)                       | Representa o modelo de extensão de certificado do certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de assinatura digital

Os objetos a seguir são exportados para assinar dados digitalmente e verificar assinaturas digitais.



| Objeto                           | Descrição                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Fornece funcionalidade para assinatura de conteúdo com uma assinatura digital Authenticode. |
| [**SignedData**](signeddata.md) | Objeto usado para assinar dados e verificar a assinatura em dados assinados.               |
| [**Signatário**](signer.md)         | Informações sobre um único signante de dados, incluindo o certificado do signante.           |
| [**Signatários**](signers.md)       | Coleção de [**objetos Signer.**](signer.md)                                    |



 

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
| [**Oid**](oid.md)                             | Representa um identificador de objeto que é usado por várias propriedades CAPICOM.                                                                     |
| [**OIDs**](oids.md)                           | Representa uma coleção de [**objetos OID.**](oid.md)                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fornece acesso às OIDs de política de uma extensão.                                                                                             |
| [**Qualificador**](qualifier.md)                 | Representa um ponteiro CPS (Instrução de Prática de Certificação) ou um qualificador de aviso do usuário.                                                           |
| [**Qualificadores**](qualifiers.md)               | Representa uma coleção de qualificadores.                                                                                                          |
| [**Configurações**](settings.md)                   | Habilita ou desabilita caixas de diálogo para solicitar a identidade do signante ou remetente se essa identidade não for especificada.                                     |
| [**Utilitários**](utilities.md)                 | Fornece funcionalidade para tarefas comuns.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfaces de interoperabilidade

As interfaces a seguir permitem que derivações de CryptoAPI funcionem em conjunto com CAPICOM 2.0.



| Interface                              | Descrição                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fornece acesso ao contexto de um objeto certificado CAPICOM X.509v3. [](certificate.md) Esse contexto permite que o certificado CAPICOM seja usado em outras derivações de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fornece acesso ao contexto de um objeto CAPICOM [**Store.**](store.md) Esse contexto permite que o armazenamento de certificados CAPICOM seja usado em outras derivações de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornece acesso ao contexto de [](chain.md) um objeto de cadeia CAPICOM. Esse contexto permite que a cadeia de confiança de certificado CAPICOM seja usada em outras derivações de CryptoAPI.         |



 

## <a name="enumeration-types"></a>Tipos de enumeração

CAPICOM define os seguintes tipos de enumeração:

-   [**CAPICOM \_ ACTIVE \_ DIRECTORY \_ SEARCH \_ LOCATION**](capicom-active-directory-search-location.md)
-   [**ATRIBUTO \_ CAPICOM**](capicom-attribute.md)
-   [**TIPO DE INFORMAÇÕES DE CERTIFICADO CAPICOM \_ \_ \_**](capicom-cert-info-type.md)
-   [**TIPO DE ENCONTRAR CERTIFICADO CAPICOM \_ \_ \_**](capicom-certificate-find-type.md)
-   [**OPÇÃO CAPICOM \_ CERTIFICATE \_ INCLUDE \_**](capicom-certificate-include-option.md)
-   [**TIPO SALVAR CERTIFICADO CAPICOM \_ \_ \_ \_**](capicom-certificate-save-as-type.md)
-   [**CERTIFICADOS CAPICOM \_ \_ SALVAR COMO \_ \_ TIPO**](capicom-certificates-save-as-type.md)
-   [**SINALIZADOR DE VERIFICAÇÃO CAPICOM \_ \_**](capicom-check-flag.md)
-   [**CAPICOM \_ EKU**](capicom-eku.md)
-   [**TIPO DE \_ CODIFICAÇÃO \_ CAPICOM**](capicom-encoding-type.md)
-   [**ALGORITMO DE CRIPTOGRAFIA CAPICOM \_ \_**](capicom-encryption-algorithm.md)
-   [**COMPRIMENTO DA CHAVE DE CRIPTOGRAFIA CAPICOM \_ \_ \_**](capicom-encryption-key-length.md)
-   [**CÓDIGO DE ERRO CAPICOM \_ \_**](capicom-error-code.md)
-   [**SINALIZADOR DE EXPORTAÇÃO CAPICOM \_ \_**](capicom-export-flag.md)
-   [**ALGORITMO DE HASH CAPICOM \_ \_**](capicom-hash-algorithm.md)
-   [**LOCALIZAÇÃO DA CHAVE CAPICOM \_ \_**](capicom-key-location.md)
-   [**CAPICOM \_ KEY \_ SPEC**](capicom-key-spec.md)
-   [**SINALIZADOR DE ARMAZENAMENTO DE CHAVES CAPICOM \_ \_ \_**](capicom-key-storage-flag.md)
-   [**CAPICOM \_ OID**](capicom-oid.md)
-   [**CAPICOM \_ PROPID**](capicom-propid.md)
-   [**TIPO CAPICOM \_ \_ PROV**](capicom-prov-type.md)
-   [**TIPO DE SEGREDO \_ \_ CAPICOM**](capicom-secret-type.md)
-   [**SINALIZADOR CAPICOM \_ SIGNED \_ DATA \_ VERIFY \_**](capicom-signed-data-verify-flag.md)
-   [**LOCAL DO ARMAZENAMENTO CAPICOM \_ \_**](capicom-store-location.md)
-   [**MODO ABERTO DO CAPICOM \_ STORE \_ \_**](capicom-store-open-mode.md)
-   [**CAPICOM \_ STORE \_ SAVE \_ AS \_ TYPE**](capicom-store-save-as-type.md)

 

 
