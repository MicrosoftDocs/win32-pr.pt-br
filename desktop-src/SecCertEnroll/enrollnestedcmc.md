---
description: Lê uma solicitação de certificado CMC existente de um arquivo, a encapsula em outra solicitação de CMC, assina essa solicitação externa, envia-a para uma autoridade de certificação (CA) e salva a resposta do certificado da autoridade de certificação em um arquivo.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164281"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="64dee-103">enrollNestedCMC</span><span class="sxs-lookup"><span data-stu-id="64dee-103">enrollNestedCMC</span></span>

<span data-ttu-id="64dee-104">O exemplo enrollNestedCMC lê uma solicitação de certificado CMC existente de um arquivo, a encapsula em outra solicitação de CMC, assina essa solicitação externa, envia-a para uma autoridade de certificação (CA) e salva a resposta do certificado da autoridade de certificação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="64dee-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="64dee-105">Local</span><span class="sxs-lookup"><span data-stu-id="64dee-105">Location</span></span>

<span data-ttu-id="64dee-106">Quando você instala o SDK (Kit de desenvolvimento de software) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ SDKs do Microsoft \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Enrollment \\ vc \\ enrollNestedCMC.</span><span class="sxs-lookup"><span data-stu-id="64dee-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="64dee-107">Discussão</span><span class="sxs-lookup"><span data-stu-id="64dee-107">Discussion</span></span>

<span data-ttu-id="64dee-108">O exemplo de enrollNestedCMC:</span><span class="sxs-lookup"><span data-stu-id="64dee-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="64dee-109">Processa os seguintes argumentos de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="64dee-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="64dee-110">O nome do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="64dee-110">The name of the input file.</span></span>
    -   <span data-ttu-id="64dee-111">O nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="64dee-111">The name of the output file.</span></span>
    -   <span data-ttu-id="64dee-112">Um modelo de solicitação opcional.</span><span class="sxs-lookup"><span data-stu-id="64dee-112">An optional request template.</span></span>
2.  <span data-ttu-id="64dee-113">Lê uma solicitação CMC existente de um arquivo como uma matriz de bytes codificada em base63, converte a matriz de bytes em um **BSTR**, cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e usa o **BSTR** para inicializar o objeto de solicitação.</span><span class="sxs-lookup"><span data-stu-id="64dee-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="64dee-114">O objeto inicializado se torna a solicitação interna.</span><span class="sxs-lookup"><span data-stu-id="64dee-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="64dee-115">Usa o objeto de solicitação interna criado e inicializado na etapa anterior para inicializar outra solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="64dee-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="64dee-116">Recupera um certificado de autenticação existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo especificado na linha de comando e tenta registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="64dee-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="64dee-117">As funções findCertByTemplate e enrollCertByTemplate são definidas em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="64dee-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="64dee-118">Recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) da solicitação CMC externa, cria um novo objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado de autenticação recuperado e o adiciona à coleção.</span><span class="sxs-lookup"><span data-stu-id="64dee-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="64dee-119">Codifica a solicitação CMC usando Distinguished Encoding Rules (DER) e recupera a solicitação como um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="64dee-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="64dee-120">Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="64dee-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="64dee-121">Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="64dee-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="64dee-122">Verifica o status do processo de registro e salva a resposta do certificado da autoridade de certificação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="64dee-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="64dee-123">A função EncodeToFileW é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="64dee-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64dee-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64dee-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64dee-125">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="64dee-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="64dee-126">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="64dee-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
