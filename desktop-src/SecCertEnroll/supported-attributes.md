---
description: A API de registro de certificado dá suporte aos seguintes atributos. Você pode criar um atributo individual usando a interface correspondente identificada em cada uma das seções a seguir.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Atributos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bfff5785a0b891e98e6d78d59b4688e2d5c11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789501"
---
# <a name="supported-attributes"></a><span data-ttu-id="b6daa-104">Atributos com suporte</span><span class="sxs-lookup"><span data-stu-id="b6daa-104">Supported Attributes</span></span>

<span data-ttu-id="b6daa-105">A API de registro de certificado dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="b6daa-105">The Certificate Enrollment API supports the following attributes.</span></span> <span data-ttu-id="b6daa-106">Você pode criar um atributo individual usando a interface correspondente identificada em cada uma das seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6daa-106">You can create an individual attribute by using the corresponding interface identified in each of the following sections.</span></span>

## <a name="clientid"></a><span data-ttu-id="b6daa-107">ClientId</span><span class="sxs-lookup"><span data-stu-id="b6daa-107">ClientId</span></span>

<span data-ttu-id="b6daa-108">A interface [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) pode ser usada para definir um atributo que contém informações sobre o computador cliente que enviou a solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-108">The [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface can be used to define an attribute that contains information about the client computer that sent the certificate request.</span></span> <span data-ttu-id="b6daa-109">As informações podem ser usadas para diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="b6daa-109">The information can be used for diagnostics.</span></span>

<span data-ttu-id="b6daa-110">**Aplica-se a:** \#Solicitação PKCS 10 ou CMC.</span><span class="sxs-lookup"><span data-stu-id="b6daa-110">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="b6daa-111">**OID:** \_ \_ \_ \_ Informações do cliente de solicitação de OID XCN (1.3.6.1.4.1.311.21.20)</span><span class="sxs-lookup"><span data-stu-id="b6daa-111">**OID:** XCN\_OID\_REQUEST\_CLIENT\_INFO (1.3.6.1.4.1.311.21.20)</span></span>

## <a name="extensions"></a><span data-ttu-id="b6daa-112">Extensões</span><span class="sxs-lookup"><span data-stu-id="b6daa-112">Extensions</span></span>

