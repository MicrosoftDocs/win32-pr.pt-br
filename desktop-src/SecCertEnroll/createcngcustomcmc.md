---
description: Cria um objeto de solicitação CMC com base em uma solicitação PKCS 10 aninhada interna \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296195"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="d598e-103">createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="d598e-103">createCNGCustomCMC</span></span>

<span data-ttu-id="d598e-104">O exemplo createCNGCustomCMC cria um objeto de solicitação CMC por meio de uma solicitação PKCS 10 aninhada interna \# .</span><span class="sxs-lookup"><span data-stu-id="d598e-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="d598e-105">A solicitação interna é criada usando uma [*chave privada*](/windows/desktop/SecGloss/p-gly)assimétrica.</span><span class="sxs-lookup"><span data-stu-id="d598e-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="d598e-106">A chave privada é criada usando o provedor criptográfico da API de criptografia: próxima geração (CNG) e o algoritmo especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d598e-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="d598e-107">Opções personalizadas, como política de exportação e nível de proteção de chave, também são definidas na chave privada.</span><span class="sxs-lookup"><span data-stu-id="d598e-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="d598e-108">Local</span><span class="sxs-lookup"><span data-stu-id="d598e-108">Location</span></span>

<span data-ttu-id="d598e-109">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ createCNGCustomCMC.</span><span class="sxs-lookup"><span data-stu-id="d598e-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="d598e-110">Discussão</span><span class="sxs-lookup"><span data-stu-id="d598e-110">Discussion</span></span>

<span data-ttu-id="d598e-111">O exemplo de createCNGCustomCMC:</span><span class="sxs-lookup"><span data-stu-id="d598e-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="d598e-112">Processa os seguintes argumentos de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="d598e-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="d598e-113">O nome de um [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) CNG (CSP).</span><span class="sxs-lookup"><span data-stu-id="d598e-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="d598e-114">O nome do algoritmo usado para gerar uma chave privada assimétrica.</span><span class="sxs-lookup"><span data-stu-id="d598e-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="d598e-115">O nome do algoritmo usado para [*aplicar o hash*](/windows/desktop/SecGloss/h-gly) à [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="d598e-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="d598e-116">Um arquivo de saída no qual salvar a solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="d598e-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="d598e-117">Uma cadeia de caracteres opcional (AlternateSignature) que, se presente, especifica que um algoritmo de assinatura discreto em vez de combinado seja usado.</span><span class="sxs-lookup"><span data-stu-id="d598e-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="d598e-118">Para obter mais informações, consulte a propriedade [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .</span><span class="sxs-lookup"><span data-stu-id="d598e-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="d598e-119">Cria um objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e define as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="d598e-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="d598e-120">**LegacyCsp**</span><span class="sxs-lookup"><span data-stu-id="d598e-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="d598e-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d598e-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="d598e-122">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="d598e-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="d598e-123">**Proteção contra keyprotection**</span><span class="sxs-lookup"><span data-stu-id="d598e-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="d598e-124">**ExportPolicy**</span><span class="sxs-lookup"><span data-stu-id="d598e-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="d598e-125">Cria uma chave privada assimétrica.</span><span class="sxs-lookup"><span data-stu-id="d598e-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="d598e-126">Cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e inicializa-o usando a chave privada.</span><span class="sxs-lookup"><span data-stu-id="d598e-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="d598e-127">Cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o objeto de \# solicitação PKCS 10 criado na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="d598e-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="d598e-128">Define o sinalizador de algoritmo de assinatura alternativo como **Variant \_ true** ou **Variant \_ false** , dependendo se uma cadeia de caracteres de assinatura alternativa é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d598e-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="d598e-129">Para obter mais informações, consulte [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span><span class="sxs-lookup"><span data-stu-id="d598e-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="d598e-130">Cria um [](/windows/desktop/SecGloss/h-gly) [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) de algoritmo de hash (OID) do nome do algoritmo especificado na linha de comando e define o OID no objeto de solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="d598e-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="d598e-131">Assina a solicitação de certificado e a codifica usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="d598e-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="d598e-132">Recupera uma cadeia de caracteres que contém a solicitação codificada de certificado CMC e salva-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d598e-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="d598e-133">A função EncodeToFileW é definida em EnrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="d598e-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d598e-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d598e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d598e-135">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="d598e-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="d598e-136">\#Solicitação PKCS 10</span><span class="sxs-lookup"><span data-stu-id="d598e-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="d598e-137">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="d598e-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="d598e-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="d598e-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
