---
description: Exemplo de certificado. Crie aplicativos para certificação de API, instale o certificado SSL, o certificado do servidor, crie um certificado sobre a mídia, como a Internet ou uma intranet, que não são inerentemente seguras.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501750"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="c33c4-104">API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="c33c4-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="c33c4-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="c33c4-105">Purpose</span></span>

<span data-ttu-id="c33c4-106">A API de registro de certificado pode ser usada para criar um aplicativo cliente para solicitar um certificado e instalar uma resposta de certificado.</span><span class="sxs-lookup"><span data-stu-id="c33c4-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="c33c4-107">Essa API é implementada no CertEnroll.dll a partir do Windows Vista; Ele substitui Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="c33c4-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c33c4-108">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="c33c4-108">Developer audience</span></span>

<span data-ttu-id="c33c4-109">A API de registro de certificado é usada por desenvolvedores de aplicativos que permitirão que os usuários criem, solicitem e recuperem certificados por meio de mídia, como a Internet ou uma intranet, que não são inerentemente seguras.</span><span class="sxs-lookup"><span data-stu-id="c33c4-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="c33c4-110">Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++, o COM (Component Object Model) e o ambiente de programação baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="c33c4-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="c33c4-111">Embora não seja necessário, é recomendável compreender a criptografia e a infraestrutura de chave pública.</span><span class="sxs-lookup"><span data-stu-id="c33c4-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c33c4-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c33c4-112">Run-time requirements</span></span>

<span data-ttu-id="c33c4-113">A API de registro de certificado tem suporte a partir do Windows Server 2008 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c33c4-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="c33c4-114">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="c33c4-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c33c4-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c33c4-115">In this section</span></span>



| <span data-ttu-id="c33c4-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="c33c4-116">Topic</span></span>                                                                                       | <span data-ttu-id="c33c4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c33c4-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c33c4-118">Sobre a API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="c33c4-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="c33c4-119">Conceitos principais sobre solicitações de certificado são discutidos.</span><span class="sxs-lookup"><span data-stu-id="c33c4-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="c33c4-120">Usando a API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="c33c4-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="c33c4-121">Como usar a API de registro de certificado para estender os recursos de Active Directory serviços de certificados.</span><span class="sxs-lookup"><span data-stu-id="c33c4-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="c33c4-122">Referência da API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="c33c4-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="c33c4-123">Descrições detalhadas de interfaces, enumerações e outros elementos de programação que podem ser usados para registrar um usuário ou computador em uma hierarquia de certificados.</span><span class="sxs-lookup"><span data-stu-id="c33c4-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




