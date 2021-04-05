---
description: Inicializa um \# objeto de solicitação de certificado PKCS 10, encapsula-o em um objeto de solicitação CMC, envia a solicitação CMC para uma AC (autoridade de certificação) corporativa e salva o certificado retornado pela autoridade de certificação em um arquivo.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647456"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="4a98e-103">enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="4a98e-103">enrollFromPublicKey</span></span>

<span data-ttu-id="4a98e-104">O exemplo enrollFromPublicKey Inicializa um \# objeto de solicitação de certificado PKCS 10, o encapsula em um objeto de solicitação CMC, envia a solicitação CMC para uma AC (autoridade de certificação) corporativa e salva o certificado retornado pela autoridade de certificação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4a98e-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="4a98e-105">Local</span><span class="sxs-lookup"><span data-stu-id="4a98e-105">Location</span></span>

<span data-ttu-id="4a98e-106">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="4a98e-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="4a98e-107">Discussão</span><span class="sxs-lookup"><span data-stu-id="4a98e-107">Discussion</span></span>

<span data-ttu-id="4a98e-108">O exemplo de enrollFromPublicKey:</span><span class="sxs-lookup"><span data-stu-id="4a98e-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="4a98e-109">Processa os seguintes argumentos de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="4a98e-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="4a98e-110">O nome de um modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="4a98e-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="4a98e-111">O nome de um arquivo no qual salvar o certificado instalado como uma matriz de bytes codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="4a98e-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="4a98e-112">Um nome de modelo de certificado de assinatura opcional.</span><span class="sxs-lookup"><span data-stu-id="4a98e-112">An optional signing certificate template name.</span></span> <span data-ttu-id="4a98e-113">O modelo é usado para criar um certificado de assinatura se não houver nenhum no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="4a98e-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="4a98e-114">Cria um objeto de chave privada [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e chama o método [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) para criar uma chave privada assimétrica usando o provedor criptográfico padrão, o tamanho da chave e os valores [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) para o computador atual.</span><span class="sxs-lookup"><span data-stu-id="4a98e-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="4a98e-115">Recupera a parte da chave pública do objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .</span><span class="sxs-lookup"><span data-stu-id="4a98e-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="4a98e-116">Cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e o inicializa usando o modelo especificado na linha de comando e a chave pública.</span><span class="sxs-lookup"><span data-stu-id="4a98e-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="4a98e-117">Cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o objeto de \# solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="4a98e-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="4a98e-118">Recupera um certificado de autenticação existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo especificado na linha de comando e tenta registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="4a98e-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="4a98e-119">O findCertByKeyUsage é definido em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="4a98e-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="4a98e-120">Verifica a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="4a98e-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="4a98e-121">Cria um objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado de autenticação, recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) do objeto de solicitação CMC e adiciona o objeto de certificado de autenticação à coleção.</span><span class="sxs-lookup"><span data-stu-id="4a98e-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="4a98e-122">Codifica a solicitação CMC usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="4a98e-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="4a98e-123">Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="4a98e-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="4a98e-124">Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="4a98e-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="4a98e-125">Verifica o status do processo de registro e salva o certificado instalado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4a98e-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="4a98e-126">A função EncodeToFileW é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="4a98e-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a98e-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a98e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a98e-128">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="4a98e-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="4a98e-129">\#Solicitação PKCS 10</span><span class="sxs-lookup"><span data-stu-id="4a98e-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="4a98e-130">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="4a98e-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
