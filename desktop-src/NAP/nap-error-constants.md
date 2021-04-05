---
title: Constantes de erro NAP (WinError. h)
description: As constantes de erro NAP a seguir são definidas no WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918945"
---
# <a name="nap-error-constants"></a><span data-ttu-id="c1a15-103">Constantes de erro NAP</span><span class="sxs-lookup"><span data-stu-id="c1a15-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="c1a15-104">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="c1a15-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c1a15-105">As constantes de erro NAP a seguir são definidas no WinError. h.</span><span class="sxs-lookup"><span data-stu-id="c1a15-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="c1a15-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_pacote NAP E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="c1a15-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-107">\_\_TYPEDEF \_ de HRESULT (0x80270001L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-108">O pacote NAP [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) é inválido.</span><span class="sxs-lookup"><span data-stu-id="c1a15-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ faltando \_ soh**</span><span class="sxs-lookup"><span data-stu-id="c1a15-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-110">\_\_TYPEDEF \_ de HRESULT (0x80270002L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-111">Uma [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) estava ausente no pacote NAP.</span><span class="sxs-lookup"><span data-stu-id="c1a15-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP \_ E \_ ID conflitante \_**</span><span class="sxs-lookup"><span data-stu-id="c1a15-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-113">\_\_TYPEDEF \_ de HRESULT (0x80270003L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-114">A ID da entidade está em conflito com uma ID de entidade já registrada.</span><span class="sxs-lookup"><span data-stu-id="c1a15-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ nenhum \_ soh armazenado em cache \_**</span><span class="sxs-lookup"><span data-stu-id="c1a15-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-116">\_\_TYPEDEF \_ de HRESULT (0x80270004L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-117">Nenhum [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) armazenado em cache está presente.</span><span class="sxs-lookup"><span data-stu-id="c1a15-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ ainda \_ associado**</span><span class="sxs-lookup"><span data-stu-id="c1a15-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-119">\_\_TYPEDEF \_ de HRESULT (0x80270005L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-120">A entidade ainda está associada ao sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="c1a15-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**\_E/s NAP \_ não \_ registradas**</span><span class="sxs-lookup"><span data-stu-id="c1a15-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-122">\_\_TYPEDEF \_ de HRESULT (0x80270006L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-123">A entidade não está registrada com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="c1a15-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ não \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="c1a15-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-125">\_\_TYPEDEF \_ de HRESULT (0x80270007L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-126">A entidade não foi inicializada com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="c1a15-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**ID de NAP \_ E não \_ correspondente \_**</span><span class="sxs-lookup"><span data-stu-id="c1a15-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-128">\_\_TYPEDEF \_ de HRESULT (0x80270008L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-129">As IDs de correlação na solicitação [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) e na resposta **soh** não correspondem.</span><span class="sxs-lookup"><span data-stu-id="c1a15-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ não \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="c1a15-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-131">\_\_TYPEDEF \_ de HRESULT (0x80270009L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-132">A conclusão foi indicada em uma solicitação que não está pendente no momento.</span><span class="sxs-lookup"><span data-stu-id="c1a15-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ID NAP \_ E \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="c1a15-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-134">\_\_TYPEDEF \_ de HRESULT (0x8027000AL)</span><span class="sxs-lookup"><span data-stu-id="c1a15-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-135">A ID do componente NAP não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="c1a15-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ muito \_ pequeno**</span><span class="sxs-lookup"><span data-stu-id="c1a15-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-137">\_\_TYPEDEF \_ de HRESULT (0x8027000BL)</span><span class="sxs-lookup"><span data-stu-id="c1a15-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-138">O tamanho máximo da conexão é muito pequeno para um pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="c1a15-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**o \_ serviço NAP E \_ \_ não \_ está em execução**</span><span class="sxs-lookup"><span data-stu-id="c1a15-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-140">\_\_TYPEDEF \_ de HRESULT (0x8027000CL)</span><span class="sxs-lookup"><span data-stu-id="c1a15-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-141">O serviço NapAgent não está em execução.</span><span class="sxs-lookup"><span data-stu-id="c1a15-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**o \_ certificado NAP S \_ \_ já está \_ presente**</span><span class="sxs-lookup"><span data-stu-id="c1a15-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-143">\_\_TYPEDEF \_ de HRESULT (0x0027000DL)</span><span class="sxs-lookup"><span data-stu-id="c1a15-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="c1a15-144">Um certificado já está presente no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="c1a15-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_entidade E \_ NAP \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="c1a15-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-146">\_\_TYPEDEF \_ de HRESULT (0x8027000EL)</span><span class="sxs-lookup"><span data-stu-id="c1a15-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-147">A entidade está desabilitada com o serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="c1a15-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_erro de GROUPPOLICY NAP E \_ netsh \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1a15-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-149">\_\_TYPEDEF \_ de HRESULT (0x8027000FL)</span><span class="sxs-lookup"><span data-stu-id="c1a15-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-150">Política de Grupo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="c1a15-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ excesso \_ de \_ chamadas**</span><span class="sxs-lookup"><span data-stu-id="c1a15-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-152">\_\_TYPEDEF \_ de HRESULT (0x80270010L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-153">Muitas chamadas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c1a15-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**a \_ configuração de NAP E \_ SHV \_ \_ existia**</span><span class="sxs-lookup"><span data-stu-id="c1a15-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-155">\_\_TYPEDEF \_ de HRESULT (0x80270011L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-156">A configuração de SHV já existe.</span><span class="sxs-lookup"><span data-stu-id="c1a15-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="c1a15-157">Com suporte no Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c1a15-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="c1a15-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-159">\_\_TYPEDEF \_ de HRESULT (0x80270012L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-160">A configuração SHV não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="c1a15-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="c1a15-161">Com suporte no Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c1a15-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1a15-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**\_tempo limite de NAP E \_ SHV \_**</span><span class="sxs-lookup"><span data-stu-id="c1a15-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1a15-163">\_\_TYPEDEF \_ de HRESULT (0x80270013L)</span><span class="sxs-lookup"><span data-stu-id="c1a15-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="c1a15-164">O SHV atingiu o tempo limite na solicitação.</span><span class="sxs-lookup"><span data-stu-id="c1a15-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="c1a15-165">Com suporte no Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c1a15-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1a15-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1a15-166">Requirements</span></span>



| <span data-ttu-id="c1a15-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1a15-167">Requirement</span></span> | <span data-ttu-id="c1a15-168">Valor</span><span class="sxs-lookup"><span data-stu-id="c1a15-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a15-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1a15-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a15-170">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1a15-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1a15-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1a15-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a15-172">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1a15-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1a15-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1a15-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1a15-174"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a15-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a15-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1a15-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a15-176">**Constantes de NAP**</span><span class="sxs-lookup"><span data-stu-id="c1a15-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





