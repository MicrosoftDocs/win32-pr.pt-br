---
description: 'Ao contrário da CryptoAPI (API de criptografia), a CNG (Cryptography API: Next Generation) separa os provedores criptográficos dos KSPs (provedores de armazenamento de chaves).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Provedores de armazenamento de chaves CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370592"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="9ae12-103">Provedores de armazenamento de chaves CNG</span><span class="sxs-lookup"><span data-stu-id="9ae12-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="9ae12-104">Ao contrário da CryptoAPI (API de criptografia), a CNG (Cryptography API: Next Generation) separa os provedores criptográficos dos KSPs (provedores de armazenamento de chaves).</span><span class="sxs-lookup"><span data-stu-id="9ae12-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="9ae12-105">KSPs pode ser usado para criar, excluir, exportar, importar, abrir e armazenar chaves.</span><span class="sxs-lookup"><span data-stu-id="9ae12-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="9ae12-106">Dependendo da implementação, eles também podem ser usados para criptografia assimétrica, contrato secreto e assinatura.</span><span class="sxs-lookup"><span data-stu-id="9ae12-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="9ae12-107">A Microsoft instala o seguinte KSPs a partir do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9ae12-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="9ae12-108">Os fornecedores podem criar e instalar outros provedores.</span><span class="sxs-lookup"><span data-stu-id="9ae12-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="9ae12-109">Provedor de armazenamento de chaves de software da Microsoft</span><span class="sxs-lookup"><span data-stu-id="9ae12-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="9ae12-110">Dá suporte à criação de chave de software e ao armazenamento e aos seguintes algoritmos.</span><span class="sxs-lookup"><span data-stu-id="9ae12-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="9ae12-111">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="9ae12-111">Algorithm</span></span>                                          | <span data-ttu-id="9ae12-112">Finalidade</span><span class="sxs-lookup"><span data-stu-id="9ae12-112">Purpose</span></span>                           | <span data-ttu-id="9ae12-113">Comprimento da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="9ae12-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="9ae12-114">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="9ae12-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="9ae12-115">Acordo de segredo e troca de chaves</span><span class="sxs-lookup"><span data-stu-id="9ae12-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="9ae12-116">512 a 4096 em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="9ae12-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="9ae12-117">Algoritmo de assinatura digital (DSA)</span><span class="sxs-lookup"><span data-stu-id="9ae12-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="9ae12-118">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="9ae12-118">Signatures</span></span>                        | <span data-ttu-id="9ae12-119">512 a 1024 em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="9ae12-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="9ae12-120">Diffie-Hellman de curva elíptica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="9ae12-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="9ae12-121">Acordo de segredo e troca de chaves</span><span class="sxs-lookup"><span data-stu-id="9ae12-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="9ae12-122">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="9ae12-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="9ae12-123">ECDSA (algoritmo de assinatura digital de curva elíptica)</span><span class="sxs-lookup"><span data-stu-id="9ae12-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="9ae12-124">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="9ae12-124">Signatures</span></span>                        | <span data-ttu-id="9ae12-125">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="9ae12-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="9ae12-126">RSA</span><span class="sxs-lookup"><span data-stu-id="9ae12-126">RSA</span></span>                                                | <span data-ttu-id="9ae12-127">Criptografia assimétrica e assinatura</span><span class="sxs-lookup"><span data-stu-id="9ae12-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="9ae12-128">512 a 16384 em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="9ae12-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="9ae12-129">Provedor de armazenamento de chaves de cartão inteligente da Microsoft</span><span class="sxs-lookup"><span data-stu-id="9ae12-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="9ae12-130">Dá suporte à criação e ao armazenamento de chave de cartão inteligente e aos seguintes algoritmos.</span><span class="sxs-lookup"><span data-stu-id="9ae12-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="9ae12-131">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="9ae12-131">Algorithm</span></span>                                          | <span data-ttu-id="9ae12-132">Finalidade</span><span class="sxs-lookup"><span data-stu-id="9ae12-132">Purpose</span></span>                           | <span data-ttu-id="9ae12-133">Comprimento da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="9ae12-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="9ae12-134">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="9ae12-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="9ae12-135">Acordo de segredo e troca de chaves</span><span class="sxs-lookup"><span data-stu-id="9ae12-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="9ae12-136">512 a 4096 em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="9ae12-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="9ae12-137">Diffie-Hellman de curva elíptica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="9ae12-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="9ae12-138">Acordo de segredo e troca de chaves</span><span class="sxs-lookup"><span data-stu-id="9ae12-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="9ae12-139">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="9ae12-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="9ae12-140">ECDSA (algoritmo de assinatura digital de curva elíptica)</span><span class="sxs-lookup"><span data-stu-id="9ae12-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="9ae12-141">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="9ae12-141">Signatures</span></span>                        | <span data-ttu-id="9ae12-142">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="9ae12-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="9ae12-143">RSA</span><span class="sxs-lookup"><span data-stu-id="9ae12-143">RSA</span></span>                                                | <span data-ttu-id="9ae12-144">Criptografia assimétrica e assinatura</span><span class="sxs-lookup"><span data-stu-id="9ae12-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="9ae12-145">512 a 16384 em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="9ae12-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9ae12-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ae12-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae12-147">**Identificadores de algoritmo CNG**</span><span class="sxs-lookup"><span data-stu-id="9ae12-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="9ae12-148">Funções de armazenamento de chaves CNG</span><span class="sxs-lookup"><span data-stu-id="9ae12-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="9ae12-149">Noções básicas sobre provedores criptográficos</span><span class="sxs-lookup"><span data-stu-id="9ae12-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
