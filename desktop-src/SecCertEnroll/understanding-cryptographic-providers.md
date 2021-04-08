---
description: Os provedores implementam algoritmos criptográficos, geram chaves, fornecem armazenamento de chaves e autenticam usuários. Os provedores podem ser implementados em hardware, software ou ambos.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Noções básicas sobre provedores criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922291"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="f111f-104">Noções básicas sobre provedores criptográficos</span><span class="sxs-lookup"><span data-stu-id="f111f-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="f111f-105">O conceito do provedor criptográfico que foi introduzido na Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) e que evoluiu um pouco na [*Cryptography API:*](/windows/desktop/SecGloss/c-gly) a CNG (próxima geração) é fundamental para a implementação segura da funcionalidade criptográfica nos sistemas operacionais da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f111f-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="f111f-106">Esses dois SDKs foram usados para criar vários aplicativos e são chamados internamente por outros SDKs.</span><span class="sxs-lookup"><span data-stu-id="f111f-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="f111f-107">Por exemplo, Active Directory serviços de certificados e a API de registro de certificado dependem de CryptoAPI e CNG.</span><span class="sxs-lookup"><span data-stu-id="f111f-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="f111f-108">Em geral, os provedores implementam algoritmos criptográficos, geram chaves, fornecem armazenamento de chaves e autenticam usuários.</span><span class="sxs-lookup"><span data-stu-id="f111f-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="f111f-109">Os provedores podem ser implementados em hardware, software ou ambos.</span><span class="sxs-lookup"><span data-stu-id="f111f-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="f111f-110">Os aplicativos criados com o uso de CryptoAPI ou CNG não podem alterar as chaves criadas pelos provedores e não podem alterar a implementação do algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="f111f-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="f111f-111">Os vários provedores criados pela Microsoft são distribuídos com os sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="f111f-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="f111f-112">Outros provedores foram criados e distribuídos por terceiros.</span><span class="sxs-lookup"><span data-stu-id="f111f-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="f111f-113">Os tópicos a seguir destacam as diferenças entre os provedores associados ao CryptoAPI e os associados à CNG.</span><span class="sxs-lookup"><span data-stu-id="f111f-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="f111f-114">Normalmente, esta documentação se refere a provedores sem referência ao SDK com o qual eles estão associados, observando a associação somente quando ela é relevante.</span><span class="sxs-lookup"><span data-stu-id="f111f-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="f111f-115">Provedores de serviço de criptografia CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="f111f-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="f111f-116">Provedores de algoritmos criptográficos CNG</span><span class="sxs-lookup"><span data-stu-id="f111f-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="f111f-117">Provedores de armazenamento de chaves CNG</span><span class="sxs-lookup"><span data-stu-id="f111f-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="f111f-118">Enumerando provedores instalados</span><span class="sxs-lookup"><span data-stu-id="f111f-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="f111f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f111f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f111f-120">Usando a API de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="f111f-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
