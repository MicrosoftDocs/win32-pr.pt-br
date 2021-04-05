---
title: Valores de retorno
description: As constantes abaixo representam valores de retorno que a otimização de entrega gera e valores de retorno HTTP que capturam.
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58d66587061cc44fc441249407b73653153322
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007907"
---
# <a name="do-return-values"></a><span data-ttu-id="b930f-103">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b930f-103">DO Return Values</span></span>

<span data-ttu-id="b930f-104">As constantes abaixo representam valores de retorno que a otimização de entrega gera e valores de retorno HTTP que capturam.</span><span class="sxs-lookup"><span data-stu-id="b930f-104">The below constants represent return values that Delivery Optimization (DO) generates and HTTP return values that DO captures.</span></span> <span data-ttu-id="b930f-105">Todos os outros valores de retorno que você pode receber são COM, RPC ou valores de retorno DO Windows convertidos (o usa a macro [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para converter os valores de retorno do Windows em valores de HRESULT).</span><span class="sxs-lookup"><span data-stu-id="b930f-105">All other return values that you can receive are COM, RPC, or converted Windows return values (DO uses the [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<dl> <dt>

<span data-ttu-id="b930f-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span><span class="sxs-lookup"><span data-stu-id="b930f-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-107">A otimização de entrega não pôde fornecer o serviço.</span><span class="sxs-lookup"><span data-stu-id="b930f-107">Delivery Optimization was unable to provide the service.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span><span class="sxs-lookup"><span data-stu-id="b930f-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-109">O download de um arquivo não viu nenhum progresso dentro do período definido.</span><span class="sxs-lookup"><span data-stu-id="b930f-109">Download of a file saw no progress within the defined period.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span><span class="sxs-lookup"><span data-stu-id="b930f-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-111">O trabalho não foi encontrado, esperando que um trabalho esteja presente.</span><span class="sxs-lookup"><span data-stu-id="b930f-111">Job was not found, expecting a job to be present.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span><span class="sxs-lookup"><span data-stu-id="b930f-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-113">Não havia nenhum arquivo no trabalho, esperando pelo menos um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b930f-113">There was no file in the job, expecting at least one file.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span><span class="sxs-lookup"><span data-stu-id="b930f-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-115">Não há nenhum caminho de arquivo local especificado para este download.</span><span class="sxs-lookup"><span data-stu-id="b930f-115">There is no local file path specified for this download.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span><span class="sxs-lookup"><span data-stu-id="b930f-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-117">Nenhum arquivo está disponível porque nenhuma URL gerou um erro.</span><span class="sxs-lookup"><span data-stu-id="b930f-117">No file is available because no URL generated an error.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span><span class="sxs-lookup"><span data-stu-id="b930f-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-119">SetProperty () ou GetProperty () chamado com uma ID de propriedade desconhecida.</span><span class="sxs-lookup"><span data-stu-id="b930f-119">SetProperty() or GetProperty() called with an unknown property ID.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span><span class="sxs-lookup"><span data-stu-id="b930f-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-121">Não é possível chamar SetProperty () em uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b930f-121">Unable to call SetProperty() on a read-only property.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span><span class="sxs-lookup"><span data-stu-id="b930f-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-123">A ação solicitada não é permitida no estado do trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="b930f-123">The requested action is not allowed in the current job state.</span></span> <span data-ttu-id="b930f-124">O trabalho pode ter sido cancelado ou concluído.</span><span class="sxs-lookup"><span data-stu-id="b930f-124">The job might have been canceled or completed transferring.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span><span class="sxs-lookup"><span data-stu-id="b930f-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-126">Não ocorreu nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="b930f-126">No errors have occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span><span class="sxs-lookup"><span data-stu-id="b930f-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-128">O trabalho de download não é permitido devido a configurações de usuário/administrador.</span><span class="sxs-lookup"><span data-stu-id="b930f-128">Download job not allowed due to user/admin settings.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span><span class="sxs-lookup"><span data-stu-id="b930f-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-130">O trabalho foi pausado devido a restrições de política de custo.</span><span class="sxs-lookup"><span data-stu-id="b930f-130">DO paused the job due to cost policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span><span class="sxs-lookup"><span data-stu-id="b930f-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-132">Pausou o trabalho devido à detecção de restrições de política e rede celular.</span><span class="sxs-lookup"><span data-stu-id="b930f-132">DO paused the job due to detection of cellular network and policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span><span class="sxs-lookup"><span data-stu-id="b930f-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-134">Pausou o trabalho devido à detecção da alteração do estado de energia no modo não AC.</span><span class="sxs-lookup"><span data-stu-id="b930f-134">DO paused the job due to detection of power state change into non-AC mode.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span><span class="sxs-lookup"><span data-stu-id="b930f-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-136">Pausou o trabalho devido à perda de conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="b930f-136">DO paused the job due to loss of network connectivity.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span><span class="sxs-lookup"><span data-stu-id="b930f-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-138">Pausou o trabalho concluído devido à detecção da rede VPN.</span><span class="sxs-lookup"><span data-stu-id="b930f-138">DO paused the completed job due to detection of VPN network.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span><span class="sxs-lookup"><span data-stu-id="b930f-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-140">Pausou o trabalho concluído devido à detecção de uso de memória crítica no sistema.</span><span class="sxs-lookup"><span data-stu-id="b930f-140">DO paused the completed job due to detection of critical memory usage on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span><span class="sxs-lookup"><span data-stu-id="b930f-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-142">O servidor HTTP retornou uma resposta com tamanho de dados diferente do que foi solicitado.</span><span class="sxs-lookup"><span data-stu-id="b930f-142">HTTP server returned a response with data size not equal to what was requested.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span><span class="sxs-lookup"><span data-stu-id="b930f-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-144">O intervalo de bytes especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="b930f-144">The specified byte range is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span><span class="sxs-lookup"><span data-stu-id="b930f-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-146">O servidor não oferece suporte ao protocolo HTTP necessário.</span><span class="sxs-lookup"><span data-stu-id="b930f-146">The server does not support the necessary HTTP protocol.</span></span> <span data-ttu-id="b930f-147">A otimização de entrega (DO) exige que o servidor dê suporte ao cabeçalho de protocolo do intervalo.</span><span class="sxs-lookup"><span data-stu-id="b930f-147">Delivery Optimization (DO) requires that the server support the Range protocol header.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span><span class="sxs-lookup"><span data-stu-id="b930f-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-149">A lista de intervalos de bytes contém alguns intervalos sobrepostos, que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="b930f-149">The list of byte ranges contains some overlapping ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b930f-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span><span class="sxs-lookup"><span data-stu-id="b930f-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span></span>
</dt> <dd>

<span data-ttu-id="b930f-151">Erro fatal encontrado no núcleo.</span><span class="sxs-lookup"><span data-stu-id="b930f-151">Fatal error encountered in core.</span></span>

</dd> </dl>

 

 