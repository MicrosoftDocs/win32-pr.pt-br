---
description: O oferece suporte a assinaturas digitais e criptografia de dados. Ele é considerado um CSP (provedor de serviços de criptografia) de uso geral.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011450"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="8ecc3-104">PROV \_ RSA \_ AES</span><span class="sxs-lookup"><span data-stu-id="8ecc3-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="8ecc3-105">O \_ tipo de provedor de AES RSA Prov \_ oferece suporte a [assinaturas digitais](digital-signatures.md) e criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="8ecc3-106">Ele é considerado um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) de uso geral.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="8ecc3-107">O [*algoritmo de chave pública*](../secgloss/p-gly.md) RSA é usado para todas as operações de [*chave pública*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8ecc3-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="8ecc3-108">Algoritmos com suporte</span><span class="sxs-lookup"><span data-stu-id="8ecc3-108">Algorithms Supported</span></span>

<span data-ttu-id="8ecc3-109">Para obter descrições de cada um desses algoritmos, consulte o Glossário.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="8ecc3-110">Finalidade</span><span class="sxs-lookup"><span data-stu-id="8ecc3-110">Purpose</span></span>      | <span data-ttu-id="8ecc3-111">Algoritmos compatíveis</span><span class="sxs-lookup"><span data-stu-id="8ecc3-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecc3-112">Troca de chaves</span><span class="sxs-lookup"><span data-stu-id="8ecc3-112">Key Exchange</span></span> | [<span data-ttu-id="8ecc3-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="8ecc3-114">Assinatura</span><span class="sxs-lookup"><span data-stu-id="8ecc3-114">Signature</span></span>    | [<span data-ttu-id="8ecc3-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="8ecc3-116">Criptografia</span><span class="sxs-lookup"><span data-stu-id="8ecc3-116">Encryption</span></span>   | [<span data-ttu-id="8ecc3-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="8ecc3-118">*RC4*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="8ecc3-119">[*Criptografia AES*](../secgloss/a-gly.md) (AES)</span><span class="sxs-lookup"><span data-stu-id="8ecc3-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="8ecc3-120">Hash</span><span class="sxs-lookup"><span data-stu-id="8ecc3-120">Hashing</span></span>      | [<span data-ttu-id="8ecc3-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="8ecc3-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="8ecc3-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="8ecc3-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="8ecc3-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="8ecc3-125">SHA-2 (SHA-256, SHA-384 e SHA-512)</span><span class="sxs-lookup"><span data-stu-id="8ecc3-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="8ecc3-126">Documentação relacionada</span><span class="sxs-lookup"><span data-stu-id="8ecc3-126">Related Documentation</span></span>

<span data-ttu-id="8ecc3-127">Esse tipo de provedor é definido pela Microsoft e pela RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="8ecc3-128">Ele é descrito nos seguintes documentos:</span><span class="sxs-lookup"><span data-stu-id="8ecc3-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="8ecc3-129">*Guia do programador do provedor de serviços de criptografia da Microsoft*, Microsoft, 1996.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="8ecc3-130">Laboratórios RSA, padrões de criptografia de chave pública, segurança de dados RSA, novembro de 1993.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="8ecc3-131">Esses recursos podem não estar disponíveis em alguns idiomas e países ou regiões.</span><span class="sxs-lookup"><span data-stu-id="8ecc3-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 
