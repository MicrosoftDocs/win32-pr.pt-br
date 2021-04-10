---
description: Lista e explica as etapas necessárias para inicializar um pacote de segurança.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inicializando o pacote de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091387"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="fda96-103">Inicializando o pacote de segurança</span><span class="sxs-lookup"><span data-stu-id="fda96-103">Initializing the Security Package</span></span>

<span data-ttu-id="fda96-104">Essas etapas são necessárias antes de usar SSPI:</span><span class="sxs-lookup"><span data-stu-id="fda96-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="fda96-105">A função de inicialização deve ser chamada para obter o endereço da tabela de funções de segurança.</span><span class="sxs-lookup"><span data-stu-id="fda96-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="fda96-106">O cliente e o servidor chamam [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) para um ponteiro para uma tabela de expedição [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) .</span><span class="sxs-lookup"><span data-stu-id="fda96-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="fda96-107">Esta tabela contém ponteiros para funções de retorno de chamada declaradas em SSPI. h.</span><span class="sxs-lookup"><span data-stu-id="fda96-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="fda96-108">Esses ponteiros fornecem acesso às implementações da DLL das várias funções SSPI.</span><span class="sxs-lookup"><span data-stu-id="fda96-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="fda96-109">As informações devem ser obtidas sobre os pacotes de segurança com suporte.</span><span class="sxs-lookup"><span data-stu-id="fda96-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="fda96-110">Embora a maioria dos aplicativos use pacotes de segurança que dão suporte a recursos padrão ou comuns, os pacotes de segurança podem ter recursos exclusivos de interesse para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fda96-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="fda96-111">Um aplicativo que precisa de recursos especiais pode usar um pacote que oferece esses recursos.</span><span class="sxs-lookup"><span data-stu-id="fda96-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="fda96-112">Para obter mais informações, consulte [obtendo informações sobre pacotes de segurança](getting-information-about-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="fda96-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="fda96-113">Neste ponto, o aplicativo inicializou com êxito um SSP e escolheu um pacote de segurança com recursos suficientes.</span><span class="sxs-lookup"><span data-stu-id="fda96-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="fda96-114">O pacote [*Negotiate*](../secgloss/n-gly.md) pode ser usado em que contrato entre o cliente e o servidor sobre qual [*pacote de segurança*](../secgloss/s-gly.md) usar é feito nos bastidores.</span><span class="sxs-lookup"><span data-stu-id="fda96-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="fda96-115">Se o pacote Negotiate não for usado, o cliente e o servidor deverão concordar com o pacote de segurança específico a ser usado antes de executar as etapas de configuração acima.</span><span class="sxs-lookup"><span data-stu-id="fda96-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
