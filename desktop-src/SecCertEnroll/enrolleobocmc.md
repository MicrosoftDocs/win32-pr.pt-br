---
description: Cria uma solicitação de certificado CMC em nome de outro usuário e registra o usuário em uma hierarquia de certificado.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501969"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="a11e7-103">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="a11e7-103">enrollEOBOCMC</span></span>

<span data-ttu-id="a11e7-104">O exemplo enrollEOBOCMC cria uma solicitação de certificado CMC em nome de outro usuário e registra o usuário em uma hierarquia de certificados.</span><span class="sxs-lookup"><span data-stu-id="a11e7-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="a11e7-105">O registro em nome de outro usuário requer que a solicitação de certificado seja assinada usando um certificado de agente de registro.</span><span class="sxs-lookup"><span data-stu-id="a11e7-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="a11e7-106">Local</span><span class="sxs-lookup"><span data-stu-id="a11e7-106">Location</span></span>

<span data-ttu-id="a11e7-107">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollEOBOCMC.</span><span class="sxs-lookup"><span data-stu-id="a11e7-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="a11e7-108">Discussão</span><span class="sxs-lookup"><span data-stu-id="a11e7-108">Discussion</span></span>

<span data-ttu-id="a11e7-109">O exemplo de enrollEOBOCMC:</span><span class="sxs-lookup"><span data-stu-id="a11e7-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="a11e7-110">Processa os seguintes argumentos de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="a11e7-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="a11e7-111">O nome de um modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="a11e7-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="a11e7-112">O nome do usuário que está solicitando o certificado.</span><span class="sxs-lookup"><span data-stu-id="a11e7-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="a11e7-113">O nome de um arquivo PFX (troca de informações pessoais) no qual salvar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a11e7-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="a11e7-114">Uma senha a ser usada com o arquivo PFX.</span><span class="sxs-lookup"><span data-stu-id="a11e7-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="a11e7-115">Um nome de modelo de agente de registro opcional.</span><span class="sxs-lookup"><span data-stu-id="a11e7-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="a11e7-116">O modelo é usado para criar um certificado de agente de registro se não houver nenhum no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="a11e7-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="a11e7-117">Cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o modelo de certificado especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a11e7-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="a11e7-118">Adiciona o nome do solicitante ao objeto de solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="a11e7-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="a11e7-119">Recupera um certificado de agente de registro existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo de agente de registro especificado na linha de comando e tenta registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="a11e7-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="a11e7-120">Verifica a cadeia de certificados que contém o certificado do agente de registro.</span><span class="sxs-lookup"><span data-stu-id="a11e7-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="a11e7-121">Cria um objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado do agente de registro, recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) do objeto de solicitação CMC e adiciona o objeto de certificado de autenticação do agente de registro à coleção.</span><span class="sxs-lookup"><span data-stu-id="a11e7-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="a11e7-122">O objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) discutido na próxima etapa usa o certificado para assinar a solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="a11e7-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="a11e7-123">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando a solicitação CMC, tenta registrá-lo e verifica o progresso do processo de registro.</span><span class="sxs-lookup"><span data-stu-id="a11e7-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="a11e7-124">Exporta o certificado instalado para um arquivo PFX.</span><span class="sxs-lookup"><span data-stu-id="a11e7-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="a11e7-125">O arquivo é protegido usando a senha especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a11e7-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="a11e7-126">A função EncodeToFileW é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="a11e7-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="a11e7-127">Exclui o certificado do repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="a11e7-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="a11e7-128">As funções usadas no exemplo de código a seguir podem ser encontradas na documentação do CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a11e7-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="a11e7-129">Exclui a chave privada do computador.</span><span class="sxs-lookup"><span data-stu-id="a11e7-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a11e7-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a11e7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a11e7-131">Solicitação EOBO de CMC</span><span class="sxs-lookup"><span data-stu-id="a11e7-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="a11e7-132">\#Solicitação PKCS 10</span><span class="sxs-lookup"><span data-stu-id="a11e7-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="a11e7-133">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="a11e7-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



