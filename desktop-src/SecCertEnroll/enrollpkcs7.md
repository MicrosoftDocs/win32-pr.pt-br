---
description: Cria uma \# solicitação PKCS 7 de um certificado existente herdando as chaves pública e privada e o modelo de certificado.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646779"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="50ad7-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="50ad7-103">enrollPKCS7</span></span>

<span data-ttu-id="50ad7-104">O exemplo enrollPKCS7 cria uma \# solicitação PKCS 7 de um certificado existente herdando as chaves pública e privada e o modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="50ad7-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="50ad7-105">O certificado existente é usado para assinar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="50ad7-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="50ad7-106">Este exemplo registra o usuário em uma hierarquia de certificado e instala a resposta do certificado.</span><span class="sxs-lookup"><span data-stu-id="50ad7-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="50ad7-107">O exemplo usa um certificado existente para registrar e instalar um novo.</span><span class="sxs-lookup"><span data-stu-id="50ad7-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="50ad7-108">Para obter mais informações sobre como renovar um certificado existente, consulte [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span><span class="sxs-lookup"><span data-stu-id="50ad7-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="50ad7-109">Local</span><span class="sxs-lookup"><span data-stu-id="50ad7-109">Location</span></span>

<span data-ttu-id="50ad7-110">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollPKCS7.</span><span class="sxs-lookup"><span data-stu-id="50ad7-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="50ad7-111">Discussão</span><span class="sxs-lookup"><span data-stu-id="50ad7-111">Discussion</span></span>

<span data-ttu-id="50ad7-112">O exemplo de enrollPKCS7:</span><span class="sxs-lookup"><span data-stu-id="50ad7-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="50ad7-113">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="50ad7-113">Processes the command line arguments.</span></span> <span data-ttu-id="50ad7-114">A linha de comando deve conter o nome do modelo de certificado usado para localizar um certificado existente.</span><span class="sxs-lookup"><span data-stu-id="50ad7-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="50ad7-115">Recupera um certificado existente usando o nome do modelo especificado na linha de comando ou, se um certificado não puder ser encontrado, tentará registrar um novo criado usando o modelo.</span><span class="sxs-lookup"><span data-stu-id="50ad7-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="50ad7-116">As funções findCertByTemplate e enrollCertByTemplate são definidas em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="50ad7-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="50ad7-117">Verifica a cadeia de certificados e converte o certificado em um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="50ad7-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="50ad7-118">Cria um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e o inicializa usando o certificado existente.</span><span class="sxs-lookup"><span data-stu-id="50ad7-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="50ad7-119">O novo \# objeto de solicitação PKCS 7 herda as chaves pública e privada e o modelo do certificado existente.</span><span class="sxs-lookup"><span data-stu-id="50ad7-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="50ad7-120">Cria um objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado existente e o adiciona ao \# objeto de solicitação PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="50ad7-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="50ad7-121">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o \# objeto de solicitação PKCS 7, tenta registrá-lo com a AC e monitora o status do processo de registro.</span><span class="sxs-lookup"><span data-stu-id="50ad7-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="50ad7-122">A função checkEnrollStatus é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="50ad7-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50ad7-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50ad7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50ad7-124">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="50ad7-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="50ad7-125">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="50ad7-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



