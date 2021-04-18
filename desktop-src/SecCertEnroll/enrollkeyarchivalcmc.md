---
description: Cria uma solicitação de certificado CMC para arquivar uma chave privada em uma autoridade de certificação (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758170"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="38a44-103">enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="38a44-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="38a44-104">O exemplo enrollKeyArchivalCMC cria uma solicitação de certificado CMC para arquivar uma chave privada em uma autoridade de certificação (CA).</span><span class="sxs-lookup"><span data-stu-id="38a44-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="38a44-105">Para obter mais informações, consulte [solicitação de arquivamento de chave CMC](cmc-key-archival-request.md).</span><span class="sxs-lookup"><span data-stu-id="38a44-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="38a44-106">Local</span><span class="sxs-lookup"><span data-stu-id="38a44-106">Location</span></span>

<span data-ttu-id="38a44-107">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollKeyArchivalCMC.</span><span class="sxs-lookup"><span data-stu-id="38a44-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="38a44-108">Discussão</span><span class="sxs-lookup"><span data-stu-id="38a44-108">Discussion</span></span>

<span data-ttu-id="38a44-109">O exemplo de enrollKeyArchivalCMC:</span><span class="sxs-lookup"><span data-stu-id="38a44-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="38a44-110">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="38a44-110">Processes the command line arguments.</span></span> <span data-ttu-id="38a44-111">A linha de comando deve conter o nome do modelo de certificado a ser usado para o registro.</span><span class="sxs-lookup"><span data-stu-id="38a44-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="38a44-112">Cria um objeto de solicitação de certificado [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa para um contexto de usuário final usando o nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="38a44-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="38a44-113">Define a propriedade [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) na solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="38a44-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="38a44-114">Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="38a44-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="38a44-115">Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa para recuperar o certificado do Exchange para a autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="38a44-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="38a44-116">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando a solicitação CMC, cria uma cadeia de caracteres codificada em base64 que contém a solicitação de arquivamento de chave e a envia para a autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="38a44-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38a44-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38a44-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a44-118">Solicitação de arquivamento de chave CMC</span><span class="sxs-lookup"><span data-stu-id="38a44-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="38a44-119">Solicitação de CMC</span><span class="sxs-lookup"><span data-stu-id="38a44-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="38a44-120">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="38a44-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
