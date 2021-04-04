---
description: O provedor criptográfico aprimorado da Microsoft fornece um aplicativo com segurança mais forte do que o que está disponível atualmente com o provedor Microsoft Base Cryptographic. O maior comprimento de chave oferece aos usuários mais proteção para dados confidenciais.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparação de comprimento de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837386"
---
# <a name="key-length-comparison"></a><span data-ttu-id="4d337-104">Comparação de comprimento de chave</span><span class="sxs-lookup"><span data-stu-id="4d337-104">Key Length Comparison</span></span>

<span data-ttu-id="4d337-105">O provedor criptográfico aprimorado da Microsoft fornece um aplicativo com segurança mais forte do que o que está disponível atualmente com o provedor Microsoft Base Cryptographic.</span><span class="sxs-lookup"><span data-stu-id="4d337-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="4d337-106">O maior comprimento de chave oferece aos usuários mais proteção para dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="4d337-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="4d337-107">A tabela a seguir lista os [*comprimentos de chave*](../secgloss/k-gly.md) padrão com suporte pelo provedor de base e o provedor avançado para algoritmos padrão.</span><span class="sxs-lookup"><span data-stu-id="4d337-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="4d337-108">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="4d337-108">Algorithm</span></span>                                                                                | <span data-ttu-id="4d337-109">Provedor base</span><span class="sxs-lookup"><span data-stu-id="4d337-109">Base Provider</span></span> | <span data-ttu-id="4d337-110">Provedores fortes e avançados</span><span class="sxs-lookup"><span data-stu-id="4d337-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="4d337-111">Troca de chaves RSA</span><span class="sxs-lookup"><span data-stu-id="4d337-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="4d337-112">512 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-112">512-bit</span></span>       | <span data-ttu-id="4d337-113">1.024 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-113">1,024-bit</span></span>                     |
| <span data-ttu-id="4d337-114">Assinatura RSA</span><span class="sxs-lookup"><span data-stu-id="4d337-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="4d337-115">512 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-115">512-bit</span></span>       | <span data-ttu-id="4d337-116">1.024 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-116">1,024-bit</span></span>                     |
| <span data-ttu-id="4d337-117">RC2</span><span class="sxs-lookup"><span data-stu-id="4d337-117">RC2</span></span>                                                                                      | <span data-ttu-id="4d337-118">40 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-118">40-bit</span></span>        | <span data-ttu-id="4d337-119">128 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-119">128-bit</span></span>                       |
| <span data-ttu-id="4d337-120">RC4</span><span class="sxs-lookup"><span data-stu-id="4d337-120">RC4</span></span>                                                                                      | <span data-ttu-id="4d337-121">40 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-121">40-bit</span></span>        | <span data-ttu-id="4d337-122">128 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-122">128-bit</span></span>                       |
| <span data-ttu-id="4d337-123">DES</span><span class="sxs-lookup"><span data-stu-id="4d337-123">DES</span></span>                                                                                      | <span data-ttu-id="4d337-124">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4d337-124">Not supported</span></span> | <span data-ttu-id="4d337-125">56 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-125">56-bit</span></span>                        |
| <span data-ttu-id="4d337-126">[*Des triplo*](../secgloss/t-gly.md) (2 teclas)</span><span class="sxs-lookup"><span data-stu-id="4d337-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="4d337-127">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4d337-127">Not supported</span></span> | <span data-ttu-id="4d337-128">112 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-128">112-bit</span></span>                       |
| <span data-ttu-id="4d337-129">DES triplo (3 teclas)</span><span class="sxs-lookup"><span data-stu-id="4d337-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="4d337-130">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4d337-130">Not supported</span></span> | <span data-ttu-id="4d337-131">168 bits</span><span class="sxs-lookup"><span data-stu-id="4d337-131">168-bit</span></span>                       |



 

<span data-ttu-id="4d337-132">Há suporte para algoritmos [*des*](../secgloss/d-gly.md) e [*Triple DES*](../secgloss/t-gly.md) no provedor avançado.</span><span class="sxs-lookup"><span data-stu-id="4d337-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="4d337-133">O provedor avançado é compatível com versões anteriores com o provedor de base distribuído com a versão anterior do CryptoAPI com a seguinte exceção.</span><span class="sxs-lookup"><span data-stu-id="4d337-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="4d337-134">O provedor base e o provedor avançado só podem gerar chaves de sessão de comprimento de chave padrão.</span><span class="sxs-lookup"><span data-stu-id="4d337-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="4d337-135">O comprimento padrão das chaves de sessão para o provedor de base é de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="4d337-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="4d337-136">O comprimento de chave padrão para o provedor avançado é de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4d337-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="4d337-137">O provedor avançado não pode criar chaves com comprimentos de chave compatíveis com o provedor base.</span><span class="sxs-lookup"><span data-stu-id="4d337-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="4d337-138">No entanto, o provedor avançado pode importar comprimentos de chave de qualquer tamanho, até 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4d337-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
