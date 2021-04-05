---
description: Registra um usuário final com uma autoridade de certificação (CA) usando um modelo, o nome da entidade e o comprimento, em bits, da chave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011246"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="70a78-103">enrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="70a78-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="70a78-104">O exemplo enrollSimpleUserCert registra um usuário final com uma autoridade de certificação (CA) usando um modelo, o nome da entidade e o comprimento, em bits, da chave.</span><span class="sxs-lookup"><span data-stu-id="70a78-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="70a78-105">Local</span><span class="sxs-lookup"><span data-stu-id="70a78-105">Location</span></span>

<span data-ttu-id="70a78-106">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, uma versão em C++ do exemplo é instalada, por padrão, na pasta *% ProgramFiles%%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="70a78-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="70a78-107">Uma versão do C# é instalada na pasta *% ProgramFiles%%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Enroll \\ \\ EnrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="70a78-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="70a78-108">Discussão</span><span class="sxs-lookup"><span data-stu-id="70a78-108">Discussion</span></span>

<span data-ttu-id="70a78-109">O exemplo de enrollSimpleUserCert:</span><span class="sxs-lookup"><span data-stu-id="70a78-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="70a78-110">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="70a78-110">Processes the command line arguments.</span></span> <span data-ttu-id="70a78-111">A linha de comando deve conter o nome do modelo, o nome da entidade e o comprimento da chave.</span><span class="sxs-lookup"><span data-stu-id="70a78-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="70a78-112">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e o inicializa usando o modelo.</span><span class="sxs-lookup"><span data-stu-id="70a78-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="70a78-113">Recupera o objeto de solicitação de certificado interno do objeto de registro e o consulta para o objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="70a78-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="70a78-114">A solicitação mais interna é sempre uma \# solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="70a78-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="70a78-115">Recupera o objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) da solicitação PKCS \# 10 e define o comprimento da chave especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="70a78-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="70a78-116">Cria um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , usa-o para codificar o nome da entidade X. 500 e adiciona o nome à \# solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="70a78-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="70a78-117">Tenta registrar o usuário final com a AC e monitora o progresso do processo de registro.</span><span class="sxs-lookup"><span data-stu-id="70a78-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="70a78-118">A função checkEnrollStatus é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="70a78-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70a78-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70a78-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70a78-120">\#Solicitação PKCS 10</span><span class="sxs-lookup"><span data-stu-id="70a78-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="70a78-121">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="70a78-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



