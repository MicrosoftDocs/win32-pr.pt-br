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
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Enumeração HRESULT

Valores de HRESULT personalizados para a interface de captura de diagnóstico de gráficos.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**  
Um HRESULT comum que indica que a operação foi bem-sucedida conforme o esperado.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**  
Um HRESULT comum que indica que a operação foi bem-sucedida, mas de uma maneira diferente da esperada.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**arquivo de erro do PIX \_ \_ \_ não \_ encontrado**  
Um HRESULT personalizado que ecoa o arquivo de erro \_ \_ não \_ encontrado.

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**\_ \_ ambiente insatisfatório de erro do PIX \_**  
Um HRESULT personalizado que ecoa um erro \_ de \_ ambiente insatisfatório.

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_ \_ formato inadequado de erro do PIX \_**  
Um HRESULT personalizado que ecoa um \_ formato inadequado de erro \_ .

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_violação de \_ compartilhamento de erro do PIX \_**  
Um HRESULT personalizado que ecoa a violação de compartilhamento de erro \_ \_ .

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**disco de erro do PIX \_ \_ \_ cheio**  
Um HRESULT personalizado que ecoa o disco de erro \_ \_ cheio.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**erro de PIX \_ \_ mais \_ dados**  
Um HRESULT personalizado que ecoa \_ mais dados de erro \_ .

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_política de \_ \_ kits de depuração ausente \_ \_ do PIX E**  
Um HRESULT personalizado que indica que a política de kits de depuração está ausente.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**versão do PIX \_ E \_ inválida \_**  
Um HRESULT personalizado que indica que uma versão inválida está sendo usada.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ usando \_ DCOMP**  
Um HRESULT personalizado que indica que DirectComposition está em uso (a captura de DirectComposition não é suportada.)

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ usando \_ DIRECTWRITE**  
Um HRESULT personalizado que indica que DirectWrite está em uso (a captura de DirectWrite não é suportada.)

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ usando \_ d3d9**  
Um HRESULT personalizado que indica que o Direct3D9 está em uso (a captura de Direct3D9 não tem suporte no Windows 10).

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**o PIX \_ E não \_ consegue criar o \_ \_ sombreador**  
Um HRESULT personalizado que indica que um sombreador especificado não pode ser criado.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ usando \_ D2D**  
Um HRESULT personalizado que indica que Direct2D está em uso (a captura de Direct2D não é suportada.)

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ sem \_ quadros**  
Um HRESULT personalizado que indica que nenhum quadro foi capturado.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ desabilitar o \_ Spy**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ no \_ Win7**  
Um HRESULT personalizado que indica que um vsglog do Windows 8 não pode ser reproduzido no Windows 7.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_rastreamento de \_ \_ sombreador de Build \_ do PIX E**  
Um HRESULT personalizado que indica que houve um erro ao criar o rastreamento do sombreador.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**visualização de dados do PIX \_ E \_ no \_ cs \_ \_**  
Um HRESULT personalizado que indica que não há nenhuma visualização de dados do sombreador de computação.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_SDK de \_ incompatibilidade de PIX E \_**  
Um HRESULT personalizado que indica que há uma incompatibilidade com o SDK atual.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**\_SDK E \_ possível \_ INcompatibilidade do PIX \_**  
Um HRESULT personalizado que indica que há uma possível incompatibilidade com o SDK atual.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIXEL do PIX \_ E não \_ detectável \_**  
Um HRESULT personalizado que indica que há um pixel não detectável.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**o PIX \_ E não \_ consegue depurar o \_ \_ sombreador \_ usando a \_ \_ semântica de valor do sistema \_**  
Um HRESULT personalizado que indica que o sahder não pode ser depurado usando semântica de valor do sistema.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**UPDATEAVAILABLE de PIX \_ S \_**  
Um HRESULT personalizado que indica que há uma atualização disponível.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**STATUS de dxgi do PIX \_ \_ \_ sem \_ redirecionamento**  
Um HRESULT personalizado que ecoa o status de DXGI \_ \_ sem \_ redirecionamento.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**STATUS de dxgi do PIX \_ \_ \_ sem \_ acesso à área de trabalho \_**  
Um HRESULT personalizado que ecoa o \_ status dxgi \_ sem \_ acesso à área de trabalho \_ .

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ origem VIDPN dos gráficos \_ \_ de status \_ de dxgi do PIX em \_ uso**  
Um HRESULT personalizado que ecoa a \_ \_ \_ fonte VIDPN de gráficos \_ de status dxgi \_ em \_ uso.

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**modo de status de dxgi do PIX \_ \_ \_ \_ alterado**  
Um HRESULT personalizado que ecoa o \_ modo de status dxgi \_ \_ alterado.

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ \_ alteração do modo de status \_ de dxgi do PIX em \_ andamento**  
Um HRESULT personalizado que ecoa a \_ \_ \_ alteração do modo de status dxgi \_ em \_ andamento.

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_UNOCCLUDED de \_ status de dxgi do PIX \_**  
Um HRESULT personalizado que ecoa o status de DXGI \_ \_ UNOCCLUDED.

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**o \_ status de dxgi do PIX \_ \_ DDA \_ \_ ainda estava sendo \_ desenhado**  
Um HRESULT personalizado que ecoa o \_ status DDA do dxgi \_ \_ \_ ainda está \_ desenhando.

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ NOTIMPL**  
Um HRESULT personalizado que ecoa E \_ NOTIMPL.

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**  
Um HRESULT personalizado que ecoa E \_ nointerface.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_ponteiro E do PIX \_**  
Um HRESULT personalizado que ecoa o \_ ponteiro E.

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX \_ E \_ Abort**  
Um HRESULT personalizado que ecoa E \_ aborta.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**falha do PIX \_ E \_**  
Um HRESULT personalizado que ecoa E \_ falha.

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ inesperado**  
Um HRESULT personalizado que ecoa E \_ inesperado.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**  
Um HRESULT personalizado que ecoa E \_ ACCESSDENIED.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**identificador de PIX \_ E \_**  
Um HRESULT personalizado que ecoa o E o \_ identificador.

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**o PIX \_ E a \_ OUTOFMEMORY**  
Um HRESULT personalizado que ecoa E \_ OUTOFMEMORY.

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**  
Um HRESULT personalizado que ecoa E \_ INVALIDARG.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**disco de erro do PIX \_ Xbox \_ \_ \_ cheio**  
Um HRESULT personalizado que indica que o disco está cheio.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ endereço do PIX WS E \_ \_ em \_ uso**  
Um HRESULT personalizado que indica que o endereço já está em uso.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_política de \_ \_ kits ausentes do \_ PIX WS E \_**  
Um HRESULT personalizado que indica que o endereço não está disponível.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**FAILEDTOLOADSOFTWAREMODULE do PIX \_ \_**  
Um HRESULT personalizado que indica que um módulo de software necessário falhou ao ser carregado.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**USEDSOFTWAREMODULETHATWASNTWARPORREF do PIX \_ \_**  
Um HRESULT personalizado que indica que o módulo de software usado não era o driver de WARP ou de referência.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**o PIX \_ te \_ corruptfile**  
Um HRESULT personalizado que indica que o arquivo está corrompido.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**FAILEDTOOPENFILE do PIX \_ \_**  
Um HRESULT personalizado que indica que o arquivo não pôde ser aberto.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**CALLFAILEDONPLAYBACK do PIX \_ \_**  
Um HRESULT personalizado que indica que uma chamada falhou durante a reprodução.

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**UNKNOWNUUID do PIX \_ \_**  
Um HRESULT personalizado que indica que um UUID desconhecido foi encontrado; Isso nunca deve ocorrer.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**NOTCAPTUREFILEORCORRUPTED do PIX \_ \_**  
Um HRESULT personalizado que indica que o arquivo não é um arquivo de captura ou está corrompido.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ te \_ mais recente**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**o \_ & te do PIX \_ antigo**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**INVALIDMOMENT do PIX \_ \_**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**Driver do PIX \_ te \_ insatisfatório \_**  
Um HRESULT personalizado que indica que o driver é inadequado.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**\_erro de PIX não \_ consegue \_ acessar \_ DEPTHSTENCIL \_ na \_ CPU**  
Um HRESULT personalizado que indica que a CPU tentou acessar o buffer do estêncil de profundidade, resultando em um erro.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**erro de PIX não é possível \_ \_ resolver a \_ \_ textura multiamostrada \_**  
Um HRESULT personalizado que indica que houve uma tentativa de resolver uma textura de várias amostras, resultando em um erro.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_ \_ \_ chamada inválida de erro dxgi do PIX \_**  
Um HRESULT personalizado que ecoa uma \_ \_ chamada inválida de erro dxgi \_ .

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**erro de dxgi do PIX \_ \_ \_ não \_ encontrado**  
Um HRESULT personalizado que ecoa o \_ erro dxgi \_ não \_ encontrado.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_erro de \_ \_ mais \_ dados do PIX dxgi**  
Um HRESULT personalizado que ecoa \_ mais dados de erro dxgi \_ \_ .

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**erro de dxgi do PIX \_ \_ \_ sem suporte**  
Um HRESULT personalizado que ecoa o \_ erro dxgi \_ sem suporte.

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**dispositivo de erro do PIX \_ dxgi \_ \_ \_ removido**  
Um HRESULT personalizado que ecoa o \_ dispositivo de erro dxgi \_ \_ removido.

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**dispositivo de erro do PIX \_ dxgi \_ \_ \_ suspenso**  
Um HRESULT personalizado que ecoa o \_ dispositivo de erro dxgi \_ \_ suspenso.

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**redefinição de dispositivo de erro do PIX \_ dxgi \_ \_ \_**  
Um HRESULT personalizado que ecoa a \_ redefinição do dispositivo de erro dxgi \_ \_ .

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**o \_ erro do PIX dxgi \_ \_ \_ ainda estava sendo \_ desenhado**  
Um HRESULT personalizado que ecoa o \_ erro dxgi \_ \_ ainda estava \_ desenhando.

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**Estatísticas de quadros de erro do PIX \_ dxgi não \_ \_ \_ \_ contíguos**  
Um HRESULT personalizado que ecoa as estatísticas de quadro de erro DXGI não \_ \_ \_ \_ contíguos.

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ fonte de erro do PIX dxgi gráfica \_ VIDPN \_ \_ em \_ uso**  
Um HRESULT personalizado que ecoa a \_ \_ \_ fonte VIDPN de gráficos \_ de erro dxgi \_ em \_ uso.

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ erro interno do driver de erro \_ do PIX dxgi \_**  
Um HRESULT personalizado que ecoa o \_ erro interno do driver de erro dxgi \_ \_ \_ .

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**erro não exclusivo do PIX \_ dxgi \_ \_**  
Um HRESULT personalizado que ecoa o erro DXGI não \_ \_ exclusivo.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**o \_ erro dxgi do PIX \_ \_ não está \_ disponível no momento \_**  
Um HRESULT personalizado que ecoa o \_ erro dxgi \_ não \_ disponível no momento \_ .

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**\_erro de \_ \_ cliente remoto \_ \_ desconectado do PIX dxgi**  
Um HRESULT personalizado que ecoa o \_ cliente remoto de erro dxgi \_ \_ \_ desconectado.

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_ \_ \_ OUTOFMEMORY remota de erro \_ do PIX dxgi**  
Um HRESULT personalizado que ecoa a \_ OUTOFMEMORY remota de erro dxgi \_ \_ .

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ \_ alteração do modo de erro \_ do PIX dxgi em \_ andamento**  
Um HRESULT personalizado que ecoa a \_ \_ \_ alteração do modo de erro dxgi \_ em \_ andamento.

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_ \_ acesso ao erro do PIX dxgi \_ \_ perdido**  
Um HRESULT personalizado que ecoa o \_ acesso ao erro dxgi \_ \_ perdido.

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_ \_ \_ tempo limite de espera de erro \_ do PIX dxgi**  
Um HRESULT personalizado que ecoa o \_ tempo limite de espera de erro dxgi \_ \_ .

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**sessão de erro do PIX \_ dxgi \_ \_ \_ desconectada**  
Um HRESULT personalizado que ecoa a \_ sessão de erro dxgi \_ \_ desconectada.

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**erro do PIX \_ dxgi \_ \_ restringir \_ para \_ saída \_ obsoleta**  
Um HRESULT personalizado que ecoa o \_ erro dxgi \_ restringir \_ para \_ saída \_ obsoleta.

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**o \_ erro dxgi do PIX \_ \_ não pode \_ proteger o \_ conteúdo**  
Um HRESULT personalizado que ecoa o \_ erro dxgi \_ não pode \_ proteger o \_ conteúdo.

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ \_ acesso \_ negado ao pix**  
Um HRESULT personalizado que retorna o erro de acesso a DXGI \_ \_ \_ negado.

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**o \_ nome de erro do PIX dxgi \_ \_ \_ já \_ existe**  
Um HRESULT personalizado que ecoa o \_ nome de erro dxgi \_ \_ já \_ existe.

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_componente SDK de erro do PIX dxgi \_ \_ \_ \_ ausente**  
Um HRESULT personalizado que ecoa o \_ componente SDK de erro dxgi \_ \_ \_ ausente.

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_WASSTILLDRAWING de \_ erro de DDI \_ \_ do PIX dxgi**  
Um HRESULT personalizado que ecoa o \_ erro WASSTILLDRAWING de DDI de dxgi \_ \_ .

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**erro de DDI do PIX \_ dxgi \_ \_ \_ sem suporte**  
Um HRESULT personalizado que ecoa o erro de DDI de DXGI \_ \_ \_ sem suporte.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_erro não \_ exclusivo de DDI \_ \_ do PIX dxgi**  
Um HRESULT personalizado que ecoa um erro de DDI de DXGI não \_ \_ \_ exclusivo.

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**O PIX d3d10 erro é um número \_ excessivo de objetos de \_ \_ \_ \_ \_ estado exclusivos \_**  
Um HRESULT personalizado que ecoa um erro D3D10 em \_ \_ excesso de objetos de \_ \_ \_ estado exclusivos \_ .

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_Arquivo de erro d3d10 do PIX \_ \_ \_ não \_ encontrado**  
Um HRESULT personalizado que ecoa o \_ arquivo de erro d3d10 \_ \_ não \_ encontrado.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**O PIX D3D11 erro é um número \_ excessivo de objetos de \_ \_ \_ \_ \_ estado exclusivos \_**  
Um HRESULT personalizado que ecoa um erro D3D11 em \_ \_ excesso de objetos de \_ \_ \_ estado exclusivos \_ .

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_Arquivo de erro D3D11 do PIX \_ \_ \_ não \_ encontrado**  
Um HRESULT personalizado que ecoa o \_ arquivo de erro D3D11 \_ \_ não \_ encontrado.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**Erro D3D11 do PIX- \_ \_ \_ \_ muitos \_ \_ objetos de exibição exclusivos \_**  
Um HRESULT personalizado que ecoa o \_ erro D3D11 \_ de \_ muitos \_ \_ objetos de exibição exclusivos \_ .

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**\_Erro D3D11 do PIX \_ mapa de \_ contexto adiado \_ \_ \_ sem \_ \_ descarte inicial**  
Um HRESULT personalizado que ecoa o erro D3D11 do \_ \_ mapa de contexto adiado \_ \_ \_ sem \_ \_ descarte inicial.

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**erro de PIX \_ \_ obstruído \_ chamada de desenho \_**  
Um HRESULT personalizado que indica que uma chamada de desenho foi totalmente obstruído, resultando em um erro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



