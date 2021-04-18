---
description: Curvas elípticas habilitadas nas versões 1507 e 1511 do Windows 10.
title: Curvas elípticas TLS no Windows 10 versão 1507 e 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814609"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a><span data-ttu-id="cc717-103">Curvas elípticas TLS no Windows 10 versão 1507 e 1511</span><span class="sxs-lookup"><span data-stu-id="cc717-103">TLS Elliptic Curves in Windows 10 version 1507 and 1511</span></span>

<span data-ttu-id="cc717-104">Para o Windows 10, versões 1507 e 1511, as seguintes curvas elípticas estão habilitadas e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:</span><span class="sxs-lookup"><span data-stu-id="cc717-104">For Windows 10, versions 1507 and 1511, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="cc717-105">Cadeia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="cc717-105">Elliptic curve string</span></span> | <span data-ttu-id="cc717-106">Disponível no modo FIPS</span><span class="sxs-lookup"><span data-stu-id="cc717-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="cc717-107">NistP256</span><span class="sxs-lookup"><span data-stu-id="cc717-107">NistP256</span></span> | <span data-ttu-id="cc717-108">Yes</span><span class="sxs-lookup"><span data-stu-id="cc717-108">Yes</span></span> |
| <span data-ttu-id="cc717-109">NistP384</span><span class="sxs-lookup"><span data-stu-id="cc717-109">NistP384</span></span> | <span data-ttu-id="cc717-110">Yes</span><span class="sxs-lookup"><span data-stu-id="cc717-110">Yes</span></span> |


<span data-ttu-id="cc717-111">As curvas elípticas a seguir têm suporte do provedor Microsoft Schannel, mas não habilitadas por padrão:</span><span class="sxs-lookup"><span data-stu-id="cc717-111">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="cc717-112">Cadeia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="cc717-112">Elliptic curve string</span></span> | <span data-ttu-id="cc717-113">Disponível no modo FIPS</span><span class="sxs-lookup"><span data-stu-id="cc717-113">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="cc717-114">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="cc717-114">brainpoolP256r1</span></span> | <span data-ttu-id="cc717-115">No</span><span class="sxs-lookup"><span data-stu-id="cc717-115">No</span></span> |
| <span data-ttu-id="cc717-116">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="cc717-116">brainpoolP384r1</span></span> | <span data-ttu-id="cc717-117">No</span><span class="sxs-lookup"><span data-stu-id="cc717-117">No</span></span> |
| <span data-ttu-id="cc717-118">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="cc717-118">brainpoolP512r1</span></span> | <span data-ttu-id="cc717-119">No</span><span class="sxs-lookup"><span data-stu-id="cc717-119">No</span></span> |
| <span data-ttu-id="cc717-120">nistP192</span><span class="sxs-lookup"><span data-stu-id="cc717-120">nistP192</span></span> | <span data-ttu-id="cc717-121">No</span><span class="sxs-lookup"><span data-stu-id="cc717-121">No</span></span> |
| <span data-ttu-id="cc717-122">nistP224</span><span class="sxs-lookup"><span data-stu-id="cc717-122">nistP224</span></span> | <span data-ttu-id="cc717-123">No</span><span class="sxs-lookup"><span data-stu-id="cc717-123">No</span></span> |
| <span data-ttu-id="cc717-124">nistP521</span><span class="sxs-lookup"><span data-stu-id="cc717-124">nistP521</span></span> | <span data-ttu-id="cc717-125">Yes</span><span class="sxs-lookup"><span data-stu-id="cc717-125">Yes</span></span> |
| <span data-ttu-id="cc717-126">secP160k1</span><span class="sxs-lookup"><span data-stu-id="cc717-126">secP160k1</span></span> | <span data-ttu-id="cc717-127">No</span><span class="sxs-lookup"><span data-stu-id="cc717-127">No</span></span> |
| <span data-ttu-id="cc717-128">secP160r1</span><span class="sxs-lookup"><span data-stu-id="cc717-128">secP160r1</span></span> | <span data-ttu-id="cc717-129">No</span><span class="sxs-lookup"><span data-stu-id="cc717-129">No</span></span> |
| <span data-ttu-id="cc717-130">secP160r2</span><span class="sxs-lookup"><span data-stu-id="cc717-130">secP160r2</span></span> | <span data-ttu-id="cc717-131">No</span><span class="sxs-lookup"><span data-stu-id="cc717-131">No</span></span> |
| <span data-ttu-id="cc717-132">secP192k1</span><span class="sxs-lookup"><span data-stu-id="cc717-132">secP192k1</span></span> | <span data-ttu-id="cc717-133">No</span><span class="sxs-lookup"><span data-stu-id="cc717-133">No</span></span> |
| <span data-ttu-id="cc717-134">secP192r1</span><span class="sxs-lookup"><span data-stu-id="cc717-134">secP192r1</span></span> | <span data-ttu-id="cc717-135">No</span><span class="sxs-lookup"><span data-stu-id="cc717-135">No</span></span> |
| <span data-ttu-id="cc717-136">secP224k1</span><span class="sxs-lookup"><span data-stu-id="cc717-136">secP224k1</span></span> | <span data-ttu-id="cc717-137">No</span><span class="sxs-lookup"><span data-stu-id="cc717-137">No</span></span> |
| <span data-ttu-id="cc717-138">secP224r1</span><span class="sxs-lookup"><span data-stu-id="cc717-138">secP224r1</span></span> | <span data-ttu-id="cc717-139">No</span><span class="sxs-lookup"><span data-stu-id="cc717-139">No</span></span> |
| <span data-ttu-id="cc717-140">secP256k1</span><span class="sxs-lookup"><span data-stu-id="cc717-140">secP256k1</span></span> | <span data-ttu-id="cc717-141">No</span><span class="sxs-lookup"><span data-stu-id="cc717-141">No</span></span> |
| <span data-ttu-id="cc717-142">secP256r1</span><span class="sxs-lookup"><span data-stu-id="cc717-142">secP256r1</span></span> | <span data-ttu-id="cc717-143">No</span><span class="sxs-lookup"><span data-stu-id="cc717-143">No</span></span> |
| <span data-ttu-id="cc717-144">secP384r1</span><span class="sxs-lookup"><span data-stu-id="cc717-144">secP384r1</span></span> | <span data-ttu-id="cc717-145">No</span><span class="sxs-lookup"><span data-stu-id="cc717-145">No</span></span> |
| <span data-ttu-id="cc717-146">secP521r1</span><span class="sxs-lookup"><span data-stu-id="cc717-146">secP521r1</span></span> | <span data-ttu-id="cc717-147">No</span><span class="sxs-lookup"><span data-stu-id="cc717-147">No</span></span> |

