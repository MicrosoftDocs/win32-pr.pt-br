---
description: A biblioteca de Xenroll.dll foi removida do sistema operacional e substituída por CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mapeando Xenroll.dll para CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662675"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="31384-103">Mapeando Xenroll.dll para CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="31384-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="31384-104">Antes do Windows Vista, o controle de registro de certificado foi implementado em Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="31384-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="31384-105">A biblioteca de Xenroll.dll foi removida do sistema operacional e substituída por CertEnroll.dll.</span><span class="sxs-lookup"><span data-stu-id="31384-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="31384-106">O XEnroll tentou implementar dois conjuntos paralelos de interfaces.</span><span class="sxs-lookup"><span data-stu-id="31384-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="31384-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)e [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) estavam em conformidade com a automação e são compatíveis com linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="31384-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="31384-108">As interfaces correspondentes,[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)e [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4), não podiam ser inseridas no script, mas eram mais convenientes para programadores de C++.</span><span class="sxs-lookup"><span data-stu-id="31384-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="31384-109">À medida que evoluíram, os dois conjuntos de interfaces não permaneceram sincronizados.</span><span class="sxs-lookup"><span data-stu-id="31384-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="31384-110">Em particular, o conjunto de interfaces duplas representadas mais recentemente por **ICEnroll4** define apenas um subconjunto da funcionalidade definida por **IEnroll4**.</span><span class="sxs-lookup"><span data-stu-id="31384-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="31384-111">CertEnroll.dll implementa um conjunto maior e mais estruturado de interfaces COM em conformidade com a automação.</span><span class="sxs-lookup"><span data-stu-id="31384-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="31384-112">Os tópicos a seguir discutem como o Xenroll.dll é mapeado para CertEnroll.dll para diferentes tipos de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="31384-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="31384-113">Funções de solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="31384-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="31384-114">Funções de resposta de certificado</span><span class="sxs-lookup"><span data-stu-id="31384-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="31384-115">Funções de atributo</span><span class="sxs-lookup"><span data-stu-id="31384-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="31384-116">Funções de extensão</span><span class="sxs-lookup"><span data-stu-id="31384-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="31384-117">Funções de propriedade externa</span><span class="sxs-lookup"><span data-stu-id="31384-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="31384-118">Funções de chave pública e privada</span><span class="sxs-lookup"><span data-stu-id="31384-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="31384-119">Funções do provedor de serviços de criptografia</span><span class="sxs-lookup"><span data-stu-id="31384-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="31384-120">Funções de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="31384-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="31384-121">Funções de troca de informações pessoais</span><span class="sxs-lookup"><span data-stu-id="31384-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="31384-122">Funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="31384-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="31384-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31384-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31384-124">Usando a API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="31384-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
