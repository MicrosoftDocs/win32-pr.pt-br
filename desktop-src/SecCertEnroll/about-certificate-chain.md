---
description: Uma cadeia de certificados é uma coleção hierárquica de certificados que leva do usuário final ou computador de volta para uma raiz de confiança, normalmente a CA (autoridade de certificação) raiz de uma organização.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Cadeia de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756690"
---
# <a name="certificate-chain"></a><span data-ttu-id="943f6-103">Cadeia de certificados</span><span class="sxs-lookup"><span data-stu-id="943f6-103">Certificate Chain</span></span>

<span data-ttu-id="943f6-104">Uma cadeia de certificados é uma coleção hierárquica de certificados que leva do usuário final ou computador de volta para uma raiz de confiança, normalmente a CA (autoridade de certificação) raiz de uma organização.</span><span class="sxs-lookup"><span data-stu-id="943f6-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="943f6-105">Como todas as partes supostamente confiam no certificado raiz, uma parte pode obter confiança em um certificado de entidade final, verificando a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="943f6-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="943f6-106">A verificação normalmente requer o estabelecimento de cada certificado na cadeia:</span><span class="sxs-lookup"><span data-stu-id="943f6-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="943f6-107">É assinado pela chave pública no certificado anterior.</span><span class="sxs-lookup"><span data-stu-id="943f6-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="943f6-108">Não expirou.</span><span class="sxs-lookup"><span data-stu-id="943f6-108">Has not expired.</span></span>
-   <span data-ttu-id="943f6-109">Não foi revogado.</span><span class="sxs-lookup"><span data-stu-id="943f6-109">Has not been revoked.</span></span>
-   <span data-ttu-id="943f6-110">Está de acordo com as políticas especificadas pelos certificados anteriores.</span><span class="sxs-lookup"><span data-stu-id="943f6-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="943f6-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="943f6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="943f6-112">Hierarquia de certificados</span><span class="sxs-lookup"><span data-stu-id="943f6-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="943f6-113">Certificação cruzada</span><span class="sxs-lookup"><span data-stu-id="943f6-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="943f6-114">Modelos de confiança</span><span class="sxs-lookup"><span data-stu-id="943f6-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