<span data-ttu-id="b6daa-113">A interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) pode ser usada para definir um conjunto de extensões de certificado X. 509 versão 3.</span><span class="sxs-lookup"><span data-stu-id="b6daa-113">The [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface can be used to define a set of X.509 version 3 certificate extensions.</span></span> <span data-ttu-id="b6daa-114">Há suporte para as seguintes extensões.</span><span class="sxs-lookup"><span data-stu-id="b6daa-114">The following extensions are supported.</span></span> <span data-ttu-id="b6daa-115">Para obter mais informações, consulte o tópico interfaces de extensão.</span><span class="sxs-lookup"><span data-stu-id="b6daa-115">For more information, see the Extension Interfaces topic.</span></span>



| <span data-ttu-id="b6daa-116">Extensão</span><span class="sxs-lookup"><span data-stu-id="b6daa-116">Extension</span></span>              | <span data-ttu-id="b6daa-117">Description</span><span class="sxs-lookup"><span data-stu-id="b6daa-117">Description</span></span>                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6daa-118">Alternativos</span><span class="sxs-lookup"><span data-stu-id="b6daa-118">AlternativeNames</span></span>       | <span data-ttu-id="b6daa-119">Contém uma ou mais formas de nome alternativo do emissor associado ao certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-119">Contains one or more alternative name forms of the issuer associated with the certificate.</span></span>                                                                                                                                       |
| <span data-ttu-id="b6daa-120">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="b6daa-120">AuthorityKeyIdentifier</span></span> | <span data-ttu-id="b6daa-121">Contém um identificador de chave exclusivo para diferenciar entre várias chaves de assinatura de certificado da [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA).</span><span class="sxs-lookup"><span data-stu-id="b6daa-121">Contains a unique key identifier to differentiate between multiple certificate signing keys of the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span> |
| <span data-ttu-id="b6daa-122">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="b6daa-122">BasicConstraints</span></span>       | <span data-ttu-id="b6daa-123">Indica se o assunto pode atuar como uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="b6daa-123">Indicates whether the subject can act as a CA.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="b6daa-124">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="b6daa-124">CertificatePolicies</span></span>    | <span data-ttu-id="b6daa-125">Identifica as políticas e informações de qualificador opcionais associadas ao certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-125">Identifies the policies and optional qualifier information associated with the certificate.</span></span>                                                                                                                                      |
| <span data-ttu-id="b6daa-126">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="b6daa-126">MSApplicationPolicies</span></span>  | <span data-ttu-id="b6daa-127">Identifica um ou mais usos para o certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-127">Identifies one or more uses for the certificate.</span></span> <span data-ttu-id="b6daa-128">Essa extensão é semelhante à extensão EnhancedKeyUsage, mas é definida pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b6daa-128">This extension is similar to the EnhancedKeyUsage extension but is Microsoft-defined.</span></span>                                                                                           |
| <span data-ttu-id="b6daa-129">EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="b6daa-129">EnhancedKeyUsage</span></span>       | <span data-ttu-id="b6daa-130">Identifica um ou mais usos da chave pública contida no certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-130">Identifies one or more uses of the public key contained in the certificate.</span></span> <span data-ttu-id="b6daa-131">A extensão de uso avançado de chave pode ser usada além de ou no lugar da extensão de uso de chave.</span><span class="sxs-lookup"><span data-stu-id="b6daa-131">The enhanced key usage extension can be used in addition to or in place of the key usage extension.</span></span>                                                  |
| <span data-ttu-id="b6daa-132">Uso de</span><span class="sxs-lookup"><span data-stu-id="b6daa-132">KeyUsage</span></span>               | <span data-ttu-id="b6daa-133">Identifica as restrições nas operações que podem ser executadas pela chave pública contida no certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-133">Identifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                                                  |
| <span data-ttu-id="b6daa-134">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="b6daa-134">SmimeCapabilities</span></span>      | <span data-ttu-id="b6daa-135">Relata os recursos de descriptografia de um destinatário de email para o remetente do email para permitir que o remetente escolha o algoritmo simétrico mais seguro com suporte de ambas as partes.</span><span class="sxs-lookup"><span data-stu-id="b6daa-135">Reports the decryption capabilities of an email recipient to the email sender to enable the sender to choose the most secure symmetric algorithm supported by both parties.</span></span>                                                      |
| <span data-ttu-id="b6daa-136">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="b6daa-136">SubjectKeyIdentifier</span></span>   | <span data-ttu-id="b6daa-137">Contém um identificador de chave exclusivo que pode ser usado para diferenciar várias chaves de assinatura associadas ao proprietário do certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-137">Contains a unique key identifier that can be used to differentiate between multiple signing keys associated with the certificate owner.</span></span>                                                                                          |
| <span data-ttu-id="b6daa-138">Modelo</span><span class="sxs-lookup"><span data-stu-id="b6daa-138">Template</span></span>               | <span data-ttu-id="b6daa-139">Identifica o modelo a ser usado ao emitir ou renovar um certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-139">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="b6daa-140">A extensão contém o identificador de objeto (OID) do modelo.</span><span class="sxs-lookup"><span data-stu-id="b6daa-140">The extension contains the object identifier (OID) of the template.</span></span>                                                                                       |
| <span data-ttu-id="b6daa-141">TemplateName</span><span class="sxs-lookup"><span data-stu-id="b6daa-141">TemplateName</span></span>           | <span data-ttu-id="b6daa-142">Identifica o modelo a ser usado ao emitir ou renovar um certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-142">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="b6daa-143">A extensão contém o nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="b6daa-143">The extension contains the name of the template.</span></span>                                                                                                          |



 

<span data-ttu-id="b6daa-144">**Aplica-se a:** \#Solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="b6daa-144">**Applies To:** PKCS \#10 request.</span></span>

<span data-ttu-id="b6daa-145">**OID:** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)</span><span class="sxs-lookup"><span data-stu-id="b6daa-145">**OID:** XCN\_OID\_RSA\_certExtensions (1.2.840.113549.1.9.14)</span></span>

## <a name="archivekey"></a><span data-ttu-id="b6daa-146">ArchiveKey</span><span class="sxs-lookup"><span data-stu-id="b6daa-146">ArchiveKey</span></span>

<span data-ttu-id="b6daa-147">A interface [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) pode ser usada para definir um atributo que contém uma chave privada criptografada enviada a uma AC para arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b6daa-147">The [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) interface can be used to define an attribute that contains an encrypted private key submitted to a CA for archiving.</span></span>

<span data-ttu-id="b6daa-148">**Aplica-se a:** Solicitação de CMC.</span><span class="sxs-lookup"><span data-stu-id="b6daa-148">**Applies To:** CMC request.</span></span>

<span data-ttu-id="b6daa-149">**OID:** \_ \_ \_ Attr de chave arquivada \_ do OID do XCN (1.3.6.1.4.1.311.21.13)</span><span class="sxs-lookup"><span data-stu-id="b6daa-149">**OID:** XCN\_OID\_ARCHIVED\_KEY\_ATTR (1.3.6.1.4.1.311.21.13)</span></span>

