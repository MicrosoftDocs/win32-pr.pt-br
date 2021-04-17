---
description: Cria uma solicitação personalizada de PKCS \# 10 e tenta registrá-la em uma CA (autoridade de certificação) corporativa.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762033"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="0c64e-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="0c64e-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="0c64e-104">O exemplo de enrollCustomPKCS10 \_ 2 cria uma solicitação personalizada de PKCS \# 10 e tenta registrá-la em uma CA ( [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) ) corporativa.</span><span class="sxs-lookup"><span data-stu-id="0c64e-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="0c64e-105">Local</span><span class="sxs-lookup"><span data-stu-id="0c64e-105">Location</span></span>

<span data-ttu-id="0c64e-106">Ao instalar o Microsoft Windows Software Development Kit (SDK), o exemplo é instalado por padrão na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ vc \\ enrollCustomPKCS10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="0c64e-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0c64e-107">Discussão</span><span class="sxs-lookup"><span data-stu-id="0c64e-107">Discussion</span></span>

<span data-ttu-id="0c64e-108">O exemplo de enrollCustomPKCS10 \_ 2:</span><span class="sxs-lookup"><span data-stu-id="0c64e-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="0c64e-109">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0c64e-109">Processes the command line arguments.</span></span> <span data-ttu-id="0c64e-110">A linha de comando deve conter o nome de um modelo e o nome de um provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="0c64e-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="0c64e-111">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e o inicializa usando o nome do modelo especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0c64e-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="0c64e-112">Recupera a [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly) do objeto de registro.</span><span class="sxs-lookup"><span data-stu-id="0c64e-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="0c64e-113">Recupera a solicitação PKCS \# 10 interna do objeto de solicitação de certificado obtido na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="0c64e-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="0c64e-114">Recupera uma [*chave privada*](/windows/desktop/SecGloss/p-gly) da solicitação PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="0c64e-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="0c64e-115">Cria uma coleção [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) e adiciona os provedores criptográficos disponíveis à coleção e, em seguida, recupera um objeto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) para o provedor especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0c64e-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="0c64e-116">Define o objeto de status na chave privada.</span><span class="sxs-lookup"><span data-stu-id="0c64e-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="0c64e-117">Tenta registrar a [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="0c64e-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c64e-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c64e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c64e-119">\#Solicitação PKCS 10</span><span class="sxs-lookup"><span data-stu-id="0c64e-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="0c64e-120">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="0c64e-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
