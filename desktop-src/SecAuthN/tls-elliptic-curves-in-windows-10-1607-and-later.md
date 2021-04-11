---
description: Curvas elípticas habilitadas no Windows 10 versão 1607 e posteriores.
title: Curvas elípticas TLS no Windows 10 versão 1607 e posteriores
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170937"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="7030b-103">Curvas elípticas TLS no Windows 10 versão 1607 e posteriores</span><span class="sxs-lookup"><span data-stu-id="7030b-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="7030b-104">Para o Windows 10, versões 1607 e posteriores, as seguintes curvas elípticas estão habilitadas e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:</span><span class="sxs-lookup"><span data-stu-id="7030b-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="7030b-105">Cadeia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="7030b-105">Elliptic curve string</span></span> | <span data-ttu-id="7030b-106">Disponível no modo FIPS</span><span class="sxs-lookup"><span data-stu-id="7030b-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="7030b-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="7030b-107">curve25519</span></span> | <span data-ttu-id="7030b-108">No</span><span class="sxs-lookup"><span data-stu-id="7030b-108">No</span></span> |
| <span data-ttu-id="7030b-109">NistP256</span><span class="sxs-lookup"><span data-stu-id="7030b-109">NistP256</span></span> | <span data-ttu-id="7030b-110">Yes</span><span class="sxs-lookup"><span data-stu-id="7030b-110">Yes</span></span> |
| <span data-ttu-id="7030b-111">NistP384</span><span class="sxs-lookup"><span data-stu-id="7030b-111">NistP384</span></span> | <span data-ttu-id="7030b-112">Yes</span><span class="sxs-lookup"><span data-stu-id="7030b-112">Yes</span></span> |


<span data-ttu-id="7030b-113">As curvas elípticas a seguir têm suporte do provedor Microsoft Schannel, mas não habilitadas por padrão:</span><span class="sxs-lookup"><span data-stu-id="7030b-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="7030b-114">Cadeia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="7030b-114">Elliptic curve string</span></span> | <span data-ttu-id="7030b-115">Disponível no modo FIPS</span><span class="sxs-lookup"><span data-stu-id="7030b-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="7030b-116">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="7030b-116">brainpoolP256r1</span></span> | <span data-ttu-id="7030b-117">No</span><span class="sxs-lookup"><span data-stu-id="7030b-117">No</span></span> |
| <span data-ttu-id="7030b-118">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="7030b-118">brainpoolP384r1</span></span> | <span data-ttu-id="7030b-119">No</span><span class="sxs-lookup"><span data-stu-id="7030b-119">No</span></span> |
| <span data-ttu-id="7030b-120">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="7030b-120">brainpoolP512r1</span></span> | <span data-ttu-id="7030b-121">No</span><span class="sxs-lookup"><span data-stu-id="7030b-121">No</span></span> |
| <span data-ttu-id="7030b-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="7030b-122">nistP192</span></span> | <span data-ttu-id="7030b-123">No</span><span class="sxs-lookup"><span data-stu-id="7030b-123">No</span></span> |
| <span data-ttu-id="7030b-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="7030b-124">nistP224</span></span> | <span data-ttu-id="7030b-125">No</span><span class="sxs-lookup"><span data-stu-id="7030b-125">No</span></span> |
| <span data-ttu-id="7030b-126">nistP521</span><span class="sxs-lookup"><span data-stu-id="7030b-126">nistP521</span></span> | <span data-ttu-id="7030b-127">Yes</span><span class="sxs-lookup"><span data-stu-id="7030b-127">Yes</span></span> |
| <span data-ttu-id="7030b-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="7030b-128">secP160k1</span></span> | <span data-ttu-id="7030b-129">No</span><span class="sxs-lookup"><span data-stu-id="7030b-129">No</span></span> |
| <span data-ttu-id="7030b-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="7030b-130">secP160r1</span></span> | <span data-ttu-id="7030b-131">No</span><span class="sxs-lookup"><span data-stu-id="7030b-131">No</span></span> |
| <span data-ttu-id="7030b-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="7030b-132">secP160r2</span></span> | <span data-ttu-id="7030b-133">No</span><span class="sxs-lookup"><span data-stu-id="7030b-133">No</span></span> |
| <span data-ttu-id="7030b-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="7030b-134">secP192k1</span></span> | <span data-ttu-id="7030b-135">No</span><span class="sxs-lookup"><span data-stu-id="7030b-135">No</span></span> |
| <span data-ttu-id="7030b-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="7030b-136">secP192r1</span></span> | <span data-ttu-id="7030b-137">No</span><span class="sxs-lookup"><span data-stu-id="7030b-137">No</span></span> |
| <span data-ttu-id="7030b-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="7030b-138">secP224k1</span></span> | <span data-ttu-id="7030b-139">No</span><span class="sxs-lookup"><span data-stu-id="7030b-139">No</span></span> |
| <span data-ttu-id="7030b-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="7030b-140">secP224r1</span></span> | <span data-ttu-id="7030b-141">No</span><span class="sxs-lookup"><span data-stu-id="7030b-141">No</span></span> |
| <span data-ttu-id="7030b-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="7030b-142">secP256k1</span></span> | <span data-ttu-id="7030b-143">No</span><span class="sxs-lookup"><span data-stu-id="7030b-143">No</span></span> |
| <span data-ttu-id="7030b-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="7030b-144">secP256r1</span></span> | <span data-ttu-id="7030b-145">No</span><span class="sxs-lookup"><span data-stu-id="7030b-145">No</span></span> |
| <span data-ttu-id="7030b-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="7030b-146">secP384r1</span></span> | <span data-ttu-id="7030b-147">No</span><span class="sxs-lookup"><span data-stu-id="7030b-147">No</span></span> |
| <span data-ttu-id="7030b-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="7030b-148">secP521r1</span></span> | <span data-ttu-id="7030b-149">No</span><span class="sxs-lookup"><span data-stu-id="7030b-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="7030b-150">Habilitando curvas elípticas</span><span class="sxs-lookup"><span data-stu-id="7030b-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="7030b-151">Para adicionar curvas elípticas, implante uma política de grupo ou use os cmdlets TLS:</span><span class="sxs-lookup"><span data-stu-id="7030b-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="7030b-152">Para usar a política de grupo, [defina a ordem de curva ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) em configuração do computador > modelos administrativos > rede > definições de configuração SSL com a lista de prioridades para todas as curvas elípticas que você deseja habilitar.</span><span class="sxs-lookup"><span data-stu-id="7030b-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="7030b-153">Para usar o PowerShell, consulte [cmdlets de TLS](/powershell/module/tls) para obter uma lista completa de sintaxe e descrições de cmdlets TLS.</span><span class="sxs-lookup"><span data-stu-id="7030b-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="7030b-154">Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva.</span><span class="sxs-lookup"><span data-stu-id="7030b-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="7030b-155">O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.</span><span class="sxs-lookup"><span data-stu-id="7030b-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="7030b-156">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7030b-156">See Also</span></span>

[<span data-ttu-id="7030b-157">Configurando a ordem de curva do TLS ECC</span><span class="sxs-lookup"><span data-stu-id="7030b-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="7030b-158">Gerenciando a ordem de ECC TLS</span><span class="sxs-lookup"><span data-stu-id="7030b-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="7030b-159">Gerenciando as curvas do ECC do Windows usando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="7030b-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="7030b-160">Cmdlets TLS</span><span class="sxs-lookup"><span data-stu-id="7030b-160">TLS cmdlets</span></span>](/powershell/module/tls)