## <a name="enabling-elliptic-curves"></a><span data-ttu-id="cc717-148">Habilitando curvas elípticas</span><span class="sxs-lookup"><span data-stu-id="cc717-148">Enabling Elliptic Curves</span></span>

<span data-ttu-id="cc717-149">Para adicionar curvas elípticas, implante uma política de grupo ou use os cmdlets TLS:</span><span class="sxs-lookup"><span data-stu-id="cc717-149">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="cc717-150">Para usar a política de grupo, [defina a ordem de curva ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) em configuração do computador > modelos administrativos > rede > definições de configuração SSL com a lista de prioridades para todas as curvas elípticas que você deseja habilitar.</span><span class="sxs-lookup"><span data-stu-id="cc717-150">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="cc717-151">Para usar o PowerShell, consulte [cmdlets de TLS](/powershell/module/tls) para obter uma lista completa de sintaxe e descrições de cmdlets TLS.</span><span class="sxs-lookup"><span data-stu-id="cc717-151">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="cc717-152">Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva.</span><span class="sxs-lookup"><span data-stu-id="cc717-152">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="cc717-153">O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.</span><span class="sxs-lookup"><span data-stu-id="cc717-153">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="cc717-154">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cc717-154">See Also</span></span>

[<span data-ttu-id="cc717-155">Configurando a ordem de curva do TLS ECC</span><span class="sxs-lookup"><span data-stu-id="cc717-155">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="cc717-156">Gerenciando a ordem de ECC TLS</span><span class="sxs-lookup"><span data-stu-id="cc717-156">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="cc717-157">Gerenciando as curvas do ECC do Windows usando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="cc717-157">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="cc717-158">Cmdlets TLS</span><span class="sxs-lookup"><span data-stu-id="cc717-158">TLS cmdlets</span></span>](/powershell/module/tls)