## <a name="archivekeyhash"></a><span data-ttu-id="b6daa-150">ArchiveKeyHash</span><span class="sxs-lookup"><span data-stu-id="b6daa-150">ArchiveKeyHash</span></span>

<span data-ttu-id="b6daa-151">A interface [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) pode ser usada para definir um hash da chave privada contida no atributo **ArchiveKey** .</span><span class="sxs-lookup"><span data-stu-id="b6daa-151">The [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) interface can be used to define a hash of the private key contained in the **ArchiveKey** attribute.</span></span>

<span data-ttu-id="b6daa-152">**Aplica-se a:** Solicitação de CMC.</span><span class="sxs-lookup"><span data-stu-id="b6daa-152">**Applies To:** CMC request.</span></span>

<span data-ttu-id="b6daa-153">**OID:** \_ \_ \_ Hash de chave criptografada de OID XCN \_ (1.3.6.1.4.1.311.21.21)</span><span class="sxs-lookup"><span data-stu-id="b6daa-153">**OID:** XCN\_OID\_ENCRYPTED\_KEY\_HASH (1.3.6.1.4.1.311.21.21)</span></span>

## <a name="cspprovider"></a><span data-ttu-id="b6daa-154">CspProvider</span><span class="sxs-lookup"><span data-stu-id="b6daa-154">CspProvider</span></span>

<span data-ttu-id="b6daa-155">A interface [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) pode ser usada para definir um atributo que contém informações sobre o CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ) usado pelo solicitante para operações criptográficas.</span><span class="sxs-lookup"><span data-stu-id="b6daa-155">The [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) interface can be used to define an attribute that contains information about the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) used by the requester for cryptographic operations.</span></span>

<span data-ttu-id="b6daa-156">**Aplica-se a:** \#Solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="b6daa-156">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="b6daa-157">Esse atributo é criado automaticamente quando você cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="b6daa-157">This attribute is automatically created when you create an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>

<span data-ttu-id="b6daa-158">**OID:** \_ \_ \_ Provedor CSP de registro \_ do XCN OID (1.3.6.1.4.1.311.13.2.2)</span><span class="sxs-lookup"><span data-stu-id="b6daa-158">**OID:** XCN\_OID\_ENROLLMENT\_CSP\_PROVIDER (1.3.6.1.4.1.311.13.2.2)</span></span>

## <a name="osversion"></a><span data-ttu-id="b6daa-159">OSVersion</span><span class="sxs-lookup"><span data-stu-id="b6daa-159">OSVersion</span></span>

<span data-ttu-id="b6daa-160">A interface [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) pode ser usada para criar um atributo que contém informações de versão sobre o sistema operacional do cliente.</span><span class="sxs-lookup"><span data-stu-id="b6daa-160">The [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) interface can be used to create an attribute that contains version information about the client operating system.</span></span> <span data-ttu-id="b6daa-161">As informações podem ser usadas pela autoridade de certificação para determinar o tipo de processamento a ser aplicado ao criar o certificado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-161">The information can be used by the CA to determine the type of processing to apply when creating the certificate.</span></span>

<span data-ttu-id="b6daa-162">**Aplica-se a:** \#Solicitação PKCS 10 ou CMC.</span><span class="sxs-lookup"><span data-stu-id="b6daa-162">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="b6daa-163">**OID:** \_ \_ Versão do sistema operacional XCN OID \_ (1.3.6.1.4.1.311.13.2.3)</span><span class="sxs-lookup"><span data-stu-id="b6daa-163">**OID:** XCN\_OID\_OS\_VERSION (1.3.6.1.4.1.311.13.2.3)</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="b6daa-164">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="b6daa-164">RenewalCertificate</span></span>

<span data-ttu-id="b6daa-165">A interface [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) pode ser usada para criar um atributo que contém o certificado que está sendo renovado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-165">The [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) interface can be used to create an attribute that contains the certificate being renewed.</span></span>

<span data-ttu-id="b6daa-166">**Aplica-se a:** \#Solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="b6daa-166">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="b6daa-167">Esse atributo será criado automaticamente se você criar uma \# solicitação PKCS 10 iniciando-a com o certificado que está sendo renovado.</span><span class="sxs-lookup"><span data-stu-id="b6daa-167">This attribute is automatically created if you create a PKCS \#10 request by initiating it with the certificate being renewed.</span></span>

<span data-ttu-id="b6daa-168">**OID:** XCN \_ \_ \_ certificado de renovação de OID (1.3.6.1.4.1.311.13.1)</span><span class="sxs-lookup"><span data-stu-id="b6daa-168">**OID:** XCN\_OID\_RENEWAL\_CERTIFICATE (1.3.6.1.4.1.311.13.1)</span></span>

 

 
