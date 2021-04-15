---
description: Cria um \# objeto de solicitação PKCS 7 para renovar um certificado existente. O objeto de solicitação usa um novo par de chaves, mas retém o provedor criptográfico associado ao certificado que está sendo renovado.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505973"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="73749-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="73749-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="73749-105">O exemplo enrollRenewalPKCS7 cria um \# objeto de solicitação PKCS 7 para renovar um certificado existente.</span><span class="sxs-lookup"><span data-stu-id="73749-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="73749-106">O objeto de solicitação usa um novo par de chaves, mas retém o provedor criptográfico associado ao certificado que está sendo renovado.</span><span class="sxs-lookup"><span data-stu-id="73749-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="73749-107">Local</span><span class="sxs-lookup"><span data-stu-id="73749-107">Location</span></span>

<span data-ttu-id="73749-108">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="73749-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="73749-109">Discussão</span><span class="sxs-lookup"><span data-stu-id="73749-109">Discussion</span></span>

<span data-ttu-id="73749-110">O exemplo de enrollRenewalPKCS7:</span><span class="sxs-lookup"><span data-stu-id="73749-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="73749-111">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="73749-111">Processes the command line arguments.</span></span> <span data-ttu-id="73749-112">A linha de comando deve conter o nome do modelo usado para criar a solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="73749-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="73749-113">Recupera um certificado existente usando o nome do modelo especificado na linha de comando ou, se um certificado não puder ser encontrado, tentará registrá-lo usando o modelo.</span><span class="sxs-lookup"><span data-stu-id="73749-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="73749-114">As funções findCertByTemplate e enrollCertByTemplate são definidas em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="73749-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="73749-115">Verifica a cadeia de certificados e converte o certificado em um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="73749-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="73749-116">Cria um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e o inicializa usando o certificado existente.</span><span class="sxs-lookup"><span data-stu-id="73749-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="73749-117">Como o parâmetro *inheritoptions* é definido como InheritDefault, um novo par de chaves é criado para a solicitação, mas o provedor criptográfico no certificado existente é usado.</span><span class="sxs-lookup"><span data-stu-id="73749-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="73749-118">Para obter mais informações, consulte o método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .</span><span class="sxs-lookup"><span data-stu-id="73749-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="73749-119">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o \# objeto de solicitação PKCS 7, tenta registrá-lo com a AC e monitora o status do processo de registro.</span><span class="sxs-lookup"><span data-stu-id="73749-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="73749-120">A função checkEnrollStatus é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="73749-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73749-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73749-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73749-122">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="73749-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="73749-123">\#Solicitação de renovação PKCS 7</span><span class="sxs-lookup"><span data-stu-id="73749-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="73749-124">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="73749-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



