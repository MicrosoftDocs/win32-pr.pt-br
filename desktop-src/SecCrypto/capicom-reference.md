---
description: Fornece serviços que permitem que os desenvolvedores de aplicativos adicionem segurança com base na criptografia a aplicativos.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Referência de CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b828f3b5b35e3e0ef799529f866c23416c8df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770351"
---
# <a name="capicom-reference"></a>Referência de CAPICOM

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

O cliente COM CAPICOM fornece serviços que permitem que os desenvolvedores de aplicativos adicionem segurança com base na [*criptografia*](../secgloss/c-gly.md) a aplicativos. O CryptoAPI inclui a funcionalidade de autenticação usando [*assinaturas digitais*](../secgloss/d-gly.md), para mensagens enveloping e para criptografar e descriptografar dados.



| Categoria                    | Descrição                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Objetos de repositório de certificados   | Objetos disponíveis para uso de repositórios de certificados e certificados nesses armazenamentos.                                       |
| Objetos de assinatura digital   | Objetos usados para assinar digitalmente os dados e para verificar as assinaturas digitais.                                                      |
| Objetos de dados de envelope      | Objetos usados para criar mensagens de dados envelopadas para privacidade e descriptografar dados em mensagens envelopadas.                      |
| Objetos de criptografia de dados     | Objetos usados para criptografar dados e descriptografar dados criptografados.                                                                |
| Objetos auxiliares           | Objetos usados para alterar comportamentos padrão e gerenciar certificados, repositórios de certificados e mensagens de interface do usuário (IU). |
| Interfaces de interoperabilidade | Interfaces que permitem que as derivações de CryptoAPI funcionem em conjunto com CAPICOM 2,0.                                          |
| Tipos de enumeração           | Tipos de enumeração usados com CAPICOM.                                                                                       |



 

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
| [**ExtendedProperty**](extendedproperty.md)       | Representa uma propriedade estendida da Microsoft.                                                                               |
| [**Extensão**](extension.md)                     | Representa uma única extensão de certificado.                                                                              |
| [**Extensões**](extensions.md)                   | Representa uma coleção de objetos de [**extensão**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Representa uma chave privada.                                                                                               |
| [**PublicKey**](publickey.md)                     | Representa uma chave pública em um objeto de [**certificado**](certificate.md) .                                                 |
| [**Repositório**](store.md)                             | Fornece as propriedades e os métodos para escolher, gerenciar e usar os repositórios de certificados e os certificados nesses armazenamentos. |
| [**Modelo**](template.md)                       | Representa o modelo de extensão de certificado do certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de assinatura digital

Os objetos a seguir são exportados para assinar dados digitalmente e para verificar assinaturas digitais.



| Objeto                           | Descrição                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Fornece a funcionalidade para assinar conteúdo com uma assinatura digital Authenticode. |
| [**SignedData**](signeddata.md) | Objeto usado para assinar dados e verificar a assinatura em dados assinados.               |
| [**Signatário**](signer.md)         | Informações sobre um único signatário de dados, incluindo o certificado do signatário.           |
| [**Signatários**](signers.md)       | Coleção de objetos de [**signatário**](signer.md) .                                    |



 

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
| [**OIDs**](oid.md)                             | Representa um identificador de objeto que é usado por várias propriedades capicor.                                                                     |
| [**OID**](oids.md)                           | Representa uma coleção de objetos [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fornece acesso aos OIDs de política de uma extensão.                                                                                             |
| [**Qualificador**](qualifier.md)                 | Representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.                                                           |
| [**Qualificadores**](qualifiers.md)               | Representa uma coleção de qualificadores.                                                                                                          |
| [**Configurações**](settings.md)                   | Habilita ou desabilita as caixas de diálogo para solicitar a identidade do assinante ou do remetente se essa identidade não for especificada.                                     |
| [**Utilitários**](utilities.md)                 | Fornece funcionalidade para tarefas comuns.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfaces de interoperabilidade

As interfaces a seguir permitem que as derivações de CryptoAPI funcionem em conjunto com CAPICOM 2,0.



| Interface                              | Descrição                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fornece acesso ao contexto de um objeto de [**certificado**](certificate.md) CAPICOM X. 509v3. Esse contexto permite que o certificado capicor seja usado em outras derivações de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fornece acesso ao contexto de um objeto de [**armazenamento**](store.md) capicor. Esse contexto permite que o repositório de certificados capicor seja usado em outras derivações de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornece acesso ao contexto de um objeto de [**cadeia**](chain.md) capicor. Esse contexto permite que a cadeia de confiança do certificado capicor seja usada em outras derivações de CryptoAPI.         |



 

## <a name="enumeration-types"></a>Tipos de enumeração

CAPICOM define os seguintes tipos de enumeração:

-   [**local de pesquisa do CAPICOM \_ \_ do Active Directory \_ \_**](capicom-active-directory-search-location.md)
-   [**atributo CAPICOM \_**](capicom-attribute.md)
-   [**\_tipo de \_ informações do certificado CAPICOM \_**](capicom-cert-info-type.md)
-   [**\_tipo de \_ localização de certificado CAPICOM \_**](capicom-certificate-find-type.md)
-   [**opção de certificado CAPICOM de \_ \_ inclusão \_**](capicom-certificate-include-option.md)
-   [**\_ \_ Salvar \_ como tipo de certificado de CAPICOM \_**](capicom-certificate-save-as-type.md)
-   [**os certificados CAPICOM \_ \_ Salvar \_ como \_ tipo**](capicom-certificates-save-as-type.md)
-   [**\_sinalizador de verificação de CApicom \_**](capicom-check-flag.md)
-   [**EKU de CAPICOM \_**](capicom-eku.md)
-   [**\_tipo de codificação CApicom \_**](capicom-encoding-type.md)
-   [**\_algoritmo de criptografia CApicom \_**](capicom-encryption-algorithm.md)
-   [**\_comprimento da \_ chave de criptografia CAPICOM \_**](capicom-encryption-key-length.md)
-   [**\_código de erro CApicom \_**](capicom-error-code.md)
-   [**\_sinalizador de exportação de CApicom \_**](capicom-export-flag.md)
-   [**\_algoritmo de hash CApicom \_**](capicom-hash-algorithm.md)
-   [**\_local da chave CApicom \_**](capicom-key-location.md)
-   [**\_espec de chave de CApicom \_**](capicom-key-spec.md)
-   [**\_sinalizador de \_ armazenamento de chave CAPICOM \_**](capicom-key-storage-flag.md)
-   [**OID de CAPICOM \_**](capicom-oid.md)
-   [**CAPICOM \_ propid**](capicom-propid.md)
-   [**tipo CAPICOM \_ Prov \_**](capicom-prov-type.md)
-   [**\_tipo de segredo CApicom \_**](capicom-secret-type.md)
-   [**\_sinalizador de \_ verificação de dados assinados CAPICOM \_ \_**](capicom-signed-data-verify-flag.md)
-   [**\_local do armazenamento CApicom \_**](capicom-store-location.md)
-   [**\_modo de \_ abertura do armazenamento CAPICOM \_**](capicom-store-open-mode.md)
-   [**\_ \_ \_ tipo salvar como \_ do repositório CAPICOM**](capicom-store-save-as-type.md)

 

 
