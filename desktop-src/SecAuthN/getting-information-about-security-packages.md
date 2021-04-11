---
description: Quando um cliente é iniciado, ele seleciona um pacote de segurança para suas transações com um servidor e, em seguida, entra em contato com esse servidor. Um servidor seleciona um ou mais pacotes de segurança e aguarda uma conexão de cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obtendo informações sobre pacotes de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090758"
---
# <a name="getting-information-about-security-packages"></a><span data-ttu-id="9a3a2-104">Obtendo informações sobre pacotes de segurança</span><span class="sxs-lookup"><span data-stu-id="9a3a2-104">Getting Information About Security Packages</span></span>

<span data-ttu-id="9a3a2-105">Quando um cliente é iniciado, ele seleciona um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) para suas transações com um servidor e, em seguida, entra em contato com esse servidor.</span><span class="sxs-lookup"><span data-stu-id="9a3a2-105">When a client begins, it selects a [*security package*](/windows/desktop/SecGloss/s-gly) for its transactions with a server and then contacts that server.</span></span> <span data-ttu-id="9a3a2-106">Um servidor seleciona um ou mais pacotes de segurança e aguarda uma conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="9a3a2-106">A server selects one or more security packages and waits for a client connection.</span></span>

<span data-ttu-id="9a3a2-107">Para obter informações específicas sobre os pacotes de segurança SSPI disponíveis com um SSP específico, a função [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) pode ser chamada para recuperar uma estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="9a3a2-107">For specific information about the SSPI security packages available with a particular SSP, the [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) function can be called to retrieve a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span>

<span data-ttu-id="9a3a2-108">Para recuperar a estrutura de saída, o chamador passa para a função o endereço de um ponteiro para o tipo da estrutura de retorno.</span><span class="sxs-lookup"><span data-stu-id="9a3a2-108">To retrieve the output structure, the caller passes to the function the address of a pointer to the type of the return structure.</span></span> <span data-ttu-id="9a3a2-109">A função aloca memória e retorna os dados para o chamador atribuindo o endereço do buffer de dados de retorno ao argumento.</span><span class="sxs-lookup"><span data-stu-id="9a3a2-109">The function allocates memory and returns the data to the caller by assigning the address of the return data buffer to the argument.</span></span> <span data-ttu-id="9a3a2-110">A Convenção SSPI é que a função aloca memória para a estrutura e o aplicativo de chamada libera essa memória usando [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span><span class="sxs-lookup"><span data-stu-id="9a3a2-110">The SSPI convention is that the function allocates memory for the structure, and the calling application frees that memory using [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span></span>

<span data-ttu-id="9a3a2-111">Chamar a função [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) recupera os atributos de um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="9a3a2-111">Calling the [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) function retrieves the attributes of a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="9a3a2-112">Tanto o servidor quanto o cliente podem chamar a função **QuerySecurityPackageInfo** para obter o comprimento máximo do token de segurança do membro **CbMaxToken** da estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="9a3a2-112">Both server and client can call the **QuerySecurityPackageInfo** function to get the maximum length of the security token from the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="9a3a2-113">Para obter um exemplo, consulte a chamada para a função **QuerySecurityPackageInfo** mostrada em [usando SSPI com um servidor do Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="9a3a2-113">For an example, see the call to the **QuerySecurityPackageInfo** function shown in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span>

<span data-ttu-id="9a3a2-114">Para obter mais informações sobre as funções de pacote, consulte [Gerenciamento de pacotes](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9a3a2-114">For more information on package functions, see [Package Management](authentication-functions.md).</span></span>

 

 
