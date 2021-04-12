---
description: Descreve os códigos de erro 12000-1599 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Códigos de erro do sistema (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457025"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="22c84-103">Códigos de erro do sistema (12000-15999)</span><span class="sxs-lookup"><span data-stu-id="22c84-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="22c84-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="22c84-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="22c84-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="22c84-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="22c84-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 12000 a 15999).</span><span class="sxs-lookup"><span data-stu-id="22c84-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="22c84-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="22c84-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="22c84-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="22c84-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="22c84-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**Erro \_ do \_Internet \** _</span><span class="sxs-lookup"><span data-stu-id="22c84-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-110">12000-12175 (0x2EE0)</span><span class="sxs-lookup"><span data-stu-id="22c84-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-111">Consulte [códigos de erro da Internet](../wininet/wininet-errors.md) e Wininet. h.</span><span class="sxs-lookup"><span data-stu-id="22c84-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *erro \_ a \_ política IPSec qm \_ \_ existe*\*</span><span class="sxs-lookup"><span data-stu-id="22c84-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-113">13000 (0x32C8)</span><span class="sxs-lookup"><span data-stu-id="22c84-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-114">A política de modo rápido especificada já existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERRO \_ de \_ política IPSec qm \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-116">13001 (0x32C9)</span><span class="sxs-lookup"><span data-stu-id="22c84-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-117">A política de modo rápido especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERRO \_ \_ \_ de política IPSec qm \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="22c84-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-119">13002 (0x32CA)</span><span class="sxs-lookup"><span data-stu-id="22c84-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-120">A política de modo rápido especificada está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="22c84-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERRO \_ a \_ política IPSec mm \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="22c84-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-122">13003 (0x32CB)</span><span class="sxs-lookup"><span data-stu-id="22c84-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-123">A política de modo principal especificada já existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERRO \_ de \_ política IPSec mm \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-125">13004 (0x32CC)</span><span class="sxs-lookup"><span data-stu-id="22c84-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-126">A política de modo principal especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERRO \_ \_ \_ de política IPSec mm \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="22c84-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-128">13005 (0x32CD)</span><span class="sxs-lookup"><span data-stu-id="22c84-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-129">A política de modo principal especificada está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="22c84-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERRO \_ o \_ filtro IPSec mm \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="22c84-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-131">13006 (0x32CE)</span><span class="sxs-lookup"><span data-stu-id="22c84-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-132">O filtro de modo principal especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERRO \_ de \_ filtro IPSec mm \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-134">13007 (0x32CF)</span><span class="sxs-lookup"><span data-stu-id="22c84-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-135">O filtro de modo principal especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERRO \_ o \_ filtro de transporte IPSec \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="22c84-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-137">13008 (0x32D0)</span><span class="sxs-lookup"><span data-stu-id="22c84-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-138">O filtro de modo de transporte especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERRO \_ de \_ filtro de transporte IPSec \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-140">13009 (0x32D1)</span><span class="sxs-lookup"><span data-stu-id="22c84-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-141">O filtro de modo de transporte especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERRO \_ a \_ autenticação IPsec mm \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="22c84-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-143">13010 (0x32D2)</span><span class="sxs-lookup"><span data-stu-id="22c84-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-144">A lista de autenticação de modo principal especificada existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERRO \_ de \_ autenticação IPsec mm \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-146">13011 (0x32D3)</span><span class="sxs-lookup"><span data-stu-id="22c84-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-147">A lista de autenticação de modo principal especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERRO \_ \_ \_ de autenticação IPsec mm \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="22c84-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-149">13012 (0x32D4)</span><span class="sxs-lookup"><span data-stu-id="22c84-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-150">A lista de autenticação de modo principal especificada está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="22c84-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERRO \_ de \_ política de IPSec padrão \_ mm \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-152">13013 (0x32D5)</span><span class="sxs-lookup"><span data-stu-id="22c84-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-153">A política de modo principal padrão especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERRO \_ IPSec \_ padrão \_ mm de \_ autenticação \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-155">13014 (0x32D6)</span><span class="sxs-lookup"><span data-stu-id="22c84-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-156">A lista de autenticação de modo principal padrão especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERRO \_ de \_ política IPSec de \_ QM padrão \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-158">13015 (0x32D7)</span><span class="sxs-lookup"><span data-stu-id="22c84-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-159">A política de modo rápido padrão especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERRO \_ o \_ filtro de túnel IPSec \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="22c84-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-161">13016 (0x32D8)</span><span class="sxs-lookup"><span data-stu-id="22c84-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-162">O filtro de modo de túnel especificado existe.</span><span class="sxs-lookup"><span data-stu-id="22c84-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERRO \_ de \_ filtro de túnel IPSec \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-164">13017 (0x32D9)</span><span class="sxs-lookup"><span data-stu-id="22c84-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-165">O filtro de modo de túnel especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente do filtro IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-167">13018 (0x32DA)</span><span class="sxs-lookup"><span data-stu-id="22c84-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-168">O filtro de modo principal está com a exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="22c84-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente do filtro de transporte IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-170">13019 (0x32DB)</span><span class="sxs-lookup"><span data-stu-id="22c84-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-171">O filtro de transporte está com a exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="22c84-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente do filtro de túnel IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-173">13020 (0x32DC)</span><span class="sxs-lookup"><span data-stu-id="22c84-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-174">O filtro de túnel está com a exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="22c84-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente da política IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-176">13021 (0x32DD)</span><span class="sxs-lookup"><span data-stu-id="22c84-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-177">A política de modo principal tem exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="22c84-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERRO de \_ exclusão de autenticação do IPSec \_ mm \_ \_ pendente \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-179">13022 (0x32DE)</span><span class="sxs-lookup"><span data-stu-id="22c84-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-180">O grupo de autenticação de modo principal tem exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="22c84-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente da política IPSec qm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-182">13023 (0x32DF)</span><span class="sxs-lookup"><span data-stu-id="22c84-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-183">A política de modo rápido tem exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="22c84-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**AVISO \_ de \_ política IPSec mm \_ \_ removida**</span><span class="sxs-lookup"><span data-stu-id="22c84-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-185">13024 (0x32E0)</span><span class="sxs-lookup"><span data-stu-id="22c84-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-186">A política de modo principal foi adicionada com êxito, mas não há suporte para algumas das ofertas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="22c84-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**\_política de IPSec qm de aviso \_ \_ \_ removida**</span><span class="sxs-lookup"><span data-stu-id="22c84-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-188">13025 (0x32E1)</span><span class="sxs-lookup"><span data-stu-id="22c84-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-189">A política de modo rápido foi adicionada com êxito, mas não há suporte para algumas das ofertas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="22c84-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERRO \_ de \_ \_ início de status de neg IPSec IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-191">13800 (0x35E8)</span><span class="sxs-lookup"><span data-stu-id="22c84-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-192">ERRO \_ de \_ \_ início de status de neg IPSec IKE \_ \_</span><span class="sxs-lookup"><span data-stu-id="22c84-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERRO \_ de \_ autenticação IKE IPsec com \_ \_ falha**</span><span class="sxs-lookup"><span data-stu-id="22c84-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-194">13801 (0x35E9)</span><span class="sxs-lookup"><span data-stu-id="22c84-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-195">As credenciais de autenticação IKE são inaceitáveis.</span><span class="sxs-lookup"><span data-stu-id="22c84-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERRO \_ de \_ Atrib IPSec IKE com \_ \_ falha**</span><span class="sxs-lookup"><span data-stu-id="22c84-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-197">13802 (0x35EA)</span><span class="sxs-lookup"><span data-stu-id="22c84-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-198">Os atributos de segurança IKE são inaceitáveis.</span><span class="sxs-lookup"><span data-stu-id="22c84-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERRO \_ de \_ negociação IKE IPSec \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="22c84-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-200">13803 (0x35EB)</span><span class="sxs-lookup"><span data-stu-id="22c84-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-201">Negociação IKE em andamento.</span><span class="sxs-lookup"><span data-stu-id="22c84-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**erro \_ de \_ \_ processamento geral de Ike de \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-203">13804 (0x35EC)</span><span class="sxs-lookup"><span data-stu-id="22c84-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-204">Erro geral de processamento.</span><span class="sxs-lookup"><span data-stu-id="22c84-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERRO \_ \_ IKE IPSec \_ atingiu o tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="22c84-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-206">13805 (0x35ED)</span><span class="sxs-lookup"><span data-stu-id="22c84-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-207">A negociação atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="22c84-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ certificado**</span><span class="sxs-lookup"><span data-stu-id="22c84-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-209">13806 (0x35EE)</span><span class="sxs-lookup"><span data-stu-id="22c84-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-210">Falha de IKE ao localizar certificado de máquina válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="22c84-211">Entre em contato com o administrador de segurança de rede para instalar um certificado válido no repositório de certificados apropriado.</span><span class="sxs-lookup"><span data-stu-id="22c84-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERRO \_ \_ Ike \_ SA IPsec \_ excluído**</span><span class="sxs-lookup"><span data-stu-id="22c84-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-213">13807 (0x35EF)</span><span class="sxs-lookup"><span data-stu-id="22c84-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-214">SA IKE excluído pelo par antes da conclusão do estabelecimento.</span><span class="sxs-lookup"><span data-stu-id="22c84-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERRO \_ de \_ SA IKE IPSec \_ \_ colher**</span><span class="sxs-lookup"><span data-stu-id="22c84-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-216">13808 (0x35F0)</span><span class="sxs-lookup"><span data-stu-id="22c84-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-217">SA de IKE excluído antes do estabelecimento ser concluído.</span><span class="sxs-lookup"><span data-stu-id="22c84-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERRO \_ IPSec \_ Ike \_ mm \_ adquirir \_ drop**</span><span class="sxs-lookup"><span data-stu-id="22c84-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-219">13809 (0x35F1)</span><span class="sxs-lookup"><span data-stu-id="22c84-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-220">Solicitação de negociação colocada em fila muito longa.</span><span class="sxs-lookup"><span data-stu-id="22c84-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERRO \_ IPSec \_ Ike \_ qm de \_ aquisição \_ drop**</span><span class="sxs-lookup"><span data-stu-id="22c84-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-222">13810 (0x35F2)</span><span class="sxs-lookup"><span data-stu-id="22c84-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-223">Solicitação de negociação colocada em fila muito longa.</span><span class="sxs-lookup"><span data-stu-id="22c84-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERRO \_ ao \_ \_ \_ remover mm da fila Ike de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-225">13811 (0x35F3)</span><span class="sxs-lookup"><span data-stu-id="22c84-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-226">Solicitação de negociação colocada em fila muito longa.</span><span class="sxs-lookup"><span data-stu-id="22c84-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERRO \_ de \_ fila Ike de IPSec não é possível \_ \_ Remover \_ \_ mm**</span><span class="sxs-lookup"><span data-stu-id="22c84-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-228">13812 (0x35F4)</span><span class="sxs-lookup"><span data-stu-id="22c84-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-229">Solicitação de negociação colocada em fila muito longa.</span><span class="sxs-lookup"><span data-stu-id="22c84-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERRO \_ de \_ \_ descartar IPSec IKE \_ sem \_ resposta**</span><span class="sxs-lookup"><span data-stu-id="22c84-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-231">13813 (0x35F5)</span><span class="sxs-lookup"><span data-stu-id="22c84-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-232">Sem resposta do par.</span><span class="sxs-lookup"><span data-stu-id="22c84-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERRO \_ ao \_ \_ \_ remover atraso de IPSec IKE mm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-234">13814 (0x35F6)</span><span class="sxs-lookup"><span data-stu-id="22c84-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-235">A negociação demorou muito tempo.</span><span class="sxs-lookup"><span data-stu-id="22c84-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERRO \_ ao \_ \_ \_ remover atraso de IPSec IKE qm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-237">13815 (0x35F7)</span><span class="sxs-lookup"><span data-stu-id="22c84-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-238">A negociação demorou muito tempo.</span><span class="sxs-lookup"><span data-stu-id="22c84-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**erro de erro de \_ \_ IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-240">13816 (0x35F8)</span><span class="sxs-lookup"><span data-stu-id="22c84-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-241">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="22c84-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERRO \_ \_ CRL Ike \_ IPSec \_ com falha**</span><span class="sxs-lookup"><span data-stu-id="22c84-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-243">13817 (0x35F9)</span><span class="sxs-lookup"><span data-stu-id="22c84-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-244">Falha na verificação de revogação de certificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERRO \_ de \_ \_ uso de \_ chave \_ inválido de IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="22c84-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-246">13818 (0x35FA)</span><span class="sxs-lookup"><span data-stu-id="22c84-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-247">Uso inválido de chave de certificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERRO \_ \_ tipo de certificado IPSec IKE \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-249">13819 (0x35FB)</span><span class="sxs-lookup"><span data-stu-id="22c84-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-250">Tipo de certificado inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ \_ chave privada**</span><span class="sxs-lookup"><span data-stu-id="22c84-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-252">13820 (0x35FC)</span><span class="sxs-lookup"><span data-stu-id="22c84-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-253">A negociação IKE falhou porque o certificado da máquina usado não tem uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="22c84-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="22c84-254">Os certificados IPsec exigem uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="22c84-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="22c84-255">Entre em contato com o administrador de segurança de rede para substituir por um certificado que tenha uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="22c84-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERRO \_ de \_ \_ rechaveamento simultâneo de Ike de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-257">13821 (0x35FD)</span><span class="sxs-lookup"><span data-stu-id="22c84-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-258">Foram detectadas rechaves simultâneas.</span><span class="sxs-lookup"><span data-stu-id="22c84-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERRO de \_ falha de IPSec \_ Ike \_ DH \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-260">13822 (0x35FE)</span><span class="sxs-lookup"><span data-stu-id="22c84-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-261">Falha na computação Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="22c84-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERRO \_ de \_ \_ carga crítica IPSec IKE \_ \_ não \_ reconhecida**</span><span class="sxs-lookup"><span data-stu-id="22c84-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-263">13823 (0x35FF)</span><span class="sxs-lookup"><span data-stu-id="22c84-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-264">Não sabe como processar a carga crítica.</span><span class="sxs-lookup"><span data-stu-id="22c84-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERRO \_ de \_ \_ cabeçalho inválido de IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-266">13824 (0x3600)</span><span class="sxs-lookup"><span data-stu-id="22c84-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-267">Cabeçalho inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ política**</span><span class="sxs-lookup"><span data-stu-id="22c84-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-269">13825 (0x3601)</span><span class="sxs-lookup"><span data-stu-id="22c84-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-270">Nenhuma política configurada.</span><span class="sxs-lookup"><span data-stu-id="22c84-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERRO \_ de \_ assinatura de IKE IPSec \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-272">13826 (0x3602)</span><span class="sxs-lookup"><span data-stu-id="22c84-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-273">Falha ao verificar assinatura.</span><span class="sxs-lookup"><span data-stu-id="22c84-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**erro \_ de \_ Kerberos Ike de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-275">13827 (0x3603)</span><span class="sxs-lookup"><span data-stu-id="22c84-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-276">Falha ao autenticar usando Kerberos.</span><span class="sxs-lookup"><span data-stu-id="22c84-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ \_ chave pública**</span><span class="sxs-lookup"><span data-stu-id="22c84-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-278">13828 (0x3604)</span><span class="sxs-lookup"><span data-stu-id="22c84-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-279">O certificado do par não tinha uma chave pública.</span><span class="sxs-lookup"><span data-stu-id="22c84-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERRO \_ de \_ processo Ike de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-281">13829 (0x3605)</span><span class="sxs-lookup"><span data-stu-id="22c84-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-282">Erro ao processar carga de erro.</span><span class="sxs-lookup"><span data-stu-id="22c84-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERRO \_ de \_ processo Ike de IPSec Error \_ \_ \_ SA**</span><span class="sxs-lookup"><span data-stu-id="22c84-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-284">13830 (0x3606)</span><span class="sxs-lookup"><span data-stu-id="22c84-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-285">Erro ao processar carga SA.</span><span class="sxs-lookup"><span data-stu-id="22c84-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERRO \_ \_ Ike do \_ processo \_ de \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="22c84-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-287">13831 (0x3607)</span><span class="sxs-lookup"><span data-stu-id="22c84-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-288">Erro ao processar a carga da proposta.</span><span class="sxs-lookup"><span data-stu-id="22c84-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERRO \_ de \_ \_ transação do processo Ike \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-290">13832 (0x3608)</span><span class="sxs-lookup"><span data-stu-id="22c84-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-291">Erro ao processar carga de transformação.</span><span class="sxs-lookup"><span data-stu-id="22c84-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERRO \_ de \_ processo IKE IPSec \_ \_ Err \_ ke**</span><span class="sxs-lookup"><span data-stu-id="22c84-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-293">13833 (0x3609)</span><span class="sxs-lookup"><span data-stu-id="22c84-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-294">Erro ao processar carga de KE.</span><span class="sxs-lookup"><span data-stu-id="22c84-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERRO \_ de \_ \_ ID do processo Ike \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-296">13834 (0x360A)</span><span class="sxs-lookup"><span data-stu-id="22c84-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-297">Erro ao processar carga de ID.</span><span class="sxs-lookup"><span data-stu-id="22c84-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERRO \_ de \_ certificado IKE do \_ processo IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-299">13835 (0x360B)</span><span class="sxs-lookup"><span data-stu-id="22c84-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-300">Erro ao processar carga de certificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERRO \_ de \_ certificado IKE do processo de IPSec \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-302">13836 (0x360C)</span><span class="sxs-lookup"><span data-stu-id="22c84-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-303">Erro ao processar carga de solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERRO \_ de \_ \_ hash do processo Ike \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-305">13837 (0x360D)</span><span class="sxs-lookup"><span data-stu-id="22c84-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-306">Erro ao processar carga de hash.</span><span class="sxs-lookup"><span data-stu-id="22c84-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERRO \_ \_ IKE IPSec \_ processo \_ Err \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="22c84-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-308">13838 (0x360E)</span><span class="sxs-lookup"><span data-stu-id="22c84-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-309">Erro ao processar carga de assinatura.</span><span class="sxs-lookup"><span data-stu-id="22c84-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERRO de \_ processo de Ike de IPSec \_ \_ \_ \_ innonce**</span><span class="sxs-lookup"><span data-stu-id="22c84-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-311">13839 (0x360F)</span><span class="sxs-lookup"><span data-stu-id="22c84-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-312">Erro ao processar carga nonce.</span><span class="sxs-lookup"><span data-stu-id="22c84-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERRO de notificação de erros de \_ \_ processo IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-314">13840 (0x3610)</span><span class="sxs-lookup"><span data-stu-id="22c84-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-315">Erro ao processar a carga de notificação.</span><span class="sxs-lookup"><span data-stu-id="22c84-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERRO \_ de \_ \_ exclusão do processo Ike \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-317">13841 (0x3611)</span><span class="sxs-lookup"><span data-stu-id="22c84-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-318">Erro ao processar a carga de exclusão.</span><span class="sxs-lookup"><span data-stu-id="22c84-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERRO de fornecedor de erros de \_ \_ processo IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-320">13842 (0x3612)</span><span class="sxs-lookup"><span data-stu-id="22c84-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-321">Erro ao processar a carga de VendorID.</span><span class="sxs-lookup"><span data-stu-id="22c84-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERRO \_ de \_ \_ carga inválida de IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-323">13843 (0x3613)</span><span class="sxs-lookup"><span data-stu-id="22c84-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-324">Carga inválida recebida.</span><span class="sxs-lookup"><span data-stu-id="22c84-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERRO de \_ IP \_ Ike de \_ carga \_ \_ de IPSec**</span><span class="sxs-lookup"><span data-stu-id="22c84-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-326">13844 (0x3614)</span><span class="sxs-lookup"><span data-stu-id="22c84-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-327">SA suave carregado.</span><span class="sxs-lookup"><span data-stu-id="22c84-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERRO \_ IPSec \_ Ike \_ Soft \_ SA \_ rasgado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-329">13845 (0x3615)</span><span class="sxs-lookup"><span data-stu-id="22c84-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-330">SA suave interrompida.</span><span class="sxs-lookup"><span data-stu-id="22c84-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERRO de \_ cookie de IPSec \_ Ike \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-332">13846 (0x3616)</span><span class="sxs-lookup"><span data-stu-id="22c84-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-333">Cookie inválido recebido.</span><span class="sxs-lookup"><span data-stu-id="22c84-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERRO \_ IPSec \_ Ike \_ no \_ par de \_ certificados**</span><span class="sxs-lookup"><span data-stu-id="22c84-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-335">13847 (0x3617)</span><span class="sxs-lookup"><span data-stu-id="22c84-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-336">O par não pôde enviar um certificado de máquina válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERRO \_ \_ falha de \_ CRL de par Ike \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-338">13848 (0x3618)</span><span class="sxs-lookup"><span data-stu-id="22c84-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-339">Falha na verificação de revogação da certificação do certificado do par.</span><span class="sxs-lookup"><span data-stu-id="22c84-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERRO \_ na \_ \_ alteração da política IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-341">13849 (0x3619)</span><span class="sxs-lookup"><span data-stu-id="22c84-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-342">Nova SAs invalidada de política formada com política antiga.</span><span class="sxs-lookup"><span data-stu-id="22c84-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERRO \_ de \_ política IPSec IKE \_ não \_ mm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-344">13850 (0x361A)</span><span class="sxs-lookup"><span data-stu-id="22c84-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-345">Não há nenhuma política IKE de modo principal disponível.</span><span class="sxs-lookup"><span data-stu-id="22c84-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERRO de \_ IPSec \_ Ike \_ NOTCBPRIV**</span><span class="sxs-lookup"><span data-stu-id="22c84-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-347">13851 (0x361B)</span><span class="sxs-lookup"><span data-stu-id="22c84-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-348">Falha ao habilitar o privilégio TCB.</span><span class="sxs-lookup"><span data-stu-id="22c84-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERRO de \_ IPSec \_ Ike \_ SECLOADFAIL**</span><span class="sxs-lookup"><span data-stu-id="22c84-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-350">13852 (0x361C)</span><span class="sxs-lookup"><span data-stu-id="22c84-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-351">Falha ao carregar SECURITY.DLL.</span><span class="sxs-lookup"><span data-stu-id="22c84-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERRO de \_ IPSec \_ Ike \_ FAILSSPINIT**</span><span class="sxs-lookup"><span data-stu-id="22c84-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-353">13853 (0x361D)</span><span class="sxs-lookup"><span data-stu-id="22c84-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-354">Falha ao obter o endereço de expedição da tabela da função de segurança do SSPI.</span><span class="sxs-lookup"><span data-stu-id="22c84-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERRO de \_ IPSec \_ Ike \_ FAILQUERYSSP**</span><span class="sxs-lookup"><span data-stu-id="22c84-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-356">13854 (0x361E)</span><span class="sxs-lookup"><span data-stu-id="22c84-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-357">Falha ao consultar o pacote Kerberos para obter o tamanho máximo do token.</span><span class="sxs-lookup"><span data-stu-id="22c84-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERRO de \_ IPSec \_ Ike \_ SRVACQFAIL**</span><span class="sxs-lookup"><span data-stu-id="22c84-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-359">13855 (0x361F)</span><span class="sxs-lookup"><span data-stu-id="22c84-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-360">Falha ao obter as credenciais do servidor Kerberos para ISAKMP/erro \_ IPSec \_ Ike Service.</span><span class="sxs-lookup"><span data-stu-id="22c84-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="22c84-361">A autenticação Kerberos não funcionará.</span><span class="sxs-lookup"><span data-stu-id="22c84-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="22c84-362">O motivo mais provável para isso é a falta de associação de domínio.</span><span class="sxs-lookup"><span data-stu-id="22c84-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="22c84-363">Isso é normal se o computador for membro de um grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22c84-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERRO de \_ IPSec \_ Ike \_ SRVQUERYCRED**</span><span class="sxs-lookup"><span data-stu-id="22c84-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-365">13856 (0x3620)</span><span class="sxs-lookup"><span data-stu-id="22c84-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-366">Falha ao determinar o nome da entidade de segurança SSPI para ISAKMP/erro \_ IPSec \_ Ike Service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span><span class="sxs-lookup"><span data-stu-id="22c84-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERRO de \_ IPSec \_ Ike \_ GETSPIFAIL**</span><span class="sxs-lookup"><span data-stu-id="22c84-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-368">13857 (0x3621)</span><span class="sxs-lookup"><span data-stu-id="22c84-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-369">Falha ao obter o novo SPI para o SA de entrada do Driver IPsec.</span><span class="sxs-lookup"><span data-stu-id="22c84-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="22c84-370">A causa mais comum para isso é que o driver não tem o filtro correto.</span><span class="sxs-lookup"><span data-stu-id="22c84-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="22c84-371">Verifique sua política para verificar os filtros.</span><span class="sxs-lookup"><span data-stu-id="22c84-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERRO \_ de \_ \_ filtro inválido de IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-373">13858 (0x3622)</span><span class="sxs-lookup"><span data-stu-id="22c84-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-374">O filtro fornecido é inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERRO \_ \_ IKE IPSec \_ sem \_ \_ memória**</span><span class="sxs-lookup"><span data-stu-id="22c84-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-376">13859 (0x3623)</span><span class="sxs-lookup"><span data-stu-id="22c84-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-377">Falha na alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="22c84-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERRO \_ IPSec \_ Ike \_ \_ \_ falha ao adicionar chave de atualização \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-379">13860 (0x3624)</span><span class="sxs-lookup"><span data-stu-id="22c84-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-380">Falha ao adicionar Associação de segurança ao Driver IPsec.</span><span class="sxs-lookup"><span data-stu-id="22c84-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="22c84-381">A causa mais comum para isso é se a negociação IKE demorou muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="22c84-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="22c84-382">Se o problema persistir, reduza a carga no computador com falha.</span><span class="sxs-lookup"><span data-stu-id="22c84-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERRO \_ de \_ política de Ike \_ inválida IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-384">13861 (0x3625)</span><span class="sxs-lookup"><span data-stu-id="22c84-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-385">Política inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERRO \_ de \_ doi de Ike \_ desconhecido IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-387">13862 (0x3626)</span><span class="sxs-lookup"><span data-stu-id="22c84-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-388">DOI inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERRO \_ de \_ situação de Ike \_ inválida de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-390">13863 (0x3627)</span><span class="sxs-lookup"><span data-stu-id="22c84-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-391">Situação inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERRO \_ de \_ \_ falha DH IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-393">13864 (0x3628)</span><span class="sxs-lookup"><span data-stu-id="22c84-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-394">Falha de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="22c84-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERRO \_ de \_ \_ grupo inválido de IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-396">13865 (0x3629)</span><span class="sxs-lookup"><span data-stu-id="22c84-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-397">Grupo de Diffie-Hellman inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERRO \_ de \_ criptografia IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-399">13866 (0x362A)</span><span class="sxs-lookup"><span data-stu-id="22c84-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-400">Erro ao criptografar a carga.</span><span class="sxs-lookup"><span data-stu-id="22c84-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERRO \_ de \_ descriptografia de IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-402">13867 (0x362B)</span><span class="sxs-lookup"><span data-stu-id="22c84-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-403">Erro ao descriptografar a carga.</span><span class="sxs-lookup"><span data-stu-id="22c84-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERRO \_ de \_ \_ correspondência de política IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-405">13868 (0x362C)</span><span class="sxs-lookup"><span data-stu-id="22c84-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-406">Erro de correspondência de política.</span><span class="sxs-lookup"><span data-stu-id="22c84-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERRO \_ de \_ \_ ID incompatível de IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-408">13869 (0x362D)</span><span class="sxs-lookup"><span data-stu-id="22c84-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-409">ID sem suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERRO de \_ hash de IPSec \_ Ike \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-411">13870 (0x362E)</span><span class="sxs-lookup"><span data-stu-id="22c84-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-412">Falha na verificação de hash.</span><span class="sxs-lookup"><span data-stu-id="22c84-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERRO \_ de \_ hash de IP Ike \_ inválido \_ \_ alg**</span><span class="sxs-lookup"><span data-stu-id="22c84-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-414">13871 (0x362F)</span><span class="sxs-lookup"><span data-stu-id="22c84-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-415">Algoritmo de hash inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERRO \_ de \_ \_ tamanho de \_ hash \_ inválido de IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="22c84-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-417">13872 (0x3630)</span><span class="sxs-lookup"><span data-stu-id="22c84-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-418">Tamanho de hash inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERRO \_ \_ IKE IPSec \_ inválido \_ criptografar \_ alg**</span><span class="sxs-lookup"><span data-stu-id="22c84-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-420">13873 (0x3631)</span><span class="sxs-lookup"><span data-stu-id="22c84-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-421">Algoritmo de criptografia inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERRO \_ de \_ autenticação de IP Ike \_ inválido \_ \_ alg**</span><span class="sxs-lookup"><span data-stu-id="22c84-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-423">13874 (0x3632)</span><span class="sxs-lookup"><span data-stu-id="22c84-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-424">Algoritmo de autenticação inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERRO \_ de \_ SIG IPSec IKE \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-426">13875 (0x3633)</span><span class="sxs-lookup"><span data-stu-id="22c84-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-427">Assinatura de certificado inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERRO \_ \_ \_ ao carregar Ike de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-429">13876 (0x3634)</span><span class="sxs-lookup"><span data-stu-id="22c84-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-430">Falha no carregamento.</span><span class="sxs-lookup"><span data-stu-id="22c84-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERRO \_ de \_ \_ exclusão de RPC IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-432">13877 (0x3635)</span><span class="sxs-lookup"><span data-stu-id="22c84-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-433">Excluído via chamada RPC.</span><span class="sxs-lookup"><span data-stu-id="22c84-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERRO \_ de \_ \_ reinicialização de Ike de IPSec benigno \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-435">13878 (0x3636)</span><span class="sxs-lookup"><span data-stu-id="22c84-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-436">Estado temporário criado para executar a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="22c84-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="22c84-437">Isso não é uma falha real.</span><span class="sxs-lookup"><span data-stu-id="22c84-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERRO \_ ao \_ \_ \_ \_ notificador de tempo de resposta de Ike inválido de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-439">13879 (0x3637)</span><span class="sxs-lookup"><span data-stu-id="22c84-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-440">O valor de tempo de vida recebido na notificação de tempo de vida do respondente está abaixo do valor mínimo configurado para o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="22c84-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="22c84-441">Corrija a política na máquina par.</span><span class="sxs-lookup"><span data-stu-id="22c84-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERRO \_ de \_ \_ \_ versão principal inválida de IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-443">13880 (0x3638)</span><span class="sxs-lookup"><span data-stu-id="22c84-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-444">O destinatário não pode manipular a versão do IKE especificada no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="22c84-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERRO \_ de \_ certificado IPSec IKE \_ inválido \_ \_ KEYLEN**</span><span class="sxs-lookup"><span data-stu-id="22c84-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-446">13881 (0x3639)</span><span class="sxs-lookup"><span data-stu-id="22c84-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-447">O comprimento da chave no certificado é muito pequeno para os requisitos de segurança configurados.</span><span class="sxs-lookup"><span data-stu-id="22c84-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERRO \_ de \_ limite de Ike mm de IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-449">13882 (0x363A)</span><span class="sxs-lookup"><span data-stu-id="22c84-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-450">Número máximo de SAs MM estabelecido para par excedido.</span><span class="sxs-lookup"><span data-stu-id="22c84-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERRO \_ de \_ negociação IKE IPSec \_ \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="22c84-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-452">13883 (0x363B)</span><span class="sxs-lookup"><span data-stu-id="22c84-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-453">O IKE recebeu uma política que desabilita a negociação.</span><span class="sxs-lookup"><span data-stu-id="22c84-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERRO de \_ limite de IPSec \_ Ike \_ qm \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-455">13884 (0x363C)</span><span class="sxs-lookup"><span data-stu-id="22c84-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-456">Limite máximo de modo rápido atingido para o modo principal.</span><span class="sxs-lookup"><span data-stu-id="22c84-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="22c84-457">O novo modo principal será iniciado.</span><span class="sxs-lookup"><span data-stu-id="22c84-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERRO \_ \_ Ike mm de IPSec \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="22c84-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-459">13885 (0x363D)</span><span class="sxs-lookup"><span data-stu-id="22c84-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-460">O tempo de vida da SA de modo principal expirou ou o par enviou uma exclusão de modo principal.</span><span class="sxs-lookup"><span data-stu-id="22c84-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERRO \_ IPSec \_ Ike \_ peer \_ mm \_ considerado \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-462">13886 (0x363E)</span><span class="sxs-lookup"><span data-stu-id="22c84-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-463">SA de modo principal assumido como inválido porque o par parou de responder.</span><span class="sxs-lookup"><span data-stu-id="22c84-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERRO \_ de \_ \_ \_ \_ incompatibilidade de política de cadeia de certificado IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-465">13887 (0x363F)</span><span class="sxs-lookup"><span data-stu-id="22c84-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-466">O certificado não se encadea a uma raiz confiável na política IPsec.</span><span class="sxs-lookup"><span data-stu-id="22c84-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERRO \_ de \_ \_ ID de \_ mensagem \_ inesperada IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="22c84-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-468">13888 (0x3640)</span><span class="sxs-lookup"><span data-stu-id="22c84-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-469">ID de mensagem inesperada recebida.</span><span class="sxs-lookup"><span data-stu-id="22c84-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERRO \_ de \_ \_ carga de \_ autenticação inválida de IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-471">13889 (0x3641)</span><span class="sxs-lookup"><span data-stu-id="22c84-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-472">Ofertas de autenticação inválidas recebidas.</span><span class="sxs-lookup"><span data-stu-id="22c84-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERRO \_ de \_ cookie de dos IPSec IKE \_ \_ \_ enviado**</span><span class="sxs-lookup"><span data-stu-id="22c84-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-474">13890 (0x3642)</span><span class="sxs-lookup"><span data-stu-id="22c84-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-475">Enviada notificação de cookie DoS para o iniciador.</span><span class="sxs-lookup"><span data-stu-id="22c84-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERRO \_ de \_ \_ desligamento de IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-477">13891 (0x3643)</span><span class="sxs-lookup"><span data-stu-id="22c84-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-478">O serviço IKE está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="22c84-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERRO \_ de \_ \_ autenticação CGA IPSec IKE \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="22c84-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-480">13892 (0x3644)</span><span class="sxs-lookup"><span data-stu-id="22c84-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-481">Não foi possível verificar a associação entre o endereço CGA e o certificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERRO \_ de \_ processo Ike de IPSec \_ \_ \_ NATOA**</span><span class="sxs-lookup"><span data-stu-id="22c84-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-483">13893 (0x3645)</span><span class="sxs-lookup"><span data-stu-id="22c84-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-484">Erro ao processar carga NatOA.</span><span class="sxs-lookup"><span data-stu-id="22c84-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERRO \_ \_ de IPSec IKE \_ inválido \_ mm \_ para \_ QM**</span><span class="sxs-lookup"><span data-stu-id="22c84-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-486">13894 (0x3646)</span><span class="sxs-lookup"><span data-stu-id="22c84-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-487">Os parâmetros do modo principal são inválidos para este modo rápido.</span><span class="sxs-lookup"><span data-stu-id="22c84-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERRO \_ \_ IKE IPSec \_ qm \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="22c84-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-489">13895 (0x3647)</span><span class="sxs-lookup"><span data-stu-id="22c84-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-490">O SA de modo rápido expirou pelo driver IPsec.</span><span class="sxs-lookup"><span data-stu-id="22c84-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERRO \_ Ike de IPSec em muitos \_ \_ \_ \_ filtros**</span><span class="sxs-lookup"><span data-stu-id="22c84-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-492">13896 (0x3648)</span><span class="sxs-lookup"><span data-stu-id="22c84-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-493">Muitos filtros IKEEXT adicionados dinamicamente foram detectados.</span><span class="sxs-lookup"><span data-stu-id="22c84-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERRO \_ de \_ \_ neg de \_ status de IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-495">13897 (0x3649)</span><span class="sxs-lookup"><span data-stu-id="22c84-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-496">ERRO \_ de \_ \_ neg de \_ status de IKE IPSec \_</span><span class="sxs-lookup"><span data-stu-id="22c84-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERRO \_ IPSec \_ Ike \_ Kill \_ fictícia \_ NAP \_ Tunnel**</span><span class="sxs-lookup"><span data-stu-id="22c84-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-498">13898 (0x364A)</span><span class="sxs-lookup"><span data-stu-id="22c84-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-499">A reautenticação de NAP foi bem-sucedida e deve excluir o túnel IKEv2 NAP fictício.</span><span class="sxs-lookup"><span data-stu-id="22c84-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERRO \_ \_ \_ \_ na atribuição de IP \_ interno \_ Ike do IPSec**</span><span class="sxs-lookup"><span data-stu-id="22c84-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-501">13899 (0x364B)</span><span class="sxs-lookup"><span data-stu-id="22c84-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-502">Erro ao atribuir o endereço IP interno ao iniciador no modo de túnel.</span><span class="sxs-lookup"><span data-stu-id="22c84-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERRO \_ \_ IKE IPSec \_ requer \_ conteúdo de CP \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="22c84-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-504">13900 (0x364C)</span><span class="sxs-lookup"><span data-stu-id="22c84-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-505">Requer carga de configuração ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERRO \_ de \_ negociação de representação de módulo de chave IPSec \_ \_ \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="22c84-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-507">13901 (0x364D)</span><span class="sxs-lookup"><span data-stu-id="22c84-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-508">Uma negociação em execução como o princípio de segurança que emitiu a conexão está em andamento.</span><span class="sxs-lookup"><span data-stu-id="22c84-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERRO \_ de \_ \_ supressão de coexistência de IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-510">13902 (0x364E)</span><span class="sxs-lookup"><span data-stu-id="22c84-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-511">SA foi excluído devido à verificação de supressão de coexistência de IKEv1/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="22c84-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERRO \_ IPSec \_ Ike \_ RATELIMIT \_ drop**</span><span class="sxs-lookup"><span data-stu-id="22c84-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-513">13903 (0x364F)</span><span class="sxs-lookup"><span data-stu-id="22c84-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-514">A solicitação SA de entrada foi descartada devido à limitação da taxa de endereço IP do par.</span><span class="sxs-lookup"><span data-stu-id="22c84-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERRO \_ IPSec \_ Ike \_ peer \_ \_ não dá suporte a \_ MOBIKE**</span><span class="sxs-lookup"><span data-stu-id="22c84-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-516">13904 (0x3650)</span><span class="sxs-lookup"><span data-stu-id="22c84-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-517">O par não dá suporte a MOBIKE.</span><span class="sxs-lookup"><span data-stu-id="22c84-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERRO \_ de \_ \_ falha de autorização \_ de IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="22c84-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-519">13905 (0x3651)</span><span class="sxs-lookup"><span data-stu-id="22c84-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-520">Estabelecimento de SA não autorizado.</span><span class="sxs-lookup"><span data-stu-id="22c84-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERRO \_ de \_ \_ falha de \_ autorização de credenciais fortes \_ IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-522">13906 (0x3652)</span><span class="sxs-lookup"><span data-stu-id="22c84-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-523">O estabelecimento de SA não é autorizado porque não há uma credencial baseada em PKINIT suficientemente forte.</span><span class="sxs-lookup"><span data-stu-id="22c84-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERRO \_ \_ \_ \_ de falha de autorização IKE IPSec \_ com \_ \_ repetição opcional**</span><span class="sxs-lookup"><span data-stu-id="22c84-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-525">13907 (0x3653)</span><span class="sxs-lookup"><span data-stu-id="22c84-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-526">Estabelecimento de SA não autorizado.</span><span class="sxs-lookup"><span data-stu-id="22c84-526">SA establishment is not authorized.</span></span> <span data-ttu-id="22c84-527">Talvez seja necessário inserir credenciais atualizadas ou diferentes, como um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="22c84-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERRO \_ \_ \_ \_ \_ de autorização de credenciais fortes \_ de Ike de IPSec e \_ falha de CERTMAP \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-529">13908 (0x3654)</span><span class="sxs-lookup"><span data-stu-id="22c84-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-530">O estabelecimento de SA não é autorizado porque não há uma credencial baseada em PKINIT suficientemente forte.</span><span class="sxs-lookup"><span data-stu-id="22c84-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="22c84-531">Isso pode estar relacionado à falha de mapeamento de certificado para conta para o SA.</span><span class="sxs-lookup"><span data-stu-id="22c84-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERRO \_ IPSec \_ Ike \_ neg de \_ status \_ estendido \_ final**</span><span class="sxs-lookup"><span data-stu-id="22c84-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-533">13909 (0x3655)</span><span class="sxs-lookup"><span data-stu-id="22c84-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-534">ERRO \_ IPSec \_ Ike \_ neg de \_ status \_ estendido \_ final</span><span class="sxs-lookup"><span data-stu-id="22c84-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERRO \_ SPI de IPSec \_ insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-536">13910 (0x3656)</span><span class="sxs-lookup"><span data-stu-id="22c84-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-537">O SPI no pacote não corresponde a um SA IPsec válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERRO \_ de \_ tempo de vida da SA IPsec \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="22c84-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-539">13911 (0x3657)</span><span class="sxs-lookup"><span data-stu-id="22c84-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-540">O pacote foi recebido em um SA IPsec cujo tempo de vida expirou.</span><span class="sxs-lookup"><span data-stu-id="22c84-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERRO de \_ IPSec \_ errado \_ SA**</span><span class="sxs-lookup"><span data-stu-id="22c84-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-542">13912 (0x3658)</span><span class="sxs-lookup"><span data-stu-id="22c84-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-543">O pacote foi recebido em um SA IPsec que não corresponde às características do pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERRO \_ de \_ verificação de reprodução de IPSec \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="22c84-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-545">13913 (0x3659)</span><span class="sxs-lookup"><span data-stu-id="22c84-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-546">Falha na verificação de repetição do número de sequência de pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERRO de \_ pacote de IPSec \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-548">13914 (0x365A)</span><span class="sxs-lookup"><span data-stu-id="22c84-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-549">O cabeçalho IPsec e/ou o trailer no pacote é inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERRO \_ \_ na verificação de integridade do IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-551">13915 (0x365B)</span><span class="sxs-lookup"><span data-stu-id="22c84-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-552">Falha na verificação de integridade do IPsec.</span><span class="sxs-lookup"><span data-stu-id="22c84-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERRO \_ ao \_ \_ remover texto não criptografado IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-554">13916 (0x365C)</span><span class="sxs-lookup"><span data-stu-id="22c84-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-555">O IPsec removeu um pacote de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="22c84-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERRO \_ ao \_ \_ remover firewall de autenticação IPsec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-557">13917 (0x365D)</span><span class="sxs-lookup"><span data-stu-id="22c84-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-558">O IPsec removeu um pacote ESP de entrada no modo de firewall autenticado.</span><span class="sxs-lookup"><span data-stu-id="22c84-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="22c84-559">Essa queda é benigna.</span><span class="sxs-lookup"><span data-stu-id="22c84-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERRO \_ ao \_ remover limitação IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-561">13918 (0x365E)</span><span class="sxs-lookup"><span data-stu-id="22c84-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-562">O IPsec removeu um pacote devido à limitação do DoS.</span><span class="sxs-lookup"><span data-stu-id="22c84-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERRO \_ de \_ bloqueio de DOSP IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-564">13925 (0x3665)</span><span class="sxs-lookup"><span data-stu-id="22c84-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-565">A proteção de DoS IPsec correspondeu a uma regra de bloqueio explícita.</span><span class="sxs-lookup"><span data-stu-id="22c84-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERRO \_ IPSec \_ DOSP \_ recebido \_ multicast**</span><span class="sxs-lookup"><span data-stu-id="22c84-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-567">13926 (0x3666)</span><span class="sxs-lookup"><span data-stu-id="22c84-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-568">A proteção de DoS IPsec recebeu um pacote multicast específico de IPsec que não é permitido.</span><span class="sxs-lookup"><span data-stu-id="22c84-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERRO de \_ pacote de IPSec \_ DOSP \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-570">13927 (0x3667)</span><span class="sxs-lookup"><span data-stu-id="22c84-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-571">A proteção de DoS IPsec recebeu um pacote formatado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="22c84-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERRO \_ de \_ pesquisa de estado de DOSP IPSec \_ \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="22c84-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-573">13928 (0x3668)</span><span class="sxs-lookup"><span data-stu-id="22c84-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-574">A proteção do DoS IPsec falhou ao pesquisar o estado.</span><span class="sxs-lookup"><span data-stu-id="22c84-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERRO \_ ao \_ DOSP \_ máximo de \_ entradas IPSec**</span><span class="sxs-lookup"><span data-stu-id="22c84-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-576">13929 (0x3669)</span><span class="sxs-lookup"><span data-stu-id="22c84-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-577">Falha na proteção do DoS IPsec ao criar o estado porque o número máximo de entradas permitidas pela política foi atingido.</span><span class="sxs-lookup"><span data-stu-id="22c84-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERRO \_ IPSec \_ DOSP \_ KEYMOD \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="22c84-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-579">13930 (0x366A)</span><span class="sxs-lookup"><span data-stu-id="22c84-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-580">A proteção de DoS IPsec recebeu um pacote de negociação IPsec para um módulo de chaveamento que não é permitido pela política.</span><span class="sxs-lookup"><span data-stu-id="22c84-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERRO \_ \_ DOSP IPSec \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="22c84-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-582">13931 (0x366B)</span><span class="sxs-lookup"><span data-stu-id="22c84-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-583">A proteção de DoS IPsec não foi habilitada.</span><span class="sxs-lookup"><span data-stu-id="22c84-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERRO \_ de \_ DOSP \_ máximo de IPSec \_ por \_ filas de RATELIMIT de IP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-585">13932 (0x366C)</span><span class="sxs-lookup"><span data-stu-id="22c84-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-586">Falha na proteção do DoS IPsec ao criar uma fila por limite de taxa IP interna porque o número máximo de filas permitidas pela política foi atingido.</span><span class="sxs-lookup"><span data-stu-id="22c84-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERRO \_ na \_ seção SxS \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-588">14000 (0x36B0)</span><span class="sxs-lookup"><span data-stu-id="22c84-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-589">A seção solicitada não estava presente no contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="22c84-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERRO \_ SxS não é \_ \_ Gen \_ ACTCTX**</span><span class="sxs-lookup"><span data-stu-id="22c84-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-591">14001 (0x36B1)</span><span class="sxs-lookup"><span data-stu-id="22c84-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-592">Falha ao iniciar o aplicativo porque sua configuração lado a lado está incorreta.</span><span class="sxs-lookup"><span data-stu-id="22c84-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="22c84-593">Consulte o log de eventos do aplicativo ou use a ferramenta de sxstrace.exe de linha de comando para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="22c84-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERRO \_ do \_ \_ formato ACTCTXDATA \_ inválido de SXS**</span><span class="sxs-lookup"><span data-stu-id="22c84-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-595">14002 (0x36B2)</span><span class="sxs-lookup"><span data-stu-id="22c84-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-596">O formato de dados de associação de aplicativo é inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERRO \_ de \_ assembly SxS \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-598">14003 (0x36B3)</span><span class="sxs-lookup"><span data-stu-id="22c84-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-599">O assembly referenciado não está instalado no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="22c84-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**erro \_ de \_ formato de manifesto SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-601">14004 (0x36B4)</span><span class="sxs-lookup"><span data-stu-id="22c84-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-602">O arquivo de manifesto não começa com as informações de marca e formato necessárias.</span><span class="sxs-lookup"><span data-stu-id="22c84-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**erro \_ de \_ análise do manifesto SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-604">14005 (0x36B5)</span><span class="sxs-lookup"><span data-stu-id="22c84-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-605">O arquivo de manifesto contém um ou mais erros de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="22c84-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERRO \_ de \_ contexto de ativação SxS \_ \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="22c84-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-607">14006 (0x36B6)</span><span class="sxs-lookup"><span data-stu-id="22c84-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-608">O aplicativo tentou ativar um contexto de ativação desabilitado.</span><span class="sxs-lookup"><span data-stu-id="22c84-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERRO \_ de \_ chave SxS \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-610">14007 (0x36B7)</span><span class="sxs-lookup"><span data-stu-id="22c84-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-611">A chave de pesquisa solicitada não foi encontrada em nenhum contexto de ativação ativo.</span><span class="sxs-lookup"><span data-stu-id="22c84-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERRO \_ de \_ conflito de versão de SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-613">14008 (0x36B8)</span><span class="sxs-lookup"><span data-stu-id="22c84-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-614">Uma versão de componente exigida pelo aplicativo está em conflito com outra versão de componente já ativa.</span><span class="sxs-lookup"><span data-stu-id="22c84-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERRO \_ de \_ \_ tipo de seção errado de SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-616">14009 (0x36B9)</span><span class="sxs-lookup"><span data-stu-id="22c84-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-617">O tipo de seção de contexto de ativação solicitado não corresponde à API de consulta usada.</span><span class="sxs-lookup"><span data-stu-id="22c84-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERRO \_ de \_ consultas de thread SxS \_ \_ desabilitadas**</span><span class="sxs-lookup"><span data-stu-id="22c84-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-619">14010 (0x36BA)</span><span class="sxs-lookup"><span data-stu-id="22c84-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-620">A falta de recursos do sistema exigiu que a ativação isolada fosse desabilitada para o thread atual de execução.</span><span class="sxs-lookup"><span data-stu-id="22c84-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERRO \_ de \_ processo SxS o \_ padrão \_ já está \_ definido**</span><span class="sxs-lookup"><span data-stu-id="22c84-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-622">14011 (0x36BB)</span><span class="sxs-lookup"><span data-stu-id="22c84-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-623">Falha ao tentar definir o contexto de ativação padrão do processo porque o contexto de ativação padrão do processo já foi definido.</span><span class="sxs-lookup"><span data-stu-id="22c84-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERRO \_ grupo de codificação de SxS \_ desconhecido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-625">14012 (0x36BC)</span><span class="sxs-lookup"><span data-stu-id="22c84-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-626">O identificador do grupo de codificação especificado não é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="22c84-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERRO de \_ codificação de SxS \_ desconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-628">14013 (0x36BD)</span><span class="sxs-lookup"><span data-stu-id="22c84-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-629">A codificação solicitada não é reconhecida.</span><span class="sxs-lookup"><span data-stu-id="22c84-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERRO \_ \_ URI de \_ namespace XML inválido \_ SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-631">14014 (0x36BE)</span><span class="sxs-lookup"><span data-stu-id="22c84-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-632">O manifesto contém uma referência a um URI inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERRO \_ de \_ dependência de manifesto raiz SxS \_ \_ \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="22c84-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-634">14015 (0x36BF)</span><span class="sxs-lookup"><span data-stu-id="22c84-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-635">O manifesto do aplicativo contém uma referência a um assembly dependente que não está instalado.</span><span class="sxs-lookup"><span data-stu-id="22c84-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERRO \_ de \_ dependência de manifesto folha SxS \_ \_ \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="22c84-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-637">14016 (0x36C0)</span><span class="sxs-lookup"><span data-stu-id="22c84-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-638">O manifesto para um assembly usado pelo aplicativo tem uma referência a um assembly dependente que não está instalado.</span><span class="sxs-lookup"><span data-stu-id="22c84-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERRO \_ do \_ \_ atributo de identidade de assembly inválido \_ SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-640">14017 (0x36C1)</span><span class="sxs-lookup"><span data-stu-id="22c84-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-641">O manifesto contém um atributo para a identidade do assembly que não é válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERRO \_ de \_ manifesto SxS \_ ausente no \_ \_ namespace padrão necessário \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-643">14018 (0x36C2)</span><span class="sxs-lookup"><span data-stu-id="22c84-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-644">O manifesto não tem a especificação de namespace padrão necessária no elemento assembly.</span><span class="sxs-lookup"><span data-stu-id="22c84-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERRO \_ de \_ manifesto \_ SxS \_ inválido \_ namespace padrão necessário \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-646">14019 (0x36C3)</span><span class="sxs-lookup"><span data-stu-id="22c84-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-647">O manifesto tem um namespace padrão especificado no elemento assembly, mas seu valor não é "urn: schemas-microsoft-com: asm. v1".</span><span class="sxs-lookup"><span data-stu-id="22c84-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERRO \_ \_ de caminho privado do manifesto particular do SxS \_ \_ \_ \_ com \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-649">14020 (0x36C4)</span><span class="sxs-lookup"><span data-stu-id="22c84-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-650">A investigação do manifesto particular cruzou um caminho com um ponto de nova análise sem suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERRO \_ \_ nome de \_ dll duplicado SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-652">14021 (0x36C5)</span><span class="sxs-lookup"><span data-stu-id="22c84-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-653">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm arquivos com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="22c84-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERRO \_ \_ nome de \_ WINDOWCLASS duplicado SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-655">14022 (0x36C6)</span><span class="sxs-lookup"><span data-stu-id="22c84-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-656">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm classes de janela com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="22c84-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERRO \_ de \_ CLSID duplicado de SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-658">14023 (0x36C7)</span><span class="sxs-lookup"><span data-stu-id="22c84-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-659">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm os mesmos CLSIDs de servidor COM.</span><span class="sxs-lookup"><span data-stu-id="22c84-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERRO \_ de \_ IID duplicado de SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-661">14024 (0x36C8)</span><span class="sxs-lookup"><span data-stu-id="22c84-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-662">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm proxies para a mesma interface COM IIDs.</span><span class="sxs-lookup"><span data-stu-id="22c84-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERRO \_ \_ TLBID duplicado SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-664">14025 (0x36C9)</span><span class="sxs-lookup"><span data-stu-id="22c84-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-665">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm a mesma biblioteca de tipos COM TLBIDs.</span><span class="sxs-lookup"><span data-stu-id="22c84-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERRO \_ \_ ProgID duplicado SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-667">14026 (0x36CA)</span><span class="sxs-lookup"><span data-stu-id="22c84-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-668">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm as mesmas ProgIDs COM.</span><span class="sxs-lookup"><span data-stu-id="22c84-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERRO \_ de \_ \_ nome de assembly duplicado SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-670">14027 (0x36CB)</span><span class="sxs-lookup"><span data-stu-id="22c84-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-671">Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo são versões diferentes do mesmo componente que não é permitido.</span><span class="sxs-lookup"><span data-stu-id="22c84-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de hash de arquivo SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-673">14028 (0x36CC)</span><span class="sxs-lookup"><span data-stu-id="22c84-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-674">O arquivo de um componente não corresponde às informações de verificação presentes no manifesto do componente.</span><span class="sxs-lookup"><span data-stu-id="22c84-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**erro \_ de \_ análise de política SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-676">14029 (0x36CD)</span><span class="sxs-lookup"><span data-stu-id="22c84-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-677">O manifesto da política contém um ou mais erros de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="22c84-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGQUOTE**</span><span class="sxs-lookup"><span data-stu-id="22c84-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-679">14030 (0x36CE)</span><span class="sxs-lookup"><span data-stu-id="22c84-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-680">Erro de análise do manifesto: um literal de cadeia de caracteres era esperado, mas nenhum caractere de aspas de abertura foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERRO de \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="22c84-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-682">14031 (0x36CF)</span><span class="sxs-lookup"><span data-stu-id="22c84-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-683">Erro de análise do manifesto: sintaxe incorreta usada em um comentário.</span><span class="sxs-lookup"><span data-stu-id="22c84-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="22c84-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-685">14032 (0x36D0)</span><span class="sxs-lookup"><span data-stu-id="22c84-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-686">Erro de análise do manifesto: um nome foi iniciado com um caractere inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="22c84-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-688">14033 (0x36D1)</span><span class="sxs-lookup"><span data-stu-id="22c84-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-689">Erro de análise do manifesto: um nome continha um caractere inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADCHARINSTRING**</span><span class="sxs-lookup"><span data-stu-id="22c84-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-691">14034 (0x36D2)</span><span class="sxs-lookup"><span data-stu-id="22c84-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-692">Erro de análise do manifesto: um literal de cadeia de caracteres continha um caractere inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERRO de \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="22c84-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-694">14035 (0x36D3)</span><span class="sxs-lookup"><span data-stu-id="22c84-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-695">Erro de análise do manifesto: sintaxe inválida para uma declaração XML.</span><span class="sxs-lookup"><span data-stu-id="22c84-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADCHARDATA**</span><span class="sxs-lookup"><span data-stu-id="22c84-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-697">14036 (0x36D4)</span><span class="sxs-lookup"><span data-stu-id="22c84-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-698">Erro de análise do manifesto: um caractere inválido foi encontrado no conteúdo do texto.</span><span class="sxs-lookup"><span data-stu-id="22c84-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**</span><span class="sxs-lookup"><span data-stu-id="22c84-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-700">14037 (0x36D5)</span><span class="sxs-lookup"><span data-stu-id="22c84-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-701">Erro de análise do manifesto: espaço em branco necessário ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERRO de \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**</span><span class="sxs-lookup"><span data-stu-id="22c84-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-703">14038 (0x36D6)</span><span class="sxs-lookup"><span data-stu-id="22c84-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-704">Erro de análise do manifesto: o caractere ' > ' era esperado.</span><span class="sxs-lookup"><span data-stu-id="22c84-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**</span><span class="sxs-lookup"><span data-stu-id="22c84-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-706">14039 (0x36D7)</span><span class="sxs-lookup"><span data-stu-id="22c84-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-707">Erro de análise do manifesto: um caractere de ponto e vírgula era esperado.</span><span class="sxs-lookup"><span data-stu-id="22c84-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**</span><span class="sxs-lookup"><span data-stu-id="22c84-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-709">14040 (0x36D8)</span><span class="sxs-lookup"><span data-stu-id="22c84-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-710">Erro de análise do manifesto: parênteses desbalanceado.</span><span class="sxs-lookup"><span data-stu-id="22c84-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERRO de \_ SxS \_ XML \_ E \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="22c84-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-712">14041 (0x36D9)</span><span class="sxs-lookup"><span data-stu-id="22c84-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-713">Erro de análise do manifesto: erro interno.</span><span class="sxs-lookup"><span data-stu-id="22c84-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERRO de \_ SxS \_ XML \_ E espaço em \_ branco inesperado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-715">14042 (0x36DA)</span><span class="sxs-lookup"><span data-stu-id="22c84-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-716">Erro de análise do manifesto: espaço em branco não é permitido neste local.</span><span class="sxs-lookup"><span data-stu-id="22c84-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERRO \_ de \_ codificação de XML E de SxS \_ \_ incompleto \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-718">14043 (0x36DB)</span><span class="sxs-lookup"><span data-stu-id="22c84-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-719">Erro de análise do manifesto: fim do arquivo alcançado em estado inválido para a codificação atual.</span><span class="sxs-lookup"><span data-stu-id="22c84-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ parênteses ausentes**</span><span class="sxs-lookup"><span data-stu-id="22c84-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-721">14044 (0x36DC)</span><span class="sxs-lookup"><span data-stu-id="22c84-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-722">Erro de análise do manifesto: parêntese ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERRO de \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**</span><span class="sxs-lookup"><span data-stu-id="22c84-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-724">14045 (0x36DD)</span><span class="sxs-lookup"><span data-stu-id="22c84-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-725">Erro de análise do manifesto: um caractere de aspas simples ou duplas ( \\ ' ou \\ ") está ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERRO de \_ SxS \_ XML \_ E \_ vários \_ dois-pontos**</span><span class="sxs-lookup"><span data-stu-id="22c84-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-727">14046 (0x36DE)</span><span class="sxs-lookup"><span data-stu-id="22c84-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-728">Erro de análise do manifesto: não são permitidos vários dois-pontos em um nome.</span><span class="sxs-lookup"><span data-stu-id="22c84-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ decimal inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-730">14047 (0x36DF)</span><span class="sxs-lookup"><span data-stu-id="22c84-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-731">Erro de análise do manifesto: caractere inválido para dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="22c84-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ hexadecimal inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-733">14048 (0x36E0)</span><span class="sxs-lookup"><span data-stu-id="22c84-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-734">Erro de análise do manifesto: caractere inválido para dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="22c84-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ Unicode inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-736">14049 (0x36E1)</span><span class="sxs-lookup"><span data-stu-id="22c84-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-737">Erro de análise do manifesto: valor de caractere Unicode inválido para esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="22c84-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERRO de \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="22c84-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-739">14050 (0x36E2)</span><span class="sxs-lookup"><span data-stu-id="22c84-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-740">Erro de análise do manifesto: esperando espaço em branco ou '? '.</span><span class="sxs-lookup"><span data-stu-id="22c84-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="22c84-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-742">14051 (0x36E3)</span><span class="sxs-lookup"><span data-stu-id="22c84-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-743">Erro de análise do manifesto: a marca de fim não era esperada neste local.</span><span class="sxs-lookup"><span data-stu-id="22c84-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**</span><span class="sxs-lookup"><span data-stu-id="22c84-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-745">14052 (0x36E4)</span><span class="sxs-lookup"><span data-stu-id="22c84-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-746">Erro de análise do manifesto: as seguintes marcas não foram fechadas: %1.</span><span class="sxs-lookup"><span data-stu-id="22c84-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERRO de \_ SxS \_ XML \_ E \_ duplicataattribute**</span><span class="sxs-lookup"><span data-stu-id="22c84-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-748">14053 (0x36E5)</span><span class="sxs-lookup"><span data-stu-id="22c84-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-749">Erro de análise do manifesto: atributo duplicado.</span><span class="sxs-lookup"><span data-stu-id="22c84-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERRO de \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**</span><span class="sxs-lookup"><span data-stu-id="22c84-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-751">14054 (0x36E6)</span><span class="sxs-lookup"><span data-stu-id="22c84-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-752">Erro de análise do manifesto: apenas um elemento de nível superior é permitido em um documento XML.</span><span class="sxs-lookup"><span data-stu-id="22c84-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERRO de \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**</span><span class="sxs-lookup"><span data-stu-id="22c84-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-754">14055 (0x36E7)</span><span class="sxs-lookup"><span data-stu-id="22c84-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-755">Erro de análise do manifesto: inválido no nível superior do documento.</span><span class="sxs-lookup"><span data-stu-id="22c84-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADXMLDECL**</span><span class="sxs-lookup"><span data-stu-id="22c84-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-757">14056 (0x36E8)</span><span class="sxs-lookup"><span data-stu-id="22c84-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-758">Erro de análise do manifesto: declaração XML inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGROOT**</span><span class="sxs-lookup"><span data-stu-id="22c84-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-760">14057 (0x36E9)</span><span class="sxs-lookup"><span data-stu-id="22c84-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-761">Erro de análise do manifesto: o documento XML deve ter um elemento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="22c84-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**</span><span class="sxs-lookup"><span data-stu-id="22c84-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-763">14058 (0x36EA)</span><span class="sxs-lookup"><span data-stu-id="22c84-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-764">Erro de análise do manifesto: fim de arquivo inesperado.</span><span class="sxs-lookup"><span data-stu-id="22c84-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**</span><span class="sxs-lookup"><span data-stu-id="22c84-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-766">14059 (0x36EB)</span><span class="sxs-lookup"><span data-stu-id="22c84-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-767">Erro de análise do manifesto: entidades de parâmetro não podem ser usadas dentro de declarações de marcação em um subconjunto interno.</span><span class="sxs-lookup"><span data-stu-id="22c84-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**</span><span class="sxs-lookup"><span data-stu-id="22c84-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-769">14060 (0x36EC)</span><span class="sxs-lookup"><span data-stu-id="22c84-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-770">Erro de análise do manifesto: o elemento não foi fechado.</span><span class="sxs-lookup"><span data-stu-id="22c84-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="22c84-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-772">14061 (0x36ED)</span><span class="sxs-lookup"><span data-stu-id="22c84-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-773">Erro de análise do manifesto: o elemento final estava faltando o caractere ' > '.</span><span class="sxs-lookup"><span data-stu-id="22c84-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERRO \_ de \_ XML SxS \_ E não \_ closedstring**</span><span class="sxs-lookup"><span data-stu-id="22c84-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-775">14062 (0x36EE)</span><span class="sxs-lookup"><span data-stu-id="22c84-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-776">Erro de análise do manifesto: um literal de cadeia de caracteres não foi fechado.</span><span class="sxs-lookup"><span data-stu-id="22c84-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**</span><span class="sxs-lookup"><span data-stu-id="22c84-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-778">14063 (0x36EF)</span><span class="sxs-lookup"><span data-stu-id="22c84-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-779">Erro de análise do manifesto: um comentário não foi fechado.</span><span class="sxs-lookup"><span data-stu-id="22c84-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**</span><span class="sxs-lookup"><span data-stu-id="22c84-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-781">14064 (0x36F0)</span><span class="sxs-lookup"><span data-stu-id="22c84-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-782">Erro de análise do manifesto: uma declaração não foi fechada.</span><span class="sxs-lookup"><span data-stu-id="22c84-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**</span><span class="sxs-lookup"><span data-stu-id="22c84-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-784">14065 (0x36F1)</span><span class="sxs-lookup"><span data-stu-id="22c84-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-785">Erro de análise do manifesto: uma seção CDATA não foi fechada.</span><span class="sxs-lookup"><span data-stu-id="22c84-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERRO de \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**</span><span class="sxs-lookup"><span data-stu-id="22c84-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-787">14066 (0x36F2)</span><span class="sxs-lookup"><span data-stu-id="22c84-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-788">Erro de análise do manifesto: o prefixo do namespace não tem permissão para iniciar com a cadeia de caracteres reservada "XML".</span><span class="sxs-lookup"><span data-stu-id="22c84-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERRO de \_ SxS \_ XML \_ E \_ INVALIDENCODING**</span><span class="sxs-lookup"><span data-stu-id="22c84-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-790">14067 (0x36F3)</span><span class="sxs-lookup"><span data-stu-id="22c84-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-791">Erro de análise do manifesto: o sistema não oferece suporte à codificação especificada.</span><span class="sxs-lookup"><span data-stu-id="22c84-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERRO de \_ SxS \_ XML \_ E \_ INVALIDSWITCH**</span><span class="sxs-lookup"><span data-stu-id="22c84-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-793">14068 (0x36F4)</span><span class="sxs-lookup"><span data-stu-id="22c84-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-794">Erro de análise do manifesto: não há suporte para alternar da codificação atual para a codificação especificada.</span><span class="sxs-lookup"><span data-stu-id="22c84-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADXMLCASE**</span><span class="sxs-lookup"><span data-stu-id="22c84-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-796">14069 (0x36F5)</span><span class="sxs-lookup"><span data-stu-id="22c84-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-797">Erro de análise do manifesto: o nome ' XML ' está reservado e deve estar em letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22c84-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ autônomos inválidos**</span><span class="sxs-lookup"><span data-stu-id="22c84-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-799">14070 (0x36F6)</span><span class="sxs-lookup"><span data-stu-id="22c84-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-800">Erro de análise do manifesto: o atributo autônomo deve ter o valor ' Yes ' ou ' no '.</span><span class="sxs-lookup"><span data-stu-id="22c84-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ autônomo inesperado**</span><span class="sxs-lookup"><span data-stu-id="22c84-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-802">14071 (0x36F7)</span><span class="sxs-lookup"><span data-stu-id="22c84-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-803">Erro de análise do manifesto: o atributo autônomo não pode ser usado em entidades externas.</span><span class="sxs-lookup"><span data-stu-id="22c84-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ versão inválida**</span><span class="sxs-lookup"><span data-stu-id="22c84-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-805">14072 (0x36F8)</span><span class="sxs-lookup"><span data-stu-id="22c84-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-806">Erro de análise do manifesto: número de versão inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGEQUALS**</span><span class="sxs-lookup"><span data-stu-id="22c84-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-808">14073 (0x36F9)</span><span class="sxs-lookup"><span data-stu-id="22c84-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-809">Erro de análise do manifesto: sinal de igual ausente entre atributo e valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="22c84-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERRO \_ \_ ao recuperar proteção de SxS \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="22c84-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-811">14074 (0x36FA)</span><span class="sxs-lookup"><span data-stu-id="22c84-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-812">Erro de proteção de assembly: não é possível recuperar o assembly especificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERRO \_ \_ chave pública de proteção SxS \_ \_ \_ muito \_ curta**</span><span class="sxs-lookup"><span data-stu-id="22c84-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-814">14075 (0x36FB)</span><span class="sxs-lookup"><span data-stu-id="22c84-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-815">Erro de proteção de assembly: a chave pública de um assembly era muito curta para ser permitida.</span><span class="sxs-lookup"><span data-stu-id="22c84-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERRO \_ o \_ Catálogo de proteção SxS \_ não é \_ \_ válido**</span><span class="sxs-lookup"><span data-stu-id="22c84-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-817">14076 (0x36FC)</span><span class="sxs-lookup"><span data-stu-id="22c84-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-818">Erro de proteção de assembly: o catálogo de um assembly não é válido ou não corresponde ao manifesto do assembly.</span><span class="sxs-lookup"><span data-stu-id="22c84-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERRO \_ SxS não \_ traduzível \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="22c84-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-820">14077 (0x36FD)</span><span class="sxs-lookup"><span data-stu-id="22c84-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-821">Não foi possível converter um HRESULT em um código de erro Win32 correspondente.</span><span class="sxs-lookup"><span data-stu-id="22c84-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERRO \_ de \_ arquivo de catálogo de proteção SxS \_ \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="22c84-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-823">14078 (0x36FE)</span><span class="sxs-lookup"><span data-stu-id="22c84-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-824">Erro de proteção de assembly: o catálogo de um assembly está ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERRO \_ SxS \_ faltando \_ \_ atributo de identidade de assembly \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-826">14079 (0x36FF)</span><span class="sxs-lookup"><span data-stu-id="22c84-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-827">A identidade do assembly fornecida não tem um ou mais atributos que devem estar presentes neste contexto.</span><span class="sxs-lookup"><span data-stu-id="22c84-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERRO \_ SxS \_ \_ nome do \_ atributo de identidade de assembly inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-829">14080 (0x3700)</span><span class="sxs-lookup"><span data-stu-id="22c84-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-830">A identidade do assembly fornecida tem um ou mais nomes de atributo que contêm caracteres não permitidos em nomes XML.</span><span class="sxs-lookup"><span data-stu-id="22c84-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERRO \_ de \_ assembly SxS \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="22c84-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-832">14081 (0x3701)</span><span class="sxs-lookup"><span data-stu-id="22c84-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-833">Não foi possível encontrar o assembly referenciado.</span><span class="sxs-lookup"><span data-stu-id="22c84-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERRO \_ de \_ \_ pilha de ativação corrompida SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-835">14082 (0x3702)</span><span class="sxs-lookup"><span data-stu-id="22c84-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-836">A pilha de ativação do contexto de ativação para o thread em execução de execução está corrompida.</span><span class="sxs-lookup"><span data-stu-id="22c84-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERRO \_ de \_ corrupção de SXS**</span><span class="sxs-lookup"><span data-stu-id="22c84-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-838">14083 (0x3703)</span><span class="sxs-lookup"><span data-stu-id="22c84-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-839">Os metadados de isolamento de aplicativo para este processo ou thread foram corrompidos.</span><span class="sxs-lookup"><span data-stu-id="22c84-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERRO \_ de \_ desativação do SxS no início \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-841">14084 (0x3704)</span><span class="sxs-lookup"><span data-stu-id="22c84-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-842">O contexto de ativação que está sendo desativado não é o que foi ativado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="22c84-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERRO \_ de \_ \_ desativação de SxS inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-844">14085 (0x3705)</span><span class="sxs-lookup"><span data-stu-id="22c84-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-845">O contexto de ativação que está sendo desativado não está ativo para o thread atual de execução.</span><span class="sxs-lookup"><span data-stu-id="22c84-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERRO \_ de \_ várias \_ desativação SxS**</span><span class="sxs-lookup"><span data-stu-id="22c84-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-847">14086 (0x3706)</span><span class="sxs-lookup"><span data-stu-id="22c84-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-848">O contexto de ativação que está sendo desativado já foi desativado.</span><span class="sxs-lookup"><span data-stu-id="22c84-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERRO \_ de \_ término do processo SxS \_ \_ solicitado**</span><span class="sxs-lookup"><span data-stu-id="22c84-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-850">14087 (0x3707)</span><span class="sxs-lookup"><span data-stu-id="22c84-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-851">Um componente usado pelo recurso de isolamento solicitou o encerramento do processo.</span><span class="sxs-lookup"><span data-stu-id="22c84-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERRO \_ \_ contexto de \_ ativação da versão SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-853">14088 (0x3708)</span><span class="sxs-lookup"><span data-stu-id="22c84-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-854">Um componente de modo kernel está liberando uma referência em um contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="22c84-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERRO \_ de \_ \_ contexto de ativação padrão do sistema SxS \_ \_ \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="22c84-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-856">14089 (0x3709)</span><span class="sxs-lookup"><span data-stu-id="22c84-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-857">Não foi possível gerar o contexto de ativação do assembly padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="22c84-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERRO \_ o \_ \_ valor do atributo de identidade inválido \_ SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-859">14090 (0x370A)</span><span class="sxs-lookup"><span data-stu-id="22c84-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-860">O valor de um atributo em uma identidade não está dentro do intervalo válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERRO \_ \_ nome do \_ atributo de identidade inválido \_ SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-862">14091 (0x370B)</span><span class="sxs-lookup"><span data-stu-id="22c84-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-863">O nome de um atributo em uma identidade não está dentro do intervalo válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERRO \_ de \_ \_ atributo duplicado de identidade SxS \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-865">14092 (0x370C)</span><span class="sxs-lookup"><span data-stu-id="22c84-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-866">Uma identidade contém duas definições para o mesmo atributo.</span><span class="sxs-lookup"><span data-stu-id="22c84-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERRO \_ de \_ análise de identidade SxS do \_ \_ erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-868">14093 (0x370D)</span><span class="sxs-lookup"><span data-stu-id="22c84-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-869">A cadeia de caracteres de identidade está malformada.</span><span class="sxs-lookup"><span data-stu-id="22c84-869">The identity string is malformed.</span></span> <span data-ttu-id="22c84-870">Isso pode ser devido a uma vírgula à direita, mais de dois atributos não nomeados, nome de atributo ausente ou valor de atributo ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERRO \_ de \_ cadeia de substituição malformado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-872">14094 (0x370E)</span><span class="sxs-lookup"><span data-stu-id="22c84-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-873">Uma cadeia de caracteres que contém conteúdo substituível localizado foi malformada.</span><span class="sxs-lookup"><span data-stu-id="22c84-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="22c84-874">Um cifrão ($) foi seguido por algo diferente de um parêntese esquerdo ou outro sinal de dólar ou o parêntese direito de substituição não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERRO \_ de \_ \_ token de \_ chave \_ pública incorreto de SXS**</span><span class="sxs-lookup"><span data-stu-id="22c84-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-876">14095 (0x370F)</span><span class="sxs-lookup"><span data-stu-id="22c84-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-877">O token de chave pública não corresponde à chave pública especificada.</span><span class="sxs-lookup"><span data-stu-id="22c84-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERRO ao \_ Mapear \_ cadeia de caracteres de substituição \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-879">14096 (0x3710)</span><span class="sxs-lookup"><span data-stu-id="22c84-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-880">Uma cadeia de caracteres de substituição não tinha mapeamento.</span><span class="sxs-lookup"><span data-stu-id="22c84-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERRO \_ \_ assembly SxS \_ não \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="22c84-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-882">14097 (0x3711)</span><span class="sxs-lookup"><span data-stu-id="22c84-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-883">O componente deve ser bloqueado antes de fazer a solicitação.</span><span class="sxs-lookup"><span data-stu-id="22c84-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERRO \_ de \_ repositório de componentes SxS \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="22c84-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-885">14098 (0x3712)</span><span class="sxs-lookup"><span data-stu-id="22c84-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-886">O repositório de componentes foi corrompido.</span><span class="sxs-lookup"><span data-stu-id="22c84-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERRO \_ \_ no instalador \_ avançado**</span><span class="sxs-lookup"><span data-stu-id="22c84-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-888">14099 (0x3713)</span><span class="sxs-lookup"><span data-stu-id="22c84-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-889">Um instalador avançado falhou durante a instalação ou manutenção.</span><span class="sxs-lookup"><span data-stu-id="22c84-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**incompatibilidade de \_ codificação XML de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-891">14100 (0x3714)</span><span class="sxs-lookup"><span data-stu-id="22c84-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-892">A codificação de caracteres na declaração XML não correspondeu à codificação usada no documento.</span><span class="sxs-lookup"><span data-stu-id="22c84-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERRO \_ de \_ identidade de manifesto SxS \_ \_ igual \_ , mas \_ conteúdo \_ diferente**</span><span class="sxs-lookup"><span data-stu-id="22c84-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-894">14101 (0x3715)</span><span class="sxs-lookup"><span data-stu-id="22c84-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-895">As identidades dos manifestos são idênticas, mas seu conteúdo é diferente.</span><span class="sxs-lookup"><span data-stu-id="22c84-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERRO \_ de \_ identidades SxS \_ diferentes**</span><span class="sxs-lookup"><span data-stu-id="22c84-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-897">14102 (0x3716)</span><span class="sxs-lookup"><span data-stu-id="22c84-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-898">As identidades dos componentes são diferentes.</span><span class="sxs-lookup"><span data-stu-id="22c84-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERRO \_ \_ o assembly \_ SxS \_ não é \_ uma \_ implantação**</span><span class="sxs-lookup"><span data-stu-id="22c84-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-900">14103 (0x3717)</span><span class="sxs-lookup"><span data-stu-id="22c84-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-901">O assembly não é uma implantação.</span><span class="sxs-lookup"><span data-stu-id="22c84-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERRO \_ o \_ arquivo SxS \_ não \_ faz parte \_ do \_ assembly**</span><span class="sxs-lookup"><span data-stu-id="22c84-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-903">14104 (0x3718)</span><span class="sxs-lookup"><span data-stu-id="22c84-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-904">O arquivo não faz parte do assembly.</span><span class="sxs-lookup"><span data-stu-id="22c84-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERRO \_ de \_ manifesto SxS \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="22c84-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-906">14105 (0x3719)</span><span class="sxs-lookup"><span data-stu-id="22c84-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-907">O tamanho do manifesto excede o máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="22c84-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERRO \_ de \_ configuração de SxS \_ não \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-909">14106 (0x371A)</span><span class="sxs-lookup"><span data-stu-id="22c84-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-910">A configuração não está registrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERRO \_ de \_ fechamento de transação SxS \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="22c84-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-912">14107 (0x371B)</span><span class="sxs-lookup"><span data-stu-id="22c84-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-913">Um ou mais membros necessários da transação não estão presentes.</span><span class="sxs-lookup"><span data-stu-id="22c84-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERRO \_ \_ \_ falha no instalador primitivo SMI \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-915">14108 (0x371C)</span><span class="sxs-lookup"><span data-stu-id="22c84-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-916">O instalador do SMI Primitive falhou durante a instalação ou manutenção.</span><span class="sxs-lookup"><span data-stu-id="22c84-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERRO \_ \_ \_ falha no comando genérico**</span><span class="sxs-lookup"><span data-stu-id="22c84-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-918">14109 (0x371D)</span><span class="sxs-lookup"><span data-stu-id="22c84-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-919">Um executável de comando genérico retornou um resultado que indica falha.</span><span class="sxs-lookup"><span data-stu-id="22c84-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERRO \_ de \_ hash de arquivo SxS \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="22c84-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-921">14110 (0x371E)</span><span class="sxs-lookup"><span data-stu-id="22c84-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-922">Um componente não tem informações de verificação de arquivo em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="22c84-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRO \_ EVT \_ \_ caminho de canal inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-924">15000 (0x3A98)</span><span class="sxs-lookup"><span data-stu-id="22c84-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-925">O caminho de canal especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRO \_ EVT \_ de \_ consulta inválida**</span><span class="sxs-lookup"><span data-stu-id="22c84-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-927">15001 (0x3A99)</span><span class="sxs-lookup"><span data-stu-id="22c84-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-928">A consulta especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRO \_ EVT \_ metadados do Publicador \_ \_ não \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="22c84-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-930">15002 (0x3A9A)</span><span class="sxs-lookup"><span data-stu-id="22c84-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-931">Os metadados do Publicador não podem ser encontrados no recurso.</span><span class="sxs-lookup"><span data-stu-id="22c84-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRO \_ de \_ modelo de evento EVT \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-933">15003 (0x3A9B)</span><span class="sxs-lookup"><span data-stu-id="22c84-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-934">O modelo para uma definição de evento não pode ser encontrado no recurso (erro = %1).</span><span class="sxs-lookup"><span data-stu-id="22c84-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRO \_ EVT \_ \_ nome de editor inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-936">15004 (0x3A9C)</span><span class="sxs-lookup"><span data-stu-id="22c84-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-937">O nome de editor especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRO \_ EVT \_ \_ dados de eventos inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-939">15005 (0x3A9D)</span><span class="sxs-lookup"><span data-stu-id="22c84-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-940">Os dados de evento gerados pelo Publicador não são compatíveis com a definição do modelo de evento no manifesto do editor.</span><span class="sxs-lookup"><span data-stu-id="22c84-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRO \_ EVT \_ canal \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-942">15007 (0x3A9F)</span><span class="sxs-lookup"><span data-stu-id="22c84-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-943">O canal especificado não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-943">The specified channel could not be found.</span></span> <span data-ttu-id="22c84-944">Verifique a configuração do canal.</span><span class="sxs-lookup"><span data-stu-id="22c84-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRO \_ EVT \_ de \_ texto XML malformado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-946">15008 (0x3AA0)</span><span class="sxs-lookup"><span data-stu-id="22c84-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-947">O texto XML especificado não estava bem formado.</span><span class="sxs-lookup"><span data-stu-id="22c84-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="22c84-948">Consulte erro estendido para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="22c84-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ assinatura de erro \_ EVT \_ para \_ canal direto**</span><span class="sxs-lookup"><span data-stu-id="22c84-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-950">15009 (0x3AA1)</span><span class="sxs-lookup"><span data-stu-id="22c84-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-951">O chamador está tentando assinar um canal direto que não é permitido.</span><span class="sxs-lookup"><span data-stu-id="22c84-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="22c84-952">Os eventos de um canal direto vão diretamente para um arquivo de log e não podem ser assinados.</span><span class="sxs-lookup"><span data-stu-id="22c84-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**erro \_ de \_ configuração de EVT \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-954">15010 (0x3AA2)</span><span class="sxs-lookup"><span data-stu-id="22c84-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-955">Erro de configuração.</span><span class="sxs-lookup"><span data-stu-id="22c84-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRO \_ EVT \_ do \_ resultado da consulta \_ obsoleto**</span><span class="sxs-lookup"><span data-stu-id="22c84-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-957">15011 (0x3AA3)</span><span class="sxs-lookup"><span data-stu-id="22c84-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-958">O resultado da consulta é obsoleto/inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-958">The query result is stale / invalid.</span></span> <span data-ttu-id="22c84-959">Isso pode ser devido ao log ser limpo ou revertida depois que o resultado da consulta foi criado.</span><span class="sxs-lookup"><span data-stu-id="22c84-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="22c84-960">Os usuários devem lidar com esse código liberando o objeto de resultado da consulta e reemitindo a consulta.</span><span class="sxs-lookup"><span data-stu-id="22c84-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRO \_ EVT do \_ resultado da consulta \_ \_ posição inválida \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-962">15012 (0x3AA4)</span><span class="sxs-lookup"><span data-stu-id="22c84-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-963">O resultado da consulta está atualmente em uma posição inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRO \_ EVT \_ não \_ Validando o \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="22c84-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-965">15013 (0x3AA5)</span><span class="sxs-lookup"><span data-stu-id="22c84-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-966">O MSXML registrado não dá suporte à validação.</span><span class="sxs-lookup"><span data-stu-id="22c84-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRO \_ EVT \_ filtro \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="22c84-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-968">15014 (0x3AA6)</span><span class="sxs-lookup"><span data-stu-id="22c84-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-969">Uma expressão só pode ser seguida por uma alteração de operação de escopo se ela for avaliada como um conjunto de nós e ainda não fizer parte de alguma outra alteração de operação de escopo.</span><span class="sxs-lookup"><span data-stu-id="22c84-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRO \_ EVT \_ filtro \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="22c84-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-971">15015 (0x3AA7)</span><span class="sxs-lookup"><span data-stu-id="22c84-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-972">Não é possível executar uma operação de etapa a partir de um termo que não representa um conjunto de elementos.</span><span class="sxs-lookup"><span data-stu-id="22c84-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRO \_ EVT \_ filtro \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="22c84-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-974">15016 (0x3AA8)</span><span class="sxs-lookup"><span data-stu-id="22c84-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-975">Os argumentos do lado esquerdo para operadores binários devem ser atributos, nós ou variáveis e os argumentos do lado direito devem ser constantes.</span><span class="sxs-lookup"><span data-stu-id="22c84-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRO \_ EVT \_ filtro \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="22c84-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-977">15017 (0x3AA9)</span><span class="sxs-lookup"><span data-stu-id="22c84-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-978">Uma operação de etapa deve envolver um teste de nó ou, no caso de um predicado, uma expressão algébricas para testar cada nó no conjunto de nós identificado pelo conjunto de nós anterior pode ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="22c84-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRO \_ EVT \_ filtro \_ INVTYPE**</span><span class="sxs-lookup"><span data-stu-id="22c84-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-980">15018 (0x3AAA)</span><span class="sxs-lookup"><span data-stu-id="22c84-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-981">Não há suporte para este tipo de dados no momento.</span><span class="sxs-lookup"><span data-stu-id="22c84-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRO \_ EVT \_ filtro \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="22c84-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-983">15019 (0x3AAB)</span><span class="sxs-lookup"><span data-stu-id="22c84-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-984">Ocorreu um erro de sintaxe na posição %1! d!.</span><span class="sxs-lookup"><span data-stu-id="22c84-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRO \_ EVT \_ filtro \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="22c84-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-986">15020 (0x3AAC)</span><span class="sxs-lookup"><span data-stu-id="22c84-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-987">Este operador não tem suporte nesta implementação do filtro.</span><span class="sxs-lookup"><span data-stu-id="22c84-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRO \_ EVT \_ filtro \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="22c84-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-989">15021 (0x3AAD)</span><span class="sxs-lookup"><span data-stu-id="22c84-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-990">O token encontrado era inesperado.</span><span class="sxs-lookup"><span data-stu-id="22c84-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRO \_ EVT \_ de \_ operação inválida sobre o \_ \_ \_ canal direto habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-992">15022 (0x3AAE)</span><span class="sxs-lookup"><span data-stu-id="22c84-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-993">A operação solicitada não pode ser executada em um canal direto habilitado.</span><span class="sxs-lookup"><span data-stu-id="22c84-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="22c84-994">O canal deve primeiro ser desabilitado antes da execução da operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="22c84-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRO \_ EVT \_ \_ valor de propriedade de canal inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-996">15023 (0x3AAF)</span><span class="sxs-lookup"><span data-stu-id="22c84-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-997">Propriedade do canal %1! s!</span><span class="sxs-lookup"><span data-stu-id="22c84-997">Channel property %1!s!</span></span> <span data-ttu-id="22c84-998">contém valor inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-998">contains invalid value.</span></span> <span data-ttu-id="22c84-999">O valor tem tipo inválido, está fora do intervalo válido, não pode ser atualizado ou não é suportado por este tipo de canal.</span><span class="sxs-lookup"><span data-stu-id="22c84-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRO \_ EVT \_ \_ valor de \_ propriedade de Publicador inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1001">15024 (0x3AB0)</span><span class="sxs-lookup"><span data-stu-id="22c84-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1002">Propriedade do Publicador %1! s!</span><span class="sxs-lookup"><span data-stu-id="22c84-1002">Publisher property %1!s!</span></span> <span data-ttu-id="22c84-1003">contém valor inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1003">contains invalid value.</span></span> <span data-ttu-id="22c84-1004">O valor tem tipo inválido, está fora do intervalo válido, não pode ser atualizado ou não é suportado por este tipo de editor.</span><span class="sxs-lookup"><span data-stu-id="22c84-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRO \_ EVT de \_ canal \_ não pode \_ Ativar**</span><span class="sxs-lookup"><span data-stu-id="22c84-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1006">15025 (0x3AB1)</span><span class="sxs-lookup"><span data-stu-id="22c84-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1007">Falha na ativação do canal.</span><span class="sxs-lookup"><span data-stu-id="22c84-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**filtro de erro \_ EVT \_ \_ muito \_ complexo**</span><span class="sxs-lookup"><span data-stu-id="22c84-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1009">15026 (0x3AB2)</span><span class="sxs-lookup"><span data-stu-id="22c84-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1010">A expressão XPath excedeu a complexidade com suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="22c84-1011">Symplify-o ou divida-o em duas ou mais expressões simples.</span><span class="sxs-lookup"><span data-stu-id="22c84-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**mensagem de erro \_ EVT \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1013">15027 (0x3AB3)</span><span class="sxs-lookup"><span data-stu-id="22c84-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1014">o recurso de mensagem está presente, mas a mensagem não foi encontrada na tabela de cadeia de caracteres/mensagem.</span><span class="sxs-lookup"><span data-stu-id="22c84-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ID de mensagem de erro \_ EVT \_ \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1016">15028 (0x3AB4)</span><span class="sxs-lookup"><span data-stu-id="22c84-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1017">Não foi possível encontrar a ID da mensagem desejada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRO \_ EVT de \_ inserção de \_ valor não resolvido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1019">15029 (0x3AB5)</span><span class="sxs-lookup"><span data-stu-id="22c84-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1020">Não foi possível encontrar a cadeia de caracteres de substituição para o índice de inserção (%1).</span><span class="sxs-lookup"><span data-stu-id="22c84-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRO \_ EVT de \_ inserção de \_ parâmetro não resolvido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1022">15030 (0x3AB6)</span><span class="sxs-lookup"><span data-stu-id="22c84-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1023">Não foi possível encontrar a cadeia de caracteres de descrição para a referência de parâmetro (%1).</span><span class="sxs-lookup"><span data-stu-id="22c84-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRO \_ EVT \_ máximo de \_ inserções \_ atingido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1025">15031 (0x3AB7)</span><span class="sxs-lookup"><span data-stu-id="22c84-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1026">O número máximo de substituições foi atingido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_definição de evento EVT de erro \_ \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1028">15032 (0x3AB8)</span><span class="sxs-lookup"><span data-stu-id="22c84-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1029">Não foi possível encontrar a definição de evento para a ID de evento (%1).</span><span class="sxs-lookup"><span data-stu-id="22c84-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRO \_ EVT \_ localidade de mensagem \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="22c84-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1031">15033 (0x3AB9)</span><span class="sxs-lookup"><span data-stu-id="22c84-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1032">O recurso específico da localidade para a mensagem desejada não está presente.</span><span class="sxs-lookup"><span data-stu-id="22c84-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**versão de erro \_ EVT \_ \_ muito \_ antiga**</span><span class="sxs-lookup"><span data-stu-id="22c84-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1034">15034 (0x3ABA)</span><span class="sxs-lookup"><span data-stu-id="22c84-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1035">O recurso é muito antigo para ser compatível.</span><span class="sxs-lookup"><span data-stu-id="22c84-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**versão de erro \_ EVT \_ \_ muito \_ nova**</span><span class="sxs-lookup"><span data-stu-id="22c84-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1037">15035 (0x3ABB)</span><span class="sxs-lookup"><span data-stu-id="22c84-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1038">O recurso é muito novo para ser compatível.</span><span class="sxs-lookup"><span data-stu-id="22c84-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**o erro \_ EVT \_ não pode \_ abrir o \_ canal \_ de \_ consulta**</span><span class="sxs-lookup"><span data-stu-id="22c84-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1040">15036 (0x3ABC)</span><span class="sxs-lookup"><span data-stu-id="22c84-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1041">O canal no índice %1! d!</span><span class="sxs-lookup"><span data-stu-id="22c84-1041">The channel at index %1!d!</span></span> <span data-ttu-id="22c84-1042">Não é possível abrir a consulta.</span><span class="sxs-lookup"><span data-stu-id="22c84-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRO \_ EVT \_ Editor \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1044">15037 (0x3ABD)</span><span class="sxs-lookup"><span data-stu-id="22c84-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1045">O Publicador foi desabilitado e seu recurso não está disponível.</span><span class="sxs-lookup"><span data-stu-id="22c84-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="22c84-1046">Isso geralmente ocorre quando o Publicador está no processo de ser desinstalado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**\_ \_ filtro de erro EVT \_ fora \_ do \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="22c84-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1048">15038 (0x3ABE)</span><span class="sxs-lookup"><span data-stu-id="22c84-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1049">Tentativa de criar um tipo numérico que está fora de seu intervalo válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERRO \_ a \_ assinatura do EC \_ não pode \_ Ativar**</span><span class="sxs-lookup"><span data-stu-id="22c84-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1051">15080 (0x3AE8)</span><span class="sxs-lookup"><span data-stu-id="22c84-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1052">Falha na ativação da assinatura.</span><span class="sxs-lookup"><span data-stu-id="22c84-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERRO \_ de \_ log do EC \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1054">15081 (0x3AE9)</span><span class="sxs-lookup"><span data-stu-id="22c84-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1055">O log da assinatura está em estado desabilitado e não pode ser usado para encaminhar eventos para o.</span><span class="sxs-lookup"><span data-stu-id="22c84-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="22c84-1056">O log deve ser habilitado primeiro para que a assinatura possa ser ativada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERRO \_ de \_ encaminhamento circular do EC \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1058">15082 (0x3AEA)</span><span class="sxs-lookup"><span data-stu-id="22c84-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1059">Ao encaminhar eventos do computador local para ele mesmo, a consulta da assinatura não pode conter o log de destino da assinatura.</span><span class="sxs-lookup"><span data-stu-id="22c84-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERRO \_ EC \_ CREDSTORE \_ completo**</span><span class="sxs-lookup"><span data-stu-id="22c84-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1061">15083 (0x3AEB)</span><span class="sxs-lookup"><span data-stu-id="22c84-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1062">O repositório de credenciais usado para salvar as credenciais está cheio.</span><span class="sxs-lookup"><span data-stu-id="22c84-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERRO \_ de \_ credenciais do EC \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1064">15084 (0x3AEC)</span><span class="sxs-lookup"><span data-stu-id="22c84-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1065">A credencial usada por essa assinatura não pode ser encontrada no repositório de credenciais.</span><span class="sxs-lookup"><span data-stu-id="22c84-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERRO \_ EC \_ nenhum \_ \_ canal ativo**</span><span class="sxs-lookup"><span data-stu-id="22c84-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1067">15085 (0x3AED)</span><span class="sxs-lookup"><span data-stu-id="22c84-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1068">Nenhum canal ativo foi encontrado para a consulta.</span><span class="sxs-lookup"><span data-stu-id="22c84-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERRO \_ de \_ arquivo MUI \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1070">15100 (0x3AFC)</span><span class="sxs-lookup"><span data-stu-id="22c84-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1071">Falha do carregador de recursos ao localizar o arquivo MUI.</span><span class="sxs-lookup"><span data-stu-id="22c84-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERRO \_ de \_ arquivo inválido MUI \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1073">15101 (0x3AFD)</span><span class="sxs-lookup"><span data-stu-id="22c84-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1074">Falha do carregador de recursos ao carregar o arquivo MUI porque o arquivo não pôde passar na validação.</span><span class="sxs-lookup"><span data-stu-id="22c84-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERRO \_ de \_ \_ configuração RC inválida do MUI \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1076">15102 (0x3AFE)</span><span class="sxs-lookup"><span data-stu-id="22c84-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1077">O manifesto RC está corrompido com dados de lixo ou de versão sem suporte ou com um item necessário ausente.</span><span class="sxs-lookup"><span data-stu-id="22c84-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERRO \_ \_ nome de \_ localidade \_ inválido do MUI**</span><span class="sxs-lookup"><span data-stu-id="22c84-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1079">15103 (0x3AFF)</span><span class="sxs-lookup"><span data-stu-id="22c84-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1080">O manifesto RC tem um nome de cultura inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERRO \_ \_ nome de \_ ULTIMATEFALLBACK \_ inválido do MUI**</span><span class="sxs-lookup"><span data-stu-id="22c84-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1082">15104 (0x3B00)</span><span class="sxs-lookup"><span data-stu-id="22c84-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1083">O manifesto RC tem um nome de ultimatefallback inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERRO \_ \_ arquivo MUI \_ não \_ carregado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1085">15105 (0x3B01)</span><span class="sxs-lookup"><span data-stu-id="22c84-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1086">O cache do carregador de recursos não tem a entrada MUI carregada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**\_parada de \_ usuário de enumeração de recurso de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1088">15106 (0x3B02)</span><span class="sxs-lookup"><span data-stu-id="22c84-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1089">Enumeração de recursos interrompida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="22c84-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERRO \_ MUI \_ INTLSETTINGS \_ UILANG \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1091">15107 (0x3B03)</span><span class="sxs-lookup"><span data-stu-id="22c84-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1092">Falha na instalação do idioma da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="22c84-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERRO \_ MUI \_ INTLSETTINGS \_ \_ nome de localidade inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1094">15108 (0x3B04)</span><span class="sxs-lookup"><span data-stu-id="22c84-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1095">Falha na instalação da localidade.</span><span class="sxs-lookup"><span data-stu-id="22c84-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERRO \_ MRM \_ tempo \_ de execução sem \_ \_ recurso padrão ou \_ neutro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1097">15110 (0x3B06)</span><span class="sxs-lookup"><span data-stu-id="22c84-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1098">Um recurso não tem valor padrão ou neutro.</span><span class="sxs-lookup"><span data-stu-id="22c84-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERRO \_ MRM \_ \_ PRICONFIG inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1100">15111 (0x3B07)</span><span class="sxs-lookup"><span data-stu-id="22c84-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1101">Arquivo de configuração PRI inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERRO \_ MRM \_ \_ tipo de arquivo inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1103">15112 (0x3B08)</span><span class="sxs-lookup"><span data-stu-id="22c84-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1104">Tipo de arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERRO \_ MRM \_ \_ qualificador desconhecido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1106">15113 (0x3B09)</span><span class="sxs-lookup"><span data-stu-id="22c84-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1107">Qualificador desconhecido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERRO \_ MRM \_ \_ valor de qualificador inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1109">15114 (0x3B0A)</span><span class="sxs-lookup"><span data-stu-id="22c84-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1110">Valor de qualificador inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERRO \_ MRM \_ nenhum \_ candidato**</span><span class="sxs-lookup"><span data-stu-id="22c84-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1112">15115 (0x3B0B)</span><span class="sxs-lookup"><span data-stu-id="22c84-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1113">Nenhum candidato encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERRO \_ MRM \_ sem \_ correspondência \_ ou \_ \_ candidato padrão**</span><span class="sxs-lookup"><span data-stu-id="22c84-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1115">15116 (0x3B0C)</span><span class="sxs-lookup"><span data-stu-id="22c84-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1116">ResourceMap ou NamedResource tem um item que não tem recurso padrão ou neutro..</span><span class="sxs-lookup"><span data-stu-id="22c84-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de tipo de recurso MRM \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1118">15117 (0x3B0D)</span><span class="sxs-lookup"><span data-stu-id="22c84-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1119">Tipo de ResourceCandidate inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERRO \_ MRM \_ \_ nome do mapa duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1121">15118 (0x3B0E)</span><span class="sxs-lookup"><span data-stu-id="22c84-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1122">Mapa de recursos duplicado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERRO \_ MRM \_ entrada duplicada \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1124">15119 (0x3B0F)</span><span class="sxs-lookup"><span data-stu-id="22c84-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1125">Entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERRO \_ MRM \_ \_ identificador de recurso inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1127">15120 (0x3B10)</span><span class="sxs-lookup"><span data-stu-id="22c84-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1128">Identificador de recurso inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERRO \_ MRM \_ FilePath \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="22c84-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1130">15121 (0x3B11)</span><span class="sxs-lookup"><span data-stu-id="22c84-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1131">FilePath muito longo.</span><span class="sxs-lookup"><span data-stu-id="22c84-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERRO \_ MRM \_ tipo de diretório sem suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1133">15122 (0x3B12)</span><span class="sxs-lookup"><span data-stu-id="22c84-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1134">Tipo de diretório sem suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERRO \_ MRM \_ \_ arquivo pri \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1136">15126 (0x3B16)</span><span class="sxs-lookup"><span data-stu-id="22c84-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1137">Arquivo PRI inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERRO \_ MRM com o \_ \_ recurso nomeado \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1139">15127 (0x3B17)</span><span class="sxs-lookup"><span data-stu-id="22c84-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1140">NamedResource não encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**mapa de MRM de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1142">15135 (0x3B1F)</span><span class="sxs-lookup"><span data-stu-id="22c84-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1143">ResourceMap não encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERRO \_ MRM \_ tipo de perfil sem suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1145">15136 (0x3B20)</span><span class="sxs-lookup"><span data-stu-id="22c84-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1146">Tipo de perfil MRT sem suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERRO \_ MRM \_ \_ operador qualificador inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1148">15137 (0x3B21)</span><span class="sxs-lookup"><span data-stu-id="22c84-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1149">Operador qualificador inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERRO \_ MRM \_ \_ valor de qualificador indeterminado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1151">15138 (0x3B22)</span><span class="sxs-lookup"><span data-stu-id="22c84-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1152">Não é possível determinar se o valor do qualificador ou o valor do qualificador não foi definido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERRO \_ MRM \_ mesclagem automática \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="22c84-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1154">15139 (0x3B23)</span><span class="sxs-lookup"><span data-stu-id="22c84-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1155">A mesclagem automática está habilitada no arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="22c84-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERRO \_ MRM \_ \_ muitos \_ recursos**</span><span class="sxs-lookup"><span data-stu-id="22c84-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1157">15140 (0x3B24)</span><span class="sxs-lookup"><span data-stu-id="22c84-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1158">Muitos recursos definidos para o pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERRO \_ de \_ cadeia de \_ caracteres de funcionalidades inválidas MCA \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1160">15200 (0x3B60)</span><span class="sxs-lookup"><span data-stu-id="22c84-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1161">O monitor retornou uma cadeia de recursos DDC/CI que não estava em conformidade com a especificação ACCESS. Bus 3,0, DDC/CI 1,1 ou MCCS 2 revisão 1.</span><span class="sxs-lookup"><span data-stu-id="22c84-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERRO \_ MCA \_ \_ versão de VCP inválida \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1163">15201 (0x3B61)</span><span class="sxs-lookup"><span data-stu-id="22c84-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1164">O código VCP da versão VCP do monitor (0xDF) retornou um valor de versão inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERRO \_ o \_ Monitor MCA \_ viola \_ a \_ especificação MCCS**</span><span class="sxs-lookup"><span data-stu-id="22c84-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1166">15202 (0x3B62)</span><span class="sxs-lookup"><span data-stu-id="22c84-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1167">O monitor não está em conformidade com a especificação MCCS para a qual ele alega dar suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de versão MCA MCCs \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1169">15203 (0x3B63)</span><span class="sxs-lookup"><span data-stu-id="22c84-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1170">A versão MCCS no recurso MCCs ver de um monitor \_ não corresponde à versão MCCS que o monitor relata quando o código VCP de versão VCP (0xDF) é usado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERRO \_ de \_ versão do MCCs sem suporte para MCA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1172">15204 (0x3B64)</span><span class="sxs-lookup"><span data-stu-id="22c84-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1173">A API de configuração do monitor só funciona com monitores que dão suporte à especificação MCCS 1,0, MCCS 2,0 ou a especificação MCCS 2,0 revisão 1.</span><span class="sxs-lookup"><span data-stu-id="22c84-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**erro \_ interno de MCA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1175">15205 (0x3B65)</span><span class="sxs-lookup"><span data-stu-id="22c84-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1176">Ocorreu um erro interno de API de configuração de monitor.</span><span class="sxs-lookup"><span data-stu-id="22c84-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERRO \_ \_ tipo de \_ tecnologia inválido MCA \_ \_ retornado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1178">15206 (0x3B66)</span><span class="sxs-lookup"><span data-stu-id="22c84-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1179">O monitor retornou um tipo de tecnologia de monitor inválido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="22c84-1180">CRT, plasma e LCD (TFT) são exemplos de tipos de tecnologia de monitor.</span><span class="sxs-lookup"><span data-stu-id="22c84-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="22c84-1181">Esse erro indica que o monitor violou a especificação MCCS 2,0 ou MCCS 2,0 revisão 1.</span><span class="sxs-lookup"><span data-stu-id="22c84-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERRO \_ de \_ temperatura de cor sem suporte para MCA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1183">15207 (0x3B67)</span><span class="sxs-lookup"><span data-stu-id="22c84-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1184">O chamador de [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) especificou uma temperatura de cor para a qual o monitor atual não tinha suporte.</span><span class="sxs-lookup"><span data-stu-id="22c84-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="22c84-1185">Esse erro indica que o monitor violou a especificação MCCS 2,0 ou MCCS 2,0 revisão 1.</span><span class="sxs-lookup"><span data-stu-id="22c84-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERRO \_ de \_ dispositivo de sistema ambíguo \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1187">15250 (0x3B92)</span><span class="sxs-lookup"><span data-stu-id="22c84-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1188">O dispositivo de sistema solicitado não pode ser identificado porque vários dispositivos indistinguíveis potencialmente correspondem aos critérios de identificação.</span><span class="sxs-lookup"><span data-stu-id="22c84-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**dispositivo de sistema de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1190">15299 (0x3BC3)</span><span class="sxs-lookup"><span data-stu-id="22c84-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1191">Não é possível encontrar o dispositivo de sistema solicitado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**HASH de erro \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="22c84-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1193">15300 (0x3BC4)</span><span class="sxs-lookup"><span data-stu-id="22c84-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1194">A geração de hash para a versão de hash especificada e o tipo de hash não está habilitada no servidor.</span><span class="sxs-lookup"><span data-stu-id="22c84-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**o \_ hash de erro \_ não \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="22c84-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1196">15301 (0x3BC5)</span><span class="sxs-lookup"><span data-stu-id="22c84-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1197">O hash solicitado do servidor não está disponível ou não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERRO \_ de \_ provedor IC secundário \_ \_ não \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1199">15321 (0x3BD9)</span><span class="sxs-lookup"><span data-stu-id="22c84-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1200">A instância do controlador de interrupção secundário que gerencia a interrupção especificada não está registrada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERRO \_ de \_ informações do cliente GPIO \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1202">15322 (0x3BDA)</span><span class="sxs-lookup"><span data-stu-id="22c84-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1203">As informações fornecidas pelo driver do cliente GPIO são inválidas.</span><span class="sxs-lookup"><span data-stu-id="22c84-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**versão do GPIO de erro \_ \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="22c84-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1205">15323 (0x3BDB)</span><span class="sxs-lookup"><span data-stu-id="22c84-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1206">Não há suporte para a versão especificada pelo driver do cliente GPIO.</span><span class="sxs-lookup"><span data-stu-id="22c84-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERRO \_ GPIO \_ \_ pacote de registro inválido \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1208">15324 (0x3BDC)</span><span class="sxs-lookup"><span data-stu-id="22c84-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1209">O pacote de registro fornecido pelo driver do cliente GPIO não é válido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**operação de GPIO de erro \_ \_ \_ negada**</span><span class="sxs-lookup"><span data-stu-id="22c84-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1211">15325 (0x3BDD)</span><span class="sxs-lookup"><span data-stu-id="22c84-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1212">A operação solicitada não tem suporte para o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERRO \_ GPIO \_ modo de \_ conexão incompatível \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1214">15326 (0x3BDE)</span><span class="sxs-lookup"><span data-stu-id="22c84-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1215">O modo de conexão solicitado está em conflito com um modo existente em um ou mais dos Pins especificados.</span><span class="sxs-lookup"><span data-stu-id="22c84-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERRO \_ de \_ interrupção de GPIO já não \_ \_ mascarado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1217">15327 (0x3BDF)</span><span class="sxs-lookup"><span data-stu-id="22c84-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1218">A interrupção solicitada para não mascarada não é mascarada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERRO \_ não é possível \_ alternar \_ runlevel**</span><span class="sxs-lookup"><span data-stu-id="22c84-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1220">15400 (0x3C28)</span><span class="sxs-lookup"><span data-stu-id="22c84-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1221">A opção de nível de execução solicitada não pode ser concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="22c84-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERRO \_ de \_ configuração de runlevel inválida \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1223">15401 (0x3C29)</span><span class="sxs-lookup"><span data-stu-id="22c84-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1224">O serviço tem uma configuração de nível de execução inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="22c84-1225">O nível de execução para um serviço não deve ser maior que o nível de execução de seus serviços dependentes.</span><span class="sxs-lookup"><span data-stu-id="22c84-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERRO \_ runlevel \_ alternar \_ tempo limite**</span><span class="sxs-lookup"><span data-stu-id="22c84-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1227">15402 (0x3C2A)</span><span class="sxs-lookup"><span data-stu-id="22c84-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1228">A opção de nível de execução solicitada não pode ser concluída com êxito, pois um ou mais serviços não serão interrompidos ou reiniciados dentro do tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERRO \_ runlevel \_ \_ tempo limite do agente de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1230">15403 (0x3C2B)</span><span class="sxs-lookup"><span data-stu-id="22c84-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1231">Um agente de opção de nível de execução não respondeu dentro do tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERRO \_ runlevel \_ opção \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="22c84-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1233">15404 (0x3C2C)</span><span class="sxs-lookup"><span data-stu-id="22c84-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1234">Uma opção de nível de execução está em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="22c84-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_ \_ falha na \_ inicialização automática dos serviços de erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1236">15405 (0x3C2D)</span><span class="sxs-lookup"><span data-stu-id="22c84-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1237">Um ou mais serviços não foram iniciados durante a fase de inicialização do serviço de uma opção de nível de execução.</span><span class="sxs-lookup"><span data-stu-id="22c84-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERRO \_ de \_ parada de tarefa com \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="22c84-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1239">15501 (0x3C8D)</span><span class="sxs-lookup"><span data-stu-id="22c84-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1240">A solicitação de parada de tarefa não pode ser concluída imediatamente, pois a tarefa precisa de mais tempo para ser desligada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERRO \_ \_ ao instalar \_ pacote aberto \_ com falha**</span><span class="sxs-lookup"><span data-stu-id="22c84-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1242">15600 (0x3CF0)</span><span class="sxs-lookup"><span data-stu-id="22c84-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1243">Não foi possível abrir o pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERRO ao \_ instalar o \_ pacote \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="22c84-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1245">15601 (0x3CF1)</span><span class="sxs-lookup"><span data-stu-id="22c84-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1246">O pacote não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERRO \_ ao \_ instalar \_ pacote inválido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1248">15602 (0x3CF2)</span><span class="sxs-lookup"><span data-stu-id="22c84-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1249">Os dados do pacote são inválidos.</span><span class="sxs-lookup"><span data-stu-id="22c84-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERRO \_ ao instalar a \_ dependência de resolução \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1251">15603 (0x3CF3)</span><span class="sxs-lookup"><span data-stu-id="22c84-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1252">Atualizações com falha de pacote, dependência ou validação de conflito.</span><span class="sxs-lookup"><span data-stu-id="22c84-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERRO \_ \_ de instalação \_ sem \_ \_ espaço em disco**</span><span class="sxs-lookup"><span data-stu-id="22c84-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1254">15604 (0x3CF4)</span><span class="sxs-lookup"><span data-stu-id="22c84-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1255">Não há espaço em disco suficiente no computador.</span><span class="sxs-lookup"><span data-stu-id="22c84-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="22c84-1256">Libere espaço e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="22c84-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERRO \_ ao \_ instalar \_ falha de rede**</span><span class="sxs-lookup"><span data-stu-id="22c84-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1258">15605 (0x3CF5)</span><span class="sxs-lookup"><span data-stu-id="22c84-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1259">Houve um problema ao baixar seu produto.</span><span class="sxs-lookup"><span data-stu-id="22c84-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERRO \_ ao \_ instalar \_ falha de registro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1261">15606 (0x3CF6)</span><span class="sxs-lookup"><span data-stu-id="22c84-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1262">Não foi possível registrar o pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERRO ao \_ instalar falha de \_ cancelamento de registro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1264">15607 (0x3CF7)</span><span class="sxs-lookup"><span data-stu-id="22c84-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1265">Não foi possível cancelar o registro do pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERRO ao \_ instalar \_ cancelar**</span><span class="sxs-lookup"><span data-stu-id="22c84-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1267">15608 (0x3CF8)</span><span class="sxs-lookup"><span data-stu-id="22c84-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1268">O usuário cancelou a solicitação de instalação.</span><span class="sxs-lookup"><span data-stu-id="22c84-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**\_falha na instalação do erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1270">15609 (0x3CF9)</span><span class="sxs-lookup"><span data-stu-id="22c84-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1271">Falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="22c84-1271">Install failed.</span></span> <span data-ttu-id="22c84-1272">Entre em contato com seu fornecedor de software.</span><span class="sxs-lookup"><span data-stu-id="22c84-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**\_ \_ falha ao remover erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1274">15610 (0x3CFA)</span><span class="sxs-lookup"><span data-stu-id="22c84-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1275">Falha na remoção.</span><span class="sxs-lookup"><span data-stu-id="22c84-1275">Removal failed.</span></span> <span data-ttu-id="22c84-1276">Entre em contato com seu fornecedor de software.</span><span class="sxs-lookup"><span data-stu-id="22c84-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**o \_ pacote de erros \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="22c84-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1278">15611 (0x3CFB)</span><span class="sxs-lookup"><span data-stu-id="22c84-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1279">O pacote fornecido já está instalado e a reinstalação do pacote foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="22c84-1280">Verifique o log de eventos AppXDeployment-Server para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="22c84-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERRO \_ precisa de \_ correção**</span><span class="sxs-lookup"><span data-stu-id="22c84-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1282">15612 (0x3CFC)</span><span class="sxs-lookup"><span data-stu-id="22c84-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1283">O aplicativo não pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1283">The application cannot be started.</span></span> <span data-ttu-id="22c84-1284">Tente reinstalar o aplicativo para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="22c84-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERRO \_ ao instalar o \_ pré-requisito \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1286">15613 (0x3CFD)</span><span class="sxs-lookup"><span data-stu-id="22c84-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1287">Um pré-requisito para uma instalação não pôde ser atendido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**repositório de pacotes de erros \_ \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1289">15614 (0x3CFE)</span><span class="sxs-lookup"><span data-stu-id="22c84-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1290">O repositório do pacote está corrompido.</span><span class="sxs-lookup"><span data-stu-id="22c84-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERRO \_ de \_ falha na política de instalação \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1292">15615 (0x3CFF)</span><span class="sxs-lookup"><span data-stu-id="22c84-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1293">Para instalar este aplicativo, você precisa de uma licença de desenvolvedor do Windows ou de um sistema habilitado para Sideload.</span><span class="sxs-lookup"><span data-stu-id="22c84-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_atualização do pacote de erros \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1295">15616 (0x3D00)</span><span class="sxs-lookup"><span data-stu-id="22c84-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1296">O aplicativo não pode ser iniciado porque está sendo atualizado no momento.</span><span class="sxs-lookup"><span data-stu-id="22c84-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_implantação \_ de erro bloqueada \_ pela \_ política**</span><span class="sxs-lookup"><span data-stu-id="22c84-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1298">15617 (0x3D01)</span><span class="sxs-lookup"><span data-stu-id="22c84-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1299">A operação de implantação de pacote está bloqueada pela política.</span><span class="sxs-lookup"><span data-stu-id="22c84-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="22c84-1300">Entre em contato com o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="22c84-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_pacotes \_ de erro em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="22c84-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1302">15618 (0x3D02)</span><span class="sxs-lookup"><span data-stu-id="22c84-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1303">O pacote não pôde ser instalado porque os recursos que ele modifica estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="22c84-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERRO \_ de \_ arquivo de recuperação \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1305">15619 (0x3D03)</span><span class="sxs-lookup"><span data-stu-id="22c84-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1306">O pacote não pôde ser recuperado porque os dados necessários para recuperação foram corrompidos.</span><span class="sxs-lookup"><span data-stu-id="22c84-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERRO \_ de \_ assinatura preparada inválida \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1308">15620 (0x3D04)</span><span class="sxs-lookup"><span data-stu-id="22c84-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1309">A assinatura é inválida.</span><span class="sxs-lookup"><span data-stu-id="22c84-1309">The signature is invalid.</span></span> <span data-ttu-id="22c84-1310">Para se registrar no modo de desenvolvedor, AppxSignature. P7X e AppxBlockMap.xml devem ser válidos ou não devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="22c84-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERRO ao \_ excluir o \_ \_ repositório de APPLICATIONDATA existente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1312">15621 (0x3D05)</span><span class="sxs-lookup"><span data-stu-id="22c84-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1313">Ocorreu um erro ao excluir os dados de aplicativo anteriormente existentes do pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERRO ao \_ instalar o \_ downgrade do pacote \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1315">15622 (0x3D06)</span><span class="sxs-lookup"><span data-stu-id="22c84-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1316">Não foi possível instalar o pacote porque uma versão mais recente deste pacote já está instalada.</span><span class="sxs-lookup"><span data-stu-id="22c84-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**o \_ sistema de erros \_ precisa de \_ correção**</span><span class="sxs-lookup"><span data-stu-id="22c84-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1318">15623 (0x3D07)</span><span class="sxs-lookup"><span data-stu-id="22c84-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1319">Foi detectado um erro em um binário do sistema.</span><span class="sxs-lookup"><span data-stu-id="22c84-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="22c84-1320">Tente atualizar o PC para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="22c84-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERRO \_ de \_ integridade Appx \_ falha no \_ CLR \_ NGen**</span><span class="sxs-lookup"><span data-stu-id="22c84-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1322">15624 (0x3D08)</span><span class="sxs-lookup"><span data-stu-id="22c84-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1323">Foi detectado um binário do CLR NGEN corrompido no sistema.</span><span class="sxs-lookup"><span data-stu-id="22c84-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**arquivo de resiliência de erro \_ \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1325">15625 (0x3D09)</span><span class="sxs-lookup"><span data-stu-id="22c84-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1326">A operação não pôde ser retomada porque os dados necessários para recuperação foram corrompidos.</span><span class="sxs-lookup"><span data-stu-id="22c84-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERRO ao \_ instalar o \_ serviço de firewall \_ \_ não \_ está em execução**</span><span class="sxs-lookup"><span data-stu-id="22c84-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1328">15626 (0x3D0A)</span><span class="sxs-lookup"><span data-stu-id="22c84-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1329">Não foi possível instalar o pacote porque o serviço de firewall do Windows não está em execução.</span><span class="sxs-lookup"><span data-stu-id="22c84-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="22c84-1330">Habilite o serviço de firewall do Windows e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="22c84-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**erro de APPMODEL \_ \_ sem \_ pacote**</span><span class="sxs-lookup"><span data-stu-id="22c84-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1332">15700 (0x3D54)</span><span class="sxs-lookup"><span data-stu-id="22c84-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1333">O processo não tem nenhuma identidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="22c84-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**tempo de execução do pacote de erros do APPMODEL \_ \_ \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1335">15701 (0x3D55)</span><span class="sxs-lookup"><span data-stu-id="22c84-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1336">As informações de tempo de execução do pacote estão corrompidas.</span><span class="sxs-lookup"><span data-stu-id="22c84-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_ \_ \_ identidade \_ corrompida do pacote de erros do APPMODEL**</span><span class="sxs-lookup"><span data-stu-id="22c84-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1338">15702 (0x3D56)</span><span class="sxs-lookup"><span data-stu-id="22c84-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1339">A identidade do pacote está corrompida.</span><span class="sxs-lookup"><span data-stu-id="22c84-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**erro de APPMODEL \_ \_ sem \_ aplicativo**</span><span class="sxs-lookup"><span data-stu-id="22c84-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1341">15703 (0x3D57)</span><span class="sxs-lookup"><span data-stu-id="22c84-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1342">O processo não tem nenhuma identidade de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22c84-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**\_ \_ \_ falha no repositório de carregamento do estado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1344">15800 (0x3DB8)</span><span class="sxs-lookup"><span data-stu-id="22c84-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1345">Falha ao carregar o armazenamento de estado.</span><span class="sxs-lookup"><span data-stu-id="22c84-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**\_ \_ \_ falha ao obter versão do estado \_ de erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1347">15801 (0x3DB9)</span><span class="sxs-lookup"><span data-stu-id="22c84-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1348">Falha ao recuperar a versão de estado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22c84-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**\_ \_ \_ falha na versão do conjunto de estado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1350">15802 (0x3DBA)</span><span class="sxs-lookup"><span data-stu-id="22c84-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1351">Falha ao definir a versão de estado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22c84-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**\_ \_ \_ falha na redefinição estruturada do estado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1353">15803 (0x3DBB)</span><span class="sxs-lookup"><span data-stu-id="22c84-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1354">Falha na redefinição do estado estruturado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22c84-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**\_falha no estado do erro \_ abrir \_ contêiner \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1356">15804 (0x3DBC)</span><span class="sxs-lookup"><span data-stu-id="22c84-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1357">Falha do Gerenciador de estado ao abrir o contêiner.</span><span class="sxs-lookup"><span data-stu-id="22c84-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**\_ \_ \_ falha ao criar contêiner de estado \_ de erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1359">15805 (0x3DBD)</span><span class="sxs-lookup"><span data-stu-id="22c84-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1360">Falha do Gerenciador de estado ao criar o contêiner.</span><span class="sxs-lookup"><span data-stu-id="22c84-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**\_ \_ \_ falha ao excluir contêiner de estado \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1362">15806 (0x3DBE)</span><span class="sxs-lookup"><span data-stu-id="22c84-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1363">Falha do Gerenciador de estado ao excluir o contêiner.</span><span class="sxs-lookup"><span data-stu-id="22c84-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_ \_ \_ falha na configuração de leitura do estado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1365">15807 (0x3DBF)</span><span class="sxs-lookup"><span data-stu-id="22c84-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1366">Falha do Gerenciador de estado ao ler a configuração.</span><span class="sxs-lookup"><span data-stu-id="22c84-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_ \_ \_ falha na configuração de gravação do estado do erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1368">15808 (0x3DC0)</span><span class="sxs-lookup"><span data-stu-id="22c84-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1369">Falha do Gerenciador de estado ao gravar a configuração.</span><span class="sxs-lookup"><span data-stu-id="22c84-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_ \_ \_ falha na configuração de exclusão do estado do erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1371">15809 (0x3DC1)</span><span class="sxs-lookup"><span data-stu-id="22c84-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1372">Falha do Gerenciador de estado ao excluir a configuração.</span><span class="sxs-lookup"><span data-stu-id="22c84-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_ \_ \_ falha na configuração de consulta de estado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1374">15810 (0x3DC2)</span><span class="sxs-lookup"><span data-stu-id="22c84-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1375">Falha do Gerenciador de estado ao consultar a configuração.</span><span class="sxs-lookup"><span data-stu-id="22c84-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**\_ \_ \_ \_ falha na configuração de composição de leitura de estado \_ de erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1377">15811 (0x3DC3)</span><span class="sxs-lookup"><span data-stu-id="22c84-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1378">Falha do Gerenciador de estado ao ler a configuração composta.</span><span class="sxs-lookup"><span data-stu-id="22c84-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**\_ \_ \_ \_ falha na configuração de composição de gravação de estado \_ de erro**</span><span class="sxs-lookup"><span data-stu-id="22c84-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1380">15812 (0x3DC4)</span><span class="sxs-lookup"><span data-stu-id="22c84-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1381">Falha do Gerenciador de estado ao gravar a configuração composta.</span><span class="sxs-lookup"><span data-stu-id="22c84-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**\_ \_ \_ falha no contêiner enumerar o estado do erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1383">15813 (0x3DC5)</span><span class="sxs-lookup"><span data-stu-id="22c84-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1384">Falha do Gerenciador de estado ao enumerar os contêineres.</span><span class="sxs-lookup"><span data-stu-id="22c84-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**\_ \_ \_ falha nas configurações de enumeração de estado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="22c84-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1386">15814 (0x3DC6)</span><span class="sxs-lookup"><span data-stu-id="22c84-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1387">Falha do Gerenciador de estado ao enumerar as configurações.</span><span class="sxs-lookup"><span data-stu-id="22c84-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**Estado de erro \_ \_ \_ configuração composta limite de tamanho de \_ valor \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1389">15815 (0x3DC7)</span><span class="sxs-lookup"><span data-stu-id="22c84-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1390">O tamanho do valor da configuração composta do Gerenciador de estado excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="22c84-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**limite de tamanho de valor de configuração de estado de erro \_ \_ \_ \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1392">15816 (0x3DC8)</span><span class="sxs-lookup"><span data-stu-id="22c84-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1393">O tamanho do valor da configuração do Gerenciador de estado excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="22c84-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**limite de tamanho de nome de configuração de estado de erro \_ \_ \_ \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1395">15817 (0x3DC9)</span><span class="sxs-lookup"><span data-stu-id="22c84-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1396">O comprimento do nome da configuração do Gerenciador de estado excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="22c84-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**limite de tamanho do nome do contêiner de estado de erro \_ \_ \_ \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="22c84-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1398">15818 (0x3DCA)</span><span class="sxs-lookup"><span data-stu-id="22c84-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1399">O comprimento do nome do contêiner do Gerenciador de estado excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="22c84-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22c84-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**API de erro \_ \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="22c84-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c84-1401">15841 (0x3DE1)</span><span class="sxs-lookup"><span data-stu-id="22c84-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="22c84-1402">Essa API não pode ser usada no contexto do tipo de aplicativo do chamador.</span><span class="sxs-lookup"><span data-stu-id="22c84-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22c84-1403">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c84-1403">Requirements</span></span>



| <span data-ttu-id="22c84-1404">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c84-1404">Requirement</span></span> | <span data-ttu-id="22c84-1405">Valor</span><span class="sxs-lookup"><span data-stu-id="22c84-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22c84-1406">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22c84-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="22c84-1407">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="22c84-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="22c84-1408">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22c84-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="22c84-1409">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22c84-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22c84-1410">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22c84-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c84-1411"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="22c84-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c84-1412">Confira também</span><span class="sxs-lookup"><span data-stu-id="22c84-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c84-1413">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="22c84-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
