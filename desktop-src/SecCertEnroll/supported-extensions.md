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
# <a name="supported-extensions"></a><span data-ttu-id="7ea78-103">Extensões com suporte</span><span class="sxs-lookup"><span data-stu-id="7ea78-103">Supported Extensions</span></span>

<span data-ttu-id="7ea78-104">Você pode usar a interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir uma extensão arbitrária.</span><span class="sxs-lookup"><span data-stu-id="7ea78-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="7ea78-105">A API de registro de certificado também fornece interfaces derivadas de **IX509Extension** para permitir que você crie facilmente qualquer uma das extensões mais comuns.</span><span class="sxs-lookup"><span data-stu-id="7ea78-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="7ea78-106">A lista a seguir identifica as extensões comuns com suporte pelas autoridades de certificação da Microsoft e os identificadores de objeto e as interfaces que você pode usar para criá-las.</span><span class="sxs-lookup"><span data-stu-id="7ea78-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="7ea78-107">Alternativos</span><span class="sxs-lookup"><span data-stu-id="7ea78-107">AlternativeNames</span></span>

<span data-ttu-id="7ea78-108">A extensão de nomes alternativos pode ser usada para definir um ou mais formulários de nome alternativo para o assunto da solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="7ea78-109">Dentre os exemplos de formas alternativas incluem-se endereços de email, nomes DNS, endereços IP e URIs.</span><span class="sxs-lookup"><span data-stu-id="7ea78-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="7ea78-110">**Interface:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="7ea78-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="7ea78-111">**OID:** XCN \_ OID \_ Subject \_ ALT \_ nome2 (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="7ea78-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="7ea78-112">AuthorityInformationAccess</span><span class="sxs-lookup"><span data-stu-id="7ea78-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="7ea78-113">A extensão de acesso a informações de autoridade identifica como acessar informações e serviços de autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="7ea78-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="7ea78-114">O valor da extensão contém uma sequência de URIs.</span><span class="sxs-lookup"><span data-stu-id="7ea78-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="7ea78-115">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-116">**OID:** XCN \_ OID \_ Authority \_ info \_ Access (1.3.6.1.5.5.7.1.1)</span><span class="sxs-lookup"><span data-stu-id="7ea78-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="7ea78-117">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="7ea78-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="7ea78-118">A extensão do identificador de chave de autoridade permite a identificação da chave pública da CA que corresponde à chave privada da AC que assinou um certificado emitido.</span><span class="sxs-lookup"><span data-stu-id="7ea78-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="7ea78-119">Ele é usado pelo caminho de certificado que cria software em um Windows Server para localizar o certificado de autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="7ea78-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="7ea78-120">Quando uma CA emite um certificado, o valor da extensão é definido como igual à extensão **SubjectKeyIdentifier** no certificado de autenticação da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="7ea78-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="7ea78-121">O valor normalmente é um hash SHA-1 da chave pública.</span><span class="sxs-lookup"><span data-stu-id="7ea78-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="7ea78-122">**Interface:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="7ea78-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="7ea78-123">**OID:** \_ \_ 2.5.29.35 (XCN OID Authority \_ Key \_ IDENTIFIER2)</span><span class="sxs-lookup"><span data-stu-id="7ea78-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="7ea78-124">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="7ea78-124">BasicConstraints</span></span>

<span data-ttu-id="7ea78-125">A extensão de restrições básicas pode ser usada para identificar se a entidade pode ser usada como uma autoridade de certificação (CA) e, em caso afirmativo, o número de CAs subordinadas que podem existir abaixo dela na cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="7ea78-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="7ea78-126">**Interface:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="7ea78-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="7ea78-127">**OID:** XCN \_ OID \_ básico \_ CONSTRAINTS2 (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="7ea78-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="7ea78-128">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="7ea78-128">CertificatePolicies</span></span>

<span data-ttu-id="7ea78-129">A extensão de políticas de certificado pode ser usada para identificar as políticas sob as quais o certificado foi emitido e os fins para ele podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="7ea78-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="7ea78-130">Elas são identificadas por uma coleção de identificadores de objeto (OIDs).</span><span class="sxs-lookup"><span data-stu-id="7ea78-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="7ea78-131">As políticas são personalizadas para os requisitos de uma organização.</span><span class="sxs-lookup"><span data-stu-id="7ea78-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="7ea78-132">**Interface:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="7ea78-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="7ea78-133">**OID:** \_ \_ \_ Políticas de certificado de OID XCN (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="7ea78-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="7ea78-134">CrlDistributionPoints</span><span class="sxs-lookup"><span data-stu-id="7ea78-134">CrlDistributionPoints</span></span>

<span data-ttu-id="7ea78-135">A extensão dos pontos de distribuição da CRL (lista de certificados revogados) contém o URI da CRL (lista de certificados revogados) base.</span><span class="sxs-lookup"><span data-stu-id="7ea78-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="7ea78-136">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-137">**OID:** XCN \_ OID \_ CRL \_ dist \_ Points (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="7ea78-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="7ea78-138">EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="7ea78-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="7ea78-139">A extensão uso avançado de chave pode ser usada para definir um ou mais usos da chave pública contida no certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="7ea78-140">**Interface:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="7ea78-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="7ea78-141">**OID:** XCN \_ OID \_ Enhanced \_ Key \_ Usage (2.5.29.37)</span><span class="sxs-lookup"><span data-stu-id="7ea78-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="7ea78-142">FreshestCRL</span><span class="sxs-lookup"><span data-stu-id="7ea78-142">FreshestCRL</span></span>

<span data-ttu-id="7ea78-143">A extensão de CRL mais recente contém o URI da CRL delta.</span><span class="sxs-lookup"><span data-stu-id="7ea78-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="7ea78-144">A mesma sintaxe ASN. 1 é usada para essa extensão e a extensão **CrlDistributionPoints** .</span><span class="sxs-lookup"><span data-stu-id="7ea78-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="7ea78-145">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-146">**OID:** \_CRL mais \_ recente do XCN OID \_ (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="7ea78-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="7ea78-147">Uso de</span><span class="sxs-lookup"><span data-stu-id="7ea78-147">KeyUsage</span></span>

<span data-ttu-id="7ea78-148">A extensão de uso de chave pode ser usada para definir restrições nas operações que podem ser executadas pela chave pública contida no certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="7ea78-149">Por exemplo, você pode especificar que a chave pública seja usada somente para criar uma assinatura digital, assinar uma CRL (lista de certificados revogados) ou criptografar outra chave.</span><span class="sxs-lookup"><span data-stu-id="7ea78-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="7ea78-150">**Interface:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="7ea78-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="7ea78-151">**OID:** \_Uso da \_ chave de OID XCN \_ (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="7ea78-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="7ea78-152">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="7ea78-152">MSApplicationPolicies</span></span>

<span data-ttu-id="7ea78-153">A extensão de políticas de aplicativo da Microsoft pode ser usada por um aplicativo para filtrar certificados com base no uso permitido.</span><span class="sxs-lookup"><span data-stu-id="7ea78-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="7ea78-154">Os usos permitidos são identificados pelos OIDs.</span><span class="sxs-lookup"><span data-stu-id="7ea78-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="7ea78-155">Essa extensão é semelhante à extensão **EnhancedKeyUsage** , mas com semântica mais estrita aplicada à autoridade de certificação pai.</span><span class="sxs-lookup"><span data-stu-id="7ea78-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="7ea78-156">A extensão é específica da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ea78-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="7ea78-157">**Interface:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="7ea78-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="7ea78-158">**OID:** \_ \_ \_ Políticas de certificado de aplicativo XCN OID \_ (1.3.6.1.4.1.311.21.10)</span><span class="sxs-lookup"><span data-stu-id="7ea78-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="7ea78-159">NameConstraints</span><span class="sxs-lookup"><span data-stu-id="7ea78-159">NameConstraints</span></span>

<span data-ttu-id="7ea78-160">A extensão de restrições de nome é usada para identificar o namespace no qual todos os nomes de entidade de certificados em uma hierarquia de certificado devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="7ea78-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="7ea78-161">A extensão é usada somente em um certificado de AC.</span><span class="sxs-lookup"><span data-stu-id="7ea78-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="7ea78-162">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-163">**OID:** \_ \_ \_ Restrições de nome de OID XCN (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="7ea78-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="7ea78-164">PolicyConstraints</span><span class="sxs-lookup"><span data-stu-id="7ea78-164">PolicyConstraints</span></span>

<span data-ttu-id="7ea78-165">A extensão de restrições de política é adicionada aos certificados de autoridade de certificação para restringir a validação de caminho, proibindo o mapeamento de política ou exigindo que cada certificado na hierarquia contenha um identificador de política aceitável.</span><span class="sxs-lookup"><span data-stu-id="7ea78-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="7ea78-166">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-167">**OID:** \_ \_ \_ Restrições de política de OID XCN (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="7ea78-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="7ea78-168">PolicyMappings</span><span class="sxs-lookup"><span data-stu-id="7ea78-168">PolicyMappings</span></span>

<span data-ttu-id="7ea78-169">A extensão de mapeamentos de política é usada para identificar as políticas em uma autoridade de certificação subordinada que correspondem às políticas na AC emissora.</span><span class="sxs-lookup"><span data-stu-id="7ea78-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="7ea78-170">O valor de extensão contém uma sequência de emissão de CA e mapeamentos de política de autoridade de certificação subordinados representados por identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="7ea78-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="7ea78-171">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-172">**OID:** \_ \_ \_ Mapeamentos de política de OID XCN (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="7ea78-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="7ea78-173">PrivateKeyUsagePeriod</span><span class="sxs-lookup"><span data-stu-id="7ea78-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="7ea78-174">A extensão do período de uso de chave privada é usada para especificar um período de validade diferente para a chave privada do que para o certificado ao qual a chave está associada.</span><span class="sxs-lookup"><span data-stu-id="7ea78-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="7ea78-175">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-176">**OID:** \_ \_ \_ Período de uso do XCN OID PRIVATEKEY \_ (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="7ea78-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="7ea78-177">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="7ea78-177">SmimeCapabilities</span></span>

<span data-ttu-id="7ea78-178">A extensão de recursos de extensões S/MIME (Internet Mail Extensions) segura/multipropósito pode ser usada para relatar os recursos de descriptografia de um destinatário de email ao remetente da mensagem de email para que o remetente possa escolher o algoritmo de criptografia mais seguro com suporte de ambas as partes.</span><span class="sxs-lookup"><span data-stu-id="7ea78-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="7ea78-179">O valor de extensão contém uma coleção de OIDs de algoritmo de criptografia simétrica e um nível de criptografia opcional para cada um.</span><span class="sxs-lookup"><span data-stu-id="7ea78-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="7ea78-180">**Interface:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="7ea78-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="7ea78-181">**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)</span><span class="sxs-lookup"><span data-stu-id="7ea78-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="7ea78-182">SubjectDirectoryAttributes</span><span class="sxs-lookup"><span data-stu-id="7ea78-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="7ea78-183">A extensão de atributos de diretório de assunto pode ser usada para transmitir atributos de identificação, como a nacionalidade da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="7ea78-184">O valor da extensão é uma sequência de pares de valores OID.</span><span class="sxs-lookup"><span data-stu-id="7ea78-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="7ea78-185">**Interface:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7ea78-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7ea78-186">**OID:** XCN \_ OID \_ Subject \_ dir \_ ATTRS (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="7ea78-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="7ea78-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="7ea78-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="7ea78-188">A extensão do identificador de chave da entidade pode ser usada para diferenciar várias chaves públicas mantidas pela entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="7ea78-189">O valor da extensão é geralmente um hash SHA-1 da chave.</span><span class="sxs-lookup"><span data-stu-id="7ea78-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="7ea78-190">**Interface:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="7ea78-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="7ea78-191">**OID:** \_ \_ \_ Identificador de chave de entidade XCN OID \_ (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="7ea78-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="7ea78-192">Modelo</span><span class="sxs-lookup"><span data-stu-id="7ea78-192">Template</span></span>

<span data-ttu-id="7ea78-193">A extensão do modelo pode ser usada para identificar o modelo da versão 2 a ser usado ao emitir ou renovar um certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="7ea78-194">O valor da extensão contém a OID do modelo e as informações de versão opcionais.</span><span class="sxs-lookup"><span data-stu-id="7ea78-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="7ea78-195">A extensão é específica da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ea78-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="7ea78-196">**Interface:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="7ea78-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="7ea78-197">**OID:** \_ \_ Modelo de certificado OID XCN \_ (1.3.6.1.4.1.311.21.7)</span><span class="sxs-lookup"><span data-stu-id="7ea78-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="7ea78-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="7ea78-198">TemplateName</span></span>

<span data-ttu-id="7ea78-199">A extensão do nome do modelo pode ser usada para identificar o modelo da versão 1 a ser usado ao emitir ou renovar um certificado.</span><span class="sxs-lookup"><span data-stu-id="7ea78-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="7ea78-200">O valor da extensão contém o nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="7ea78-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="7ea78-201">A extensão é específica da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ea78-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="7ea78-202">**Interface:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="7ea78-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="7ea78-203">**OID:** \_ \_ \_ Extensão certtype de registro \_ do XCN OID (1.3.6.1.4.1.311.20.2)</span><span class="sxs-lookup"><span data-stu-id="7ea78-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ea78-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ea78-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea78-205">Extensões</span><span class="sxs-lookup"><span data-stu-id="7ea78-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



