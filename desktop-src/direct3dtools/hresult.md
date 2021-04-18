---
description: Valores de HRESULT personalizados para a interface de captura de diagnóstico de gráficos.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500429"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="7b662-103"><span id="vspixengine.hresult"></span>Enumeração HRESULT</span><span class="sxs-lookup"><span data-stu-id="7b662-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="7b662-104">Valores de HRESULT personalizados para a interface de captura de diagnóstico de gráficos.</span><span class="sxs-lookup"><span data-stu-id="7b662-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b662-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b662-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="7b662-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7b662-106">Constants</span></span>

<span data-ttu-id="7b662-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="7b662-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="7b662-108">Um HRESULT comum que indica que a operação foi bem-sucedida conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="7b662-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="7b662-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="7b662-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="7b662-110">Um HRESULT comum que indica que a operação foi bem-sucedida, mas de uma maneira diferente da esperada.</span><span class="sxs-lookup"><span data-stu-id="7b662-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="7b662-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**arquivo de erro do PIX \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="7b662-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="7b662-112">Um HRESULT personalizado que ecoa o arquivo de erro \_ \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="7b662-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="7b662-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**\_ \_ ambiente insatisfatório de erro do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="7b662-114">Um HRESULT personalizado que ecoa um erro \_ de \_ ambiente insatisfatório.</span><span class="sxs-lookup"><span data-stu-id="7b662-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="7b662-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_ \_ formato inadequado de erro do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="7b662-116">Um HRESULT personalizado que ecoa um \_ formato inadequado de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="7b662-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_violação de \_ compartilhamento de erro do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="7b662-118">Um HRESULT personalizado que ecoa a violação de compartilhamento de erro \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="7b662-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**disco de erro do PIX \_ \_ \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="7b662-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="7b662-120">Um HRESULT personalizado que ecoa o disco de erro \_ \_ cheio.</span><span class="sxs-lookup"><span data-stu-id="7b662-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="7b662-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**erro de PIX \_ \_ mais \_ dados**</span><span class="sxs-lookup"><span data-stu-id="7b662-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="7b662-122">Um HRESULT personalizado que ecoa \_ mais dados de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="7b662-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_política de \_ \_ kits de depuração ausente \_ \_ do PIX E**</span><span class="sxs-lookup"><span data-stu-id="7b662-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="7b662-124">Um HRESULT personalizado que indica que a política de kits de depuração está ausente.</span><span class="sxs-lookup"><span data-stu-id="7b662-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="7b662-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**versão do PIX \_ E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="7b662-126">Um HRESULT personalizado que indica que uma versão inválida está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="7b662-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="7b662-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ usando \_ DCOMP**</span><span class="sxs-lookup"><span data-stu-id="7b662-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="7b662-128">Um HRESULT personalizado que indica que DirectComposition está em uso (a captura de DirectComposition não é suportada.)</span><span class="sxs-lookup"><span data-stu-id="7b662-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="7b662-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ usando \_ DIRECTWRITE**</span><span class="sxs-lookup"><span data-stu-id="7b662-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="7b662-130">Um HRESULT personalizado que indica que DirectWrite está em uso (a captura de DirectWrite não é suportada.)</span><span class="sxs-lookup"><span data-stu-id="7b662-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="7b662-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ usando \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="7b662-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="7b662-132">Um HRESULT personalizado que indica que o Direct3D9 está em uso (a captura de Direct3D9 não tem suporte no Windows 10).</span><span class="sxs-lookup"><span data-stu-id="7b662-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="7b662-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**o PIX \_ E não \_ consegue criar o \_ \_ sombreador**</span><span class="sxs-lookup"><span data-stu-id="7b662-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="7b662-134">Um HRESULT personalizado que indica que um sombreador especificado não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="7b662-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="7b662-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ usando \_ D2D**</span><span class="sxs-lookup"><span data-stu-id="7b662-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="7b662-136">Um HRESULT personalizado que indica que Direct2D está em uso (a captura de Direct2D não é suportada.)</span><span class="sxs-lookup"><span data-stu-id="7b662-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="7b662-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ sem \_ quadros**</span><span class="sxs-lookup"><span data-stu-id="7b662-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="7b662-138">Um HRESULT personalizado que indica que nenhum quadro foi capturado.</span><span class="sxs-lookup"><span data-stu-id="7b662-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="7b662-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ desabilitar o \_ Spy**</span><span class="sxs-lookup"><span data-stu-id="7b662-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="7b662-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ no \_ Win7**</span><span class="sxs-lookup"><span data-stu-id="7b662-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="7b662-141">Um HRESULT personalizado que indica que um vsglog do Windows 8 não pode ser reproduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b662-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="7b662-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_rastreamento de \_ \_ sombreador de Build \_ do PIX E**</span><span class="sxs-lookup"><span data-stu-id="7b662-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="7b662-143">Um HRESULT personalizado que indica que houve um erro ao criar o rastreamento do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7b662-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="7b662-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**visualização de dados do PIX \_ E \_ no \_ cs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="7b662-145">Um HRESULT personalizado que indica que não há nenhuma visualização de dados do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="7b662-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="7b662-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_SDK de \_ incompatibilidade de PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="7b662-147">Um HRESULT personalizado que indica que há uma incompatibilidade com o SDK atual.</span><span class="sxs-lookup"><span data-stu-id="7b662-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="7b662-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**\_SDK E \_ possível \_ INcompatibilidade do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="7b662-149">Um HRESULT personalizado que indica que há uma possível incompatibilidade com o SDK atual.</span><span class="sxs-lookup"><span data-stu-id="7b662-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="7b662-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIXEL do PIX \_ E não \_ detectável \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="7b662-151">Um HRESULT personalizado que indica que há um pixel não detectável.</span><span class="sxs-lookup"><span data-stu-id="7b662-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="7b662-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**o PIX \_ E não \_ consegue depurar o \_ \_ sombreador \_ usando a \_ \_ semântica de valor do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="7b662-153">Um HRESULT personalizado que indica que o sahder não pode ser depurado usando semântica de valor do sistema.</span><span class="sxs-lookup"><span data-stu-id="7b662-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="7b662-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**UPDATEAVAILABLE de PIX \_ S \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="7b662-155">Um HRESULT personalizado que indica que há uma atualização disponível.</span><span class="sxs-lookup"><span data-stu-id="7b662-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="7b662-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**STATUS de dxgi do PIX \_ \_ \_ sem \_ redirecionamento**</span><span class="sxs-lookup"><span data-stu-id="7b662-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="7b662-157">Um HRESULT personalizado que ecoa o status de DXGI \_ \_ sem \_ redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="7b662-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="7b662-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**STATUS de dxgi do PIX \_ \_ \_ sem \_ acesso à área de trabalho \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="7b662-159">Um HRESULT personalizado que ecoa o \_ status dxgi \_ sem \_ acesso à área de trabalho \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="7b662-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ origem VIDPN dos gráficos \_ \_ de status \_ de dxgi do PIX em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="7b662-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="7b662-161">Um HRESULT personalizado que ecoa a \_ \_ \_ fonte VIDPN de gráficos \_ de status dxgi \_ em \_ uso.</span><span class="sxs-lookup"><span data-stu-id="7b662-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="7b662-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**modo de status de dxgi do PIX \_ \_ \_ \_ alterado**</span><span class="sxs-lookup"><span data-stu-id="7b662-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="7b662-163">Um HRESULT personalizado que ecoa o \_ modo de status dxgi \_ \_ alterado.</span><span class="sxs-lookup"><span data-stu-id="7b662-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="7b662-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ \_ alteração do modo de status \_ de dxgi do PIX em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="7b662-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="7b662-165">Um HRESULT personalizado que ecoa a \_ \_ \_ alteração do modo de status dxgi \_ em \_ andamento.</span><span class="sxs-lookup"><span data-stu-id="7b662-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="7b662-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_UNOCCLUDED de \_ status de dxgi do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="7b662-167">Um HRESULT personalizado que ecoa o status de DXGI \_ \_ UNOCCLUDED.</span><span class="sxs-lookup"><span data-stu-id="7b662-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="7b662-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**o \_ status de dxgi do PIX \_ \_ DDA \_ \_ ainda estava sendo \_ desenhado**</span><span class="sxs-lookup"><span data-stu-id="7b662-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="7b662-169">Um HRESULT personalizado que ecoa o \_ status DDA do dxgi \_ \_ \_ ainda está \_ desenhando.</span><span class="sxs-lookup"><span data-stu-id="7b662-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="7b662-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ NOTIMPL**</span><span class="sxs-lookup"><span data-stu-id="7b662-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="7b662-171">Um HRESULT personalizado que ecoa E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="7b662-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="7b662-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**</span><span class="sxs-lookup"><span data-stu-id="7b662-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="7b662-173">Um HRESULT personalizado que ecoa E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="7b662-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="7b662-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_ponteiro E do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="7b662-175">Um HRESULT personalizado que ecoa o \_ ponteiro E.</span><span class="sxs-lookup"><span data-stu-id="7b662-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="7b662-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX \_ E \_ Abort**</span><span class="sxs-lookup"><span data-stu-id="7b662-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="7b662-177">Um HRESULT personalizado que ecoa E \_ aborta.</span><span class="sxs-lookup"><span data-stu-id="7b662-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="7b662-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**falha do PIX \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="7b662-179">Um HRESULT personalizado que ecoa E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="7b662-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="7b662-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ inesperado**</span><span class="sxs-lookup"><span data-stu-id="7b662-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="7b662-181">Um HRESULT personalizado que ecoa E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="7b662-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="7b662-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="7b662-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="7b662-183">Um HRESULT personalizado que ecoa E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="7b662-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="7b662-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**identificador de PIX \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="7b662-185">Um HRESULT personalizado que ecoa o E o \_ identificador.</span><span class="sxs-lookup"><span data-stu-id="7b662-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="7b662-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**o PIX \_ E a \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="7b662-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="7b662-187">Um HRESULT personalizado que ecoa E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7b662-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="7b662-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="7b662-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="7b662-189">Um HRESULT personalizado que ecoa E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="7b662-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="7b662-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**disco de erro do PIX \_ Xbox \_ \_ \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="7b662-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="7b662-191">Um HRESULT personalizado que indica que o disco está cheio.</span><span class="sxs-lookup"><span data-stu-id="7b662-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="7b662-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ endereço do PIX WS E \_ \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="7b662-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="7b662-193">Um HRESULT personalizado que indica que o endereço já está em uso.</span><span class="sxs-lookup"><span data-stu-id="7b662-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="7b662-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_política de \_ \_ kits ausentes do \_ PIX WS E \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="7b662-195">Um HRESULT personalizado que indica que o endereço não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7b662-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="7b662-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**FAILEDTOLOADSOFTWAREMODULE do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="7b662-197">Um HRESULT personalizado que indica que um módulo de software necessário falhou ao ser carregado.</span><span class="sxs-lookup"><span data-stu-id="7b662-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="7b662-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**USEDSOFTWAREMODULETHATWASNTWARPORREF do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="7b662-199">Um HRESULT personalizado que indica que o módulo de software usado não era o driver de WARP ou de referência.</span><span class="sxs-lookup"><span data-stu-id="7b662-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="7b662-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**o PIX \_ te \_ corruptfile**</span><span class="sxs-lookup"><span data-stu-id="7b662-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="7b662-201">Um HRESULT personalizado que indica que o arquivo está corrompido.</span><span class="sxs-lookup"><span data-stu-id="7b662-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="7b662-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**FAILEDTOOPENFILE do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="7b662-203">Um HRESULT personalizado que indica que o arquivo não pôde ser aberto.</span><span class="sxs-lookup"><span data-stu-id="7b662-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="7b662-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**CALLFAILEDONPLAYBACK do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="7b662-205">Um HRESULT personalizado que indica que uma chamada falhou durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="7b662-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="7b662-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**UNKNOWNUUID do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="7b662-207">Um HRESULT personalizado que indica que um UUID desconhecido foi encontrado; Isso nunca deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="7b662-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="7b662-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**NOTCAPTUREFILEORCORRUPTED do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="7b662-209">Um HRESULT personalizado que indica que o arquivo não é um arquivo de captura ou está corrompido.</span><span class="sxs-lookup"><span data-stu-id="7b662-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="7b662-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ te \_ mais recente**</span><span class="sxs-lookup"><span data-stu-id="7b662-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="7b662-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**o \_ & te do PIX \_ antigo**</span><span class="sxs-lookup"><span data-stu-id="7b662-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="7b662-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**INVALIDMOMENT do PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="7b662-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**Driver do PIX \_ te \_ insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="7b662-214">Um HRESULT personalizado que indica que o driver é inadequado.</span><span class="sxs-lookup"><span data-stu-id="7b662-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="7b662-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**\_erro de PIX não \_ consegue \_ acessar \_ DEPTHSTENCIL \_ na \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="7b662-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="7b662-216">Um HRESULT personalizado que indica que a CPU tentou acessar o buffer do estêncil de profundidade, resultando em um erro.</span><span class="sxs-lookup"><span data-stu-id="7b662-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="7b662-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**erro de PIX não é possível \_ \_ resolver a \_ \_ textura multiamostrada \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="7b662-218">Um HRESULT personalizado que indica que houve uma tentativa de resolver uma textura de várias amostras, resultando em um erro.</span><span class="sxs-lookup"><span data-stu-id="7b662-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="7b662-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_ \_ \_ chamada inválida de erro dxgi do PIX \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="7b662-220">Um HRESULT personalizado que ecoa uma \_ \_ chamada inválida de erro dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="7b662-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**erro de dxgi do PIX \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="7b662-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="7b662-222">Um HRESULT personalizado que ecoa o \_ erro dxgi \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="7b662-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="7b662-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_erro de \_ \_ mais \_ dados do PIX dxgi**</span><span class="sxs-lookup"><span data-stu-id="7b662-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="7b662-224">Um HRESULT personalizado que ecoa \_ mais dados de erro dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="7b662-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**erro de dxgi do PIX \_ \_ \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="7b662-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="7b662-226">Um HRESULT personalizado que ecoa o \_ erro dxgi \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7b662-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="7b662-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**dispositivo de erro do PIX \_ dxgi \_ \_ \_ removido**</span><span class="sxs-lookup"><span data-stu-id="7b662-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="7b662-228">Um HRESULT personalizado que ecoa o \_ dispositivo de erro dxgi \_ \_ removido.</span><span class="sxs-lookup"><span data-stu-id="7b662-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="7b662-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**dispositivo de erro do PIX \_ dxgi \_ \_ \_ suspenso**</span><span class="sxs-lookup"><span data-stu-id="7b662-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="7b662-230">Um HRESULT personalizado que ecoa o \_ dispositivo de erro dxgi \_ \_ suspenso.</span><span class="sxs-lookup"><span data-stu-id="7b662-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="7b662-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**redefinição de dispositivo de erro do PIX \_ dxgi \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="7b662-232">Um HRESULT personalizado que ecoa a \_ redefinição do dispositivo de erro dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="7b662-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**o \_ erro do PIX dxgi \_ \_ \_ ainda estava sendo \_ desenhado**</span><span class="sxs-lookup"><span data-stu-id="7b662-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="7b662-234">Um HRESULT personalizado que ecoa o \_ erro dxgi \_ \_ ainda estava \_ desenhando.</span><span class="sxs-lookup"><span data-stu-id="7b662-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="7b662-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**Estatísticas de quadros de erro do PIX \_ dxgi não \_ \_ \_ \_ contíguos**</span><span class="sxs-lookup"><span data-stu-id="7b662-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="7b662-236">Um HRESULT personalizado que ecoa as estatísticas de quadro de erro DXGI não \_ \_ \_ \_ contíguos.</span><span class="sxs-lookup"><span data-stu-id="7b662-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="7b662-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ fonte de erro do PIX dxgi gráfica \_ VIDPN \_ \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="7b662-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="7b662-238">Um HRESULT personalizado que ecoa a \_ \_ \_ fonte VIDPN de gráficos \_ de erro dxgi \_ em \_ uso.</span><span class="sxs-lookup"><span data-stu-id="7b662-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="7b662-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ erro interno do driver de erro \_ do PIX dxgi \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="7b662-240">Um HRESULT personalizado que ecoa o \_ erro interno do driver de erro dxgi \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="7b662-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**erro não exclusivo do PIX \_ dxgi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="7b662-242">Um HRESULT personalizado que ecoa o erro DXGI não \_ \_ exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7b662-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="7b662-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**o \_ erro dxgi do PIX \_ \_ não está \_ disponível no momento \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="7b662-244">Um HRESULT personalizado que ecoa o \_ erro dxgi \_ não \_ disponível no momento \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="7b662-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**\_erro de \_ \_ cliente remoto \_ \_ desconectado do PIX dxgi**</span><span class="sxs-lookup"><span data-stu-id="7b662-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="7b662-246">Um HRESULT personalizado que ecoa o \_ cliente remoto de erro dxgi \_ \_ \_ desconectado.</span><span class="sxs-lookup"><span data-stu-id="7b662-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="7b662-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_ \_ \_ OUTOFMEMORY remota de erro \_ do PIX dxgi**</span><span class="sxs-lookup"><span data-stu-id="7b662-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="7b662-248">Um HRESULT personalizado que ecoa a \_ OUTOFMEMORY remota de erro dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="7b662-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ \_ alteração do modo de erro \_ do PIX dxgi em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="7b662-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="7b662-250">Um HRESULT personalizado que ecoa a \_ \_ \_ alteração do modo de erro dxgi \_ em \_ andamento.</span><span class="sxs-lookup"><span data-stu-id="7b662-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="7b662-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_ \_ acesso ao erro do PIX dxgi \_ \_ perdido**</span><span class="sxs-lookup"><span data-stu-id="7b662-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="7b662-252">Um HRESULT personalizado que ecoa o \_ acesso ao erro dxgi \_ \_ perdido.</span><span class="sxs-lookup"><span data-stu-id="7b662-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="7b662-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_ \_ \_ tempo limite de espera de erro \_ do PIX dxgi**</span><span class="sxs-lookup"><span data-stu-id="7b662-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="7b662-254">Um HRESULT personalizado que ecoa o \_ tempo limite de espera de erro dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="7b662-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**sessão de erro do PIX \_ dxgi \_ \_ \_ desconectada**</span><span class="sxs-lookup"><span data-stu-id="7b662-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="7b662-256">Um HRESULT personalizado que ecoa a \_ sessão de erro dxgi \_ \_ desconectada.</span><span class="sxs-lookup"><span data-stu-id="7b662-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="7b662-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**erro do PIX \_ dxgi \_ \_ restringir \_ para \_ saída \_ obsoleta**</span><span class="sxs-lookup"><span data-stu-id="7b662-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="7b662-258">Um HRESULT personalizado que ecoa o \_ erro dxgi \_ restringir \_ para \_ saída \_ obsoleta.</span><span class="sxs-lookup"><span data-stu-id="7b662-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="7b662-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**o \_ erro dxgi do PIX \_ \_ não pode \_ proteger o \_ conteúdo**</span><span class="sxs-lookup"><span data-stu-id="7b662-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="7b662-260">Um HRESULT personalizado que ecoa o \_ erro dxgi \_ não pode \_ proteger o \_ conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7b662-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="7b662-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ \_ acesso \_ negado ao pix**</span><span class="sxs-lookup"><span data-stu-id="7b662-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="7b662-262">Um HRESULT personalizado que retorna o erro de acesso a DXGI \_ \_ \_ negado.</span><span class="sxs-lookup"><span data-stu-id="7b662-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="7b662-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**o \_ nome de erro do PIX dxgi \_ \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="7b662-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="7b662-264">Um HRESULT personalizado que ecoa o \_ nome de erro dxgi \_ \_ já \_ existe.</span><span class="sxs-lookup"><span data-stu-id="7b662-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="7b662-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_componente SDK de erro do PIX dxgi \_ \_ \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="7b662-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="7b662-266">Um HRESULT personalizado que ecoa o \_ componente SDK de erro dxgi \_ \_ \_ ausente.</span><span class="sxs-lookup"><span data-stu-id="7b662-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="7b662-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_WASSTILLDRAWING de \_ erro de DDI \_ \_ do PIX dxgi**</span><span class="sxs-lookup"><span data-stu-id="7b662-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="7b662-268">Um HRESULT personalizado que ecoa o \_ erro WASSTILLDRAWING de DDI de dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="7b662-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**erro de DDI do PIX \_ dxgi \_ \_ \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="7b662-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="7b662-270">Um HRESULT personalizado que ecoa o erro de DDI de DXGI \_ \_ \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7b662-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="7b662-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_erro não \_ exclusivo de DDI \_ \_ do PIX dxgi**</span><span class="sxs-lookup"><span data-stu-id="7b662-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="7b662-272">Um HRESULT personalizado que ecoa um erro de DDI de DXGI não \_ \_ \_ exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7b662-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="7b662-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**O PIX d3d10 erro é um número \_ excessivo de objetos de \_ \_ \_ \_ \_ estado exclusivos \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="7b662-274">Um HRESULT personalizado que ecoa um erro D3D10 em \_ \_ excesso de objetos de \_ \_ \_ estado exclusivos \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="7b662-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_Arquivo de erro d3d10 do PIX \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="7b662-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="7b662-276">Um HRESULT personalizado que ecoa o \_ arquivo de erro d3d10 \_ \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="7b662-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="7b662-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**O PIX D3D11 erro é um número \_ excessivo de objetos de \_ \_ \_ \_ \_ estado exclusivos \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="7b662-278">Um HRESULT personalizado que ecoa um erro D3D11 em \_ \_ excesso de objetos de \_ \_ \_ estado exclusivos \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="7b662-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_Arquivo de erro D3D11 do PIX \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="7b662-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="7b662-280">Um HRESULT personalizado que ecoa o \_ arquivo de erro D3D11 \_ \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="7b662-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="7b662-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**Erro D3D11 do PIX- \_ \_ \_ \_ muitos \_ \_ objetos de exibição exclusivos \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="7b662-282">Um HRESULT personalizado que ecoa o \_ erro D3D11 \_ de \_ muitos \_ \_ objetos de exibição exclusivos \_ .</span><span class="sxs-lookup"><span data-stu-id="7b662-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="7b662-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**\_Erro D3D11 do PIX \_ mapa de \_ contexto adiado \_ \_ \_ sem \_ \_ descarte inicial**</span><span class="sxs-lookup"><span data-stu-id="7b662-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="7b662-284">Um HRESULT personalizado que ecoa o erro D3D11 do \_ \_ mapa de contexto adiado \_ \_ \_ sem \_ \_ descarte inicial.</span><span class="sxs-lookup"><span data-stu-id="7b662-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="7b662-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**erro de PIX \_ \_ obstruído \_ chamada de desenho \_**</span><span class="sxs-lookup"><span data-stu-id="7b662-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="7b662-286">Um HRESULT personalizado que indica que uma chamada de desenho foi totalmente obstruído, resultando em um erro.</span><span class="sxs-lookup"><span data-stu-id="7b662-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b662-287">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b662-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7b662-288">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b662-288">Header</span></span></p></td><td><span data-ttu-id="7b662-289">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7b662-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



