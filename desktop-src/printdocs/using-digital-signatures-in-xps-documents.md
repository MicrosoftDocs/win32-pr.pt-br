---
description: Este tópico lista considerações para usar a API de assinatura digital XPS para adicionar assinaturas digitais a um documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso da API de assinatura digital do XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828307"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="62471-103">Uso da API de assinatura digital do XPS</span><span class="sxs-lookup"><span data-stu-id="62471-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="62471-104">Este tópico lista considerações para usar a API de assinatura digital XPS para adicionar assinaturas digitais a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="62471-105">A API de assinatura digital XPS permite que os aplicativos solicitem aos usuários que assinem documentos XPS e verifiquem as assinaturas encontradas em documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="62471-106">A API de assinatura digital XPS pode ser aplicada a um documento XPS sem carregá-lo em um OM XPS e pode ser usada em fluxos de documento XPS que são serializados de um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="62471-107">A seção [tarefas de programação da API de assinatura digital XPS](#xps-digital-signature-api-programming-tasks) contém tópicos que descrevem como programar com a API de assinatura digital XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="62471-108">Este tópico lista as seguintes considerações para usar a API de assinatura digital XPS ao adicionar suporte à assinatura digital a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="62471-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="62471-109">Tarefas de programação de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="62471-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="62471-110">Observações especiais sobre a programação da API de assinatura digital do XPS</span><span class="sxs-lookup"><span data-stu-id="62471-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="62471-111">Verificando assinaturas digitais em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="62471-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="62471-112">Política de assinatura de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="62471-113">Inserindo uma cadeia de certificados</span><span class="sxs-lookup"><span data-stu-id="62471-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="62471-114">Usando a estrutura de contexto do certificado \_</span><span class="sxs-lookup"><span data-stu-id="62471-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="62471-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62471-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="62471-116">Tarefas de programação de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="62471-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="62471-117">Esta seção contém tópicos que descrevem como executar tarefas de programação usando a API de assinatura digital XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="62471-118">Tarefas comuns de programação de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="62471-119">Inicializar o Gerenciador de assinatura</span><span class="sxs-lookup"><span data-stu-id="62471-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="62471-120">Assinar um documento</span><span class="sxs-lookup"><span data-stu-id="62471-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="62471-121">Adicionar uma solicitação de assinatura a um documento XPS</span><span class="sxs-lookup"><span data-stu-id="62471-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="62471-122">Verificar assinaturas de documento</span><span class="sxs-lookup"><span data-stu-id="62471-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="62471-123">Tarefas adicionais de programação de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="62471-124">Carregar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="62471-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="62471-125">Verificar se um certificado dá suporte a um método de assinatura</span><span class="sxs-lookup"><span data-stu-id="62471-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="62471-126">Verificar se o sistema dá suporte a um método Digest</span><span class="sxs-lookup"><span data-stu-id="62471-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="62471-127">Inserir cadeias de certificados em um documento</span><span class="sxs-lookup"><span data-stu-id="62471-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="62471-128">Observações especiais sobre a programação da API de assinatura digital do XPS</span><span class="sxs-lookup"><span data-stu-id="62471-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="62471-129">Os tópicos a seguir exigem alguma consideração especial quando você usa a API de assinatura digital XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="62471-130">Verificando assinaturas digitais em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="62471-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="62471-131">Política de assinatura de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="62471-132">Inserindo uma cadeia de certificados</span><span class="sxs-lookup"><span data-stu-id="62471-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="62471-133">Usando a estrutura de contexto do certificado \_</span><span class="sxs-lookup"><span data-stu-id="62471-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="62471-134">Verificando assinaturas digitais em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="62471-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="62471-135">[**IXpsSignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) verifica apenas o conteúdo assinado para determinar que ele não foi alterado desde que foi assinado.</span><span class="sxs-lookup"><span data-stu-id="62471-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="62471-136">**IXpsSignature:: Verify** não verifica nenhum dos certificados que foram usados para assinar o conteúdo do documento.</span><span class="sxs-lookup"><span data-stu-id="62471-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="62471-137">Para obter mais informações sobre certificados e criptografia, consulte [sobre criptografia](/windows/desktop/SecCrypto/about-cryptography).</span><span class="sxs-lookup"><span data-stu-id="62471-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="62471-138">Para obter um exemplo de como verificar assinaturas de documentos em um programa, consulte [verificar assinaturas e certificados de documentos](verify-document-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="62471-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="62471-139">Política de assinatura de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="62471-140">A política de assinatura de assinatura digital determina quais partes de um documento XPS são assinadas.</span><span class="sxs-lookup"><span data-stu-id="62471-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="62471-141">Uma opção de política de assinatura é assinar as relações de assinatura que começam da parte de origem da assinatura.</span><span class="sxs-lookup"><span data-stu-id="62471-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="62471-142">Como as relações de assinatura são alteradas com cada assinatura que é adicionada, as assinaturas feitas sob essa política serão interrompidas quando novas assinaturas forem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="62471-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="62471-143">Certifique-se de entender claramente as implicações e os efeitos da definição dessa política; caso contrário, pode ocorrer um comportamento inesperado ou indesejado.</span><span class="sxs-lookup"><span data-stu-id="62471-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="62471-144">Para obter mais informações sobre diretivas de assinatura, consulte [**\_ \_ política de sinal de XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span><span class="sxs-lookup"><span data-stu-id="62471-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="62471-145">Inserindo uma cadeia de certificados</span><span class="sxs-lookup"><span data-stu-id="62471-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="62471-146">Os certificados que compõem a cadeia de confiança de um certificado específico podem ser adicionados a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="62471-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="62471-147">A inserção desses certificados pode facilitar, em cenários off-line, para que um aplicativo Verifique os certificados que uma assinatura digital usa.</span><span class="sxs-lookup"><span data-stu-id="62471-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="62471-148">Para obter mais informações sobre como inserir certificados em um documento XPS, consulte [Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="62471-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="62471-149">Usando a estrutura de contexto do certificado \_</span><span class="sxs-lookup"><span data-stu-id="62471-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="62471-150">As estruturas de [**\_ informações**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) de certificado e de [**\_ contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado são as principais estruturas de dados que mantêm informações sobre certificados.</span><span class="sxs-lookup"><span data-stu-id="62471-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="62471-151">Para obter mais informações sobre como usar essas estruturas, consulte [usando uma \_ estrutura de dados de informações de certificado](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span><span class="sxs-lookup"><span data-stu-id="62471-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="62471-152">[**Certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) As estruturas de contexto que são retornadas pelas funções da API de criptografia devem ser liberadas quando não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="62471-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="62471-153">Para liberar uma estrutura de **\_ contexto de certificado** , chame a função [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="62471-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62471-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62471-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62471-155">Tarefas comuns de programação de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="62471-156">Tarefas adicionais de programação de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="62471-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="62471-157">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="62471-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="62471-158">**informações de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="62471-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="62471-159">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="62471-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="62471-160">**\_política de assinatura de XPS \_**</span><span class="sxs-lookup"><span data-stu-id="62471-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="62471-161">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="62471-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
