---
description: Cria uma solicitação de certificado CMC e registra um computador em uma hierarquia de certificado.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647458"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="326d8-103">enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="326d8-103">enrollCustomCMC</span></span>

<span data-ttu-id="326d8-104">O exemplo enrollCustomCMC cria uma solicitação de certificado CMC e registra um computador em uma hierarquia de certificado.</span><span class="sxs-lookup"><span data-stu-id="326d8-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="326d8-105">Local</span><span class="sxs-lookup"><span data-stu-id="326d8-105">Location</span></span>

<span data-ttu-id="326d8-106">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollCustomCMC.</span><span class="sxs-lookup"><span data-stu-id="326d8-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="326d8-107">Discussão</span><span class="sxs-lookup"><span data-stu-id="326d8-107">Discussion</span></span>

<span data-ttu-id="326d8-108">O exemplo de enrollCustomCMC:</span><span class="sxs-lookup"><span data-stu-id="326d8-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="326d8-109">Processa os seguintes argumentos de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="326d8-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="326d8-110">Um par de nome/valor personalizado para adicionar à solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="326d8-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="326d8-111">Um nome de entidade alternativo.</span><span class="sxs-lookup"><span data-stu-id="326d8-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="326d8-112">Um OID (identificador de objeto) para a extensão EKU (uso avançado de chave).</span><span class="sxs-lookup"><span data-stu-id="326d8-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="326d8-113">Cria um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e inicializa-o usando o contexto do computador.</span><span class="sxs-lookup"><span data-stu-id="326d8-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="326d8-114">Usa a \# solicitação PKCS 10 para inicializar um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="326d8-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="326d8-115">Cria um objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) usando o OID especificado na linha de comando e o adiciona à coleção de extensões para a solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="326d8-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="326d8-116">Cria o objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) usando o nome especificado na linha de comando, adiciona-o à coleção [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , usa a coleção para inicializar uma extensão [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) e a adiciona à coleção de extensões para a solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="326d8-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="326d8-117">Cria um objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) usando o nome e o valor especificados na linha de comando e adiciona-o à coleção [**IX509NAMEVALUEPAIRS**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) na solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="326d8-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="326d8-118">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o objeto de solicitação CMC e recupera uma cadeia de caracteres que contém uma solicitação codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="326d8-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="326d8-119">Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="326d8-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="326d8-120">Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="326d8-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="326d8-121">Verifica o status de envio e, se for bem-sucedido, instala o certificado no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="326d8-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="326d8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="326d8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="326d8-123">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="326d8-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="326d8-124">\#Solicitação PKCS 10</span><span class="sxs-lookup"><span data-stu-id="326d8-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="326d8-125">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="326d8-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
