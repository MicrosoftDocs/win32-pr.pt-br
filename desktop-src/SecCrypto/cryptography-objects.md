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
# <a name="cryptography-objects"></a><span data-ttu-id="fa173-103">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="fa173-103">Cryptography Objects</span></span>

<span data-ttu-id="fa173-104">Os objetos de criptografia são categorizados de acordo com o uso da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fa173-104">Cryptography objects are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="fa173-105">Objetos de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="fa173-105">Certificate Store Objects</span></span>](#certificate-store-objects)
-   [<span data-ttu-id="fa173-106">Objetos de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="fa173-106">Digital Signature Objects</span></span>](#digital-signature-objects)
-   [<span data-ttu-id="fa173-107">Objetos de dados de envelope</span><span class="sxs-lookup"><span data-stu-id="fa173-107">Enveloped Data Objects</span></span>](#enveloped-data-objects)
-   [<span data-ttu-id="fa173-108">Objetos de criptografia de dados</span><span class="sxs-lookup"><span data-stu-id="fa173-108">Data Encryption Objects</span></span>](#data-encryption-objects)
-   [<span data-ttu-id="fa173-109">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="fa173-109">Auxiliary Objects</span></span>](#auxiliary-objects)
-   [<span data-ttu-id="fa173-110">Objetos de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="fa173-110">Certificate Enrollment Objects</span></span>](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a><span data-ttu-id="fa173-111">Objetos de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="fa173-111">Certificate Store Objects</span></span>

<span data-ttu-id="fa173-112">Os objetos a seguir funcionam com [*repositórios de certificados*](../secgloss/c-gly.md) e os certificados nesses armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="fa173-112">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="fa173-113">O CAPICOM dá suporte ao uso do usuário atual, do computador local, da memória e dos repositórios de certificados Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fa173-113">CAPICOM supports the use of Current User, Local Machine, memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="fa173-114">Objeto</span><span class="sxs-lookup"><span data-stu-id="fa173-114">Object</span></span>                                             | <span data-ttu-id="fa173-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa173-115">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa173-116">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="fa173-116">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="fa173-117">Um único certificado digital.</span><span class="sxs-lookup"><span data-stu-id="fa173-117">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="fa173-118">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="fa173-118">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="fa173-119">Uma coleção de objetos [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-119">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="fa173-120">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="fa173-120">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="fa173-121">Coleção de objetos de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-121">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="fa173-122">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="fa173-122">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="fa173-123">Fornece informações de status sobre um certificado.</span><span class="sxs-lookup"><span data-stu-id="fa173-123">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="fa173-124">**Cadeia**</span><span class="sxs-lookup"><span data-stu-id="fa173-124">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="fa173-125">Cria e verifica uma cadeia de validação de certificado com base em um certificado digital.</span><span class="sxs-lookup"><span data-stu-id="fa173-125">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="fa173-126">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="fa173-126">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="fa173-127">Representa uma coleção de objetos [**Extended**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-127">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="fa173-128">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="fa173-128">**ExtendedProperty**</span></span>](extendedproperties.md)     | <span data-ttu-id="fa173-129">Representa uma propriedade estendida da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa173-129">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="fa173-130">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="fa173-130">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="fa173-131">Representa uma única extensão de certificado.</span><span class="sxs-lookup"><span data-stu-id="fa173-131">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="fa173-132">**Extensões**</span><span class="sxs-lookup"><span data-stu-id="fa173-132">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="fa173-133">Representa uma coleção de objetos de [**extensão**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-133">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="fa173-134">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="fa173-134">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="fa173-135">Representa uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="fa173-135">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="fa173-136">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="fa173-136">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="fa173-137">Representa uma chave pública em um objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-137">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="fa173-138">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="fa173-138">**Store**</span></span>](store.md)                             | <span data-ttu-id="fa173-139">Fornece as propriedades e os métodos para escolher, gerenciar e usar os repositórios de certificados e os certificados nesses armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="fa173-139">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="fa173-140">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="fa173-140">**Template**</span></span>](template.md)                       | <span data-ttu-id="fa173-141">Representa o modelo de extensão de certificado do certificado.</span><span class="sxs-lookup"><span data-stu-id="fa173-141">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="fa173-142">Objetos de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="fa173-142">Digital Signature Objects</span></span>

<span data-ttu-id="fa173-143">Os objetos a seguir são exportados para assinar dados digitalmente e para verificar assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="fa173-143">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="fa173-144">Objeto</span><span class="sxs-lookup"><span data-stu-id="fa173-144">Object</span></span>                           | <span data-ttu-id="fa173-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa173-145">Description</span></span>                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa173-146">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="fa173-146">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="fa173-147">Objeto usado para assinar o código com uma assinatura digital Authenticode e verificar a assinatura no código assinado.</span><span class="sxs-lookup"><span data-stu-id="fa173-147">Object used to sign code with an Authenticode digital signature and to verify the signature on signed code.</span></span> |
| [<span data-ttu-id="fa173-148">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="fa173-148">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="fa173-149">Objeto usado para assinar dados e verificar a assinatura em dados assinados.</span><span class="sxs-lookup"><span data-stu-id="fa173-149">Object used to sign data and to verify the signature on signed data.</span></span>                                        |
| [<span data-ttu-id="fa173-150">**Signatário**</span><span class="sxs-lookup"><span data-stu-id="fa173-150">**Signer**</span></span>](signer.md)         | <span data-ttu-id="fa173-151">Informações sobre um único signatário de dados, incluindo o certificado do signatário.</span><span class="sxs-lookup"><span data-stu-id="fa173-151">Information on a single data signer, including the signer's certificate.</span></span>                                    |
| [<span data-ttu-id="fa173-152">**Signatários**</span><span class="sxs-lookup"><span data-stu-id="fa173-152">**Signers**</span></span>](signers.md)       | <span data-ttu-id="fa173-153">Coleção de objetos de [**signatário**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-153">Collection of [**Signer**](signer.md) objects.</span></span>                                                             |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="fa173-154">Objetos de dados de envelope</span><span class="sxs-lookup"><span data-stu-id="fa173-154">Enveloped Data Objects</span></span>

<span data-ttu-id="fa173-155">Os seguintes objetos são exportados para criar mensagens de dados envelopadas para privacidade e para descriptografar dados em mensagens envelopadas.</span><span class="sxs-lookup"><span data-stu-id="fa173-155">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="fa173-156">Objeto</span><span class="sxs-lookup"><span data-stu-id="fa173-156">Object</span></span>                                 | <span data-ttu-id="fa173-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa173-157">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa173-158">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="fa173-158">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="fa173-159">Objetos usados para criar, enviar e receber dados de envelopes.</span><span class="sxs-lookup"><span data-stu-id="fa173-159">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="fa173-160">Os dados de envelope são criptografados para que somente os destinatários pretendidos possam descriptografá-los.</span><span class="sxs-lookup"><span data-stu-id="fa173-160">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="fa173-161">**Destinatários**</span><span class="sxs-lookup"><span data-stu-id="fa173-161">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="fa173-162">Coleção dos objetos de [**certificado**](certificate.md) dos destinatários pretendidos de uma mensagem envelopada.</span><span class="sxs-lookup"><span data-stu-id="fa173-162">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="fa173-163">Objetos de criptografia de dados</span><span class="sxs-lookup"><span data-stu-id="fa173-163">Data Encryption Objects</span></span>

<span data-ttu-id="fa173-164">O objeto a seguir é exportado para criptografar dados arbitrários para privacidade e para descriptografar dados criptografados.</span><span class="sxs-lookup"><span data-stu-id="fa173-164">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="fa173-165">Objeto</span><span class="sxs-lookup"><span data-stu-id="fa173-165">Object</span></span>                                 | <span data-ttu-id="fa173-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa173-166">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa173-167">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="fa173-167">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="fa173-168">Objetos usados para criptografar dados.</span><span class="sxs-lookup"><span data-stu-id="fa173-168">Objects used to encrypt data.</span></span> <span data-ttu-id="fa173-169">Os dados criptografados em um objeto [**EncryptedData**](encrypteddata.md) podem ser descriptografados.</span><span class="sxs-lookup"><span data-stu-id="fa173-169">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="fa173-170">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="fa173-170">Auxiliary Objects</span></span>

<span data-ttu-id="fa173-171">Os objetos a seguir são exportados para alterar os comportamentos padrão de outros objetos e para gerenciar certificados, repositórios de certificados e mensagens.</span><span class="sxs-lookup"><span data-stu-id="fa173-171">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="fa173-172">Objeto</span><span class="sxs-lookup"><span data-stu-id="fa173-172">Object</span></span>                                         | <span data-ttu-id="fa173-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa173-173">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa173-174">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="fa173-174">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="fa173-175">Define o algoritmo e o [*comprimento da chave*](../secgloss/k-gly.md) a serem usados em operações criptográficas.</span><span class="sxs-lookup"><span data-stu-id="fa173-175">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="fa173-176">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fa173-176">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="fa173-177">Fornece uma única parte das informações adicionadas sobre uma assinatura, como a hora da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fa173-177">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="fa173-178">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="fa173-178">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="fa173-179">Coleção de objetos de [**atributo**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-179">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="fa173-180">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="fa173-180">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="fa173-181">Fornece acesso somente leitura a restrições básicas sobre os usos de um certificado.</span><span class="sxs-lookup"><span data-stu-id="fa173-181">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="fa173-182">**EKU**</span><span class="sxs-lookup"><span data-stu-id="fa173-182">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="fa173-183">Fornece acesso às propriedades EKU de certificados.</span><span class="sxs-lookup"><span data-stu-id="fa173-183">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="fa173-184">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="fa173-184">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="fa173-185">Coleção de objetos [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-185">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="fa173-186">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="fa173-186">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="fa173-187">Representa um bloco de dados codificados.</span><span class="sxs-lookup"><span data-stu-id="fa173-187">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="fa173-188">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="fa173-188">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="fa173-189">Fornece acesso somente leitura às propriedades de uso estendido de chave de certificados.</span><span class="sxs-lookup"><span data-stu-id="fa173-189">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="fa173-190">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="fa173-190">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="fa173-191">Fornece a funcionalidade para aplicar um algoritmo de hash a uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fa173-191">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="fa173-192">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="fa173-192">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="fa173-193">Fornece acesso somente leitura às principais propriedades de uso de certificados.</span><span class="sxs-lookup"><span data-stu-id="fa173-193">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="fa173-194">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="fa173-194">**NoticeNumbers**</span></span>](noticenumbers.md)         | <span data-ttu-id="fa173-195">Representa uma coleção de objetos de [**extensão**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-195">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                                              |
| [<span data-ttu-id="fa173-196">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="fa173-196">**OID**</span></span>](oid.md)                             | <span data-ttu-id="fa173-197">Representa um identificador de objeto que é usado por várias propriedades capicor.</span><span class="sxs-lookup"><span data-stu-id="fa173-197">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="fa173-198">**OID**</span><span class="sxs-lookup"><span data-stu-id="fa173-198">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="fa173-199">Representa uma coleção de objetos [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="fa173-199">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="fa173-200">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="fa173-200">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="fa173-201">Fornece acesso aos OIDs de política de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="fa173-201">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="fa173-202">**Qualificador**</span><span class="sxs-lookup"><span data-stu-id="fa173-202">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="fa173-203">Representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa173-203">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="fa173-204">**Qualificadores**</span><span class="sxs-lookup"><span data-stu-id="fa173-204">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="fa173-205">Representa uma coleção de qualificadores.</span><span class="sxs-lookup"><span data-stu-id="fa173-205">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="fa173-206">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="fa173-206">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="fa173-207">Habilita ou desabilita as caixas de diálogo para solicitar a identidade do assinante ou do remetente se essa identidade não for especificada.</span><span class="sxs-lookup"><span data-stu-id="fa173-207">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="fa173-208">**Utilitários**</span><span class="sxs-lookup"><span data-stu-id="fa173-208">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="fa173-209">Fornece funcionalidade para tarefas comuns.</span><span class="sxs-lookup"><span data-stu-id="fa173-209">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a><span data-ttu-id="fa173-210">Objetos de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="fa173-210">Certificate Enrollment Objects</span></span>

<span data-ttu-id="fa173-211">O objeto a seguir é usado para registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="fa173-211">The following object is used for certificate enrollment.</span></span>



| <span data-ttu-id="fa173-212">Objeto</span><span class="sxs-lookup"><span data-stu-id="fa173-212">Object</span></span>                     | <span data-ttu-id="fa173-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa173-213">Description</span></span>                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa173-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa173-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span></span> | <span data-ttu-id="fa173-215">Objeto que representa o controle de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="fa173-215">Object that represents the Certificate Enrollment Control.</span></span> <span data-ttu-id="fa173-216">Ele é usado principalmente na programação em Visual Basic ou em outra linguagem de automação.</span><span class="sxs-lookup"><span data-stu-id="fa173-216">It is primarily used when programming in Visual Basic or another Automation language.</span></span> |



 

 

 
