---
title: Enumeração MPNOTIFY (MpClient. h)
description: Possíveis notificações de retorno de chamada.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- recursos de ambiente Windows de enumeração herdados do MPNOTIFY
- Windows recursos de ambiente herdados do ponteiro de enumeração PMPNOTIFY
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed62a9f868aa39cbc0cfc7702afc99849005a22106892696eca857ffb20673af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747784"
---
# <a name="mpnotify-enumeration"></a>Enumeração MPNOTIFY

Possíveis notificações de retorno de chamada.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ nenhum**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_início da chamada do mpnotify \_**
</dt> <dd>

Início da chamada de notificação.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_chamada mpnotify \_ concluída**
</dt> <dd>

Chamada de notificação concluída.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_falha interna do mpnotify \_**
</dt> <dd>

Falha interna genérica.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_início do \_ serviço de status mpnotify \_**
</dt> <dd>

O serviço de proteção contra malware foi iniciado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_serviço de status mpnotify \_ \_ em execução**
</dt> <dd>

O serviço de proteção contra malware está em execução.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_interrupção do \_ serviço de status mpnotify \_**
</dt> <dd>

O serviço de proteção contra malware foi interrompido.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_componente de status do mpnotify \_**
</dt> <dd>

Componente específico habilitar/desabilitar status.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_alteração de status de mpnotify \_**
</dt> <dd>

O status geral do produto foi alterado. Chame [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) para obter o status atual.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configuração do \_ componente de status do mpnotify \_**
</dt> <dd>

Um componente específico alterou A configuração.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_alteração de \_ expiração de status do mpnotify \_**
</dt> <dd>

O status de expiração do produto foi alterado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**\_alteração da \_ \_ verificação offline de status \_ do mpnotify**
</dt> <dd>

Estado de verificação offline necessário alterado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_início da verificação de mpnotify \_**
</dt> <dd>

Verificação iniciada.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**verificação de MPNOTIFY \_ \_ pausada**
</dt> <dd>

Verificação pausada.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**verificação do MPNOTIFY \_ \_ retomada**
</dt> <dd>

verificação retomada.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY de \_ verificação \_ cancelada**
</dt> <dd>

Verificação cancelada.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**verificação de MPNOTIFY \_ \_ concluída**
</dt> <dd>

Verificação concluída.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_progresso da verificação de mpnotify \_**
</dt> <dd>

Notificação de progresso para o recurso específico que está sendo examinado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_erro de verificação de mpnotify \_**
</dt> <dd>

Falha ao verificar um recurso específico. A verificação ainda continuará.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**verificação de MPNOTIFY \_ \_ infectada**
</dt> <dd>

A verificação encontrou um recurso infectado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ Scan \_ MEMORYSTART**
</dt> <dd>

O progresso da verificação para notificar a parte da verificação de memória do sistema foi iniciado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**
</dt> <dd>

O progresso da verificação para notificar a parte da verificação de memória do sistema foi concluído.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**\_início da \_ \_ compilação Sfc \_ do mpnotify Scan**
</dt> <dd>

O andamento da verificação para notificar a parte da compilação do Sfc foi iniciado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**compilação do Sfc de verificação do MPNOTIFY \_ \_ \_ \_ concluída**
</dt> <dd>

O andamento da verificação para notificar a parte da compilação do Sfc foi concluído.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ verificação \_ FASTPATH \_ Iniciar**
</dt> <dd>

A verificação do FastPath SpyNet foi iniciada.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ verificação \_ FASTPATH \_ concluída**
</dt> <dd>

Exame FastPath SpyNet terminou.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**andamento da verificação do MPNOTIFY \_ \_ FASTPATH \_**
</dt> <dd>

Notificação de progresso para verificações de FastPath, usadas internamente e convertidas em **\_ \_ andamento da verificação do mpnotify** para o externo.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_início da limpeza do mpnotify \_**
</dt> <dd>

Limpeza iniciada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**limpeza de MPNOTIFY \_ \_ concluída**
</dt> <dd>

Limpeza concluída.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ limpar \_ RESTOREPOINT \_ Iniciar**
</dt> <dd>

Iniciada a criação de um ponto de restauração do sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ limpar \_ RESTOREPOINT com \_ êxito**
</dt> <dd>

Ponto de restauração do sistema criado com êxito.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ limpar \_ RESTOREPOINT \_ falhou**
</dt> <dd>

Falha na criação do ponto de restauração do sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_início da \_ ameaça de limpeza do mpnotify \_**
</dt> <dd>

A limpeza é iniciada para uma determinada ameaça.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**ameaça de limpeza de MPNOTIFY \_ \_ \_ bem-sucedida**
</dt> <dd>

A limpeza foi bem-sucedida para uma determinada ameaça.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**\_ \_ falha ao limpar ameaça mpnotify \_**
</dt> <dd>

A limpeza falhou para uma determinada ameaça. **Erro \_ do O código de erro de ameaça de MP \_ \_ não \_ encontrado** indica que a ameaça não foi encontrada (e não foi uma falha de limpeza).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**\_êxito ao limpar \_ recurso \_ mpnotify**
</dt> <dd>

A limpeza foi bem-sucedida para um recurso específico.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_ \_ falha ao limpar recurso mpnotify \_**
</dt> <dd>

A limpeza falhou para um recurso específico.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ limpeza de \_ ameaças \_ concluída**
</dt> <dd>

A limpeza foi concluída para uma determinada ameaça.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**\_início da PREverificação de mpnotify \_**
</dt> <dd>

Limpar preverificação iniciada.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**preverificação de MPNOTIFY \_ \_ concluída**
</dt> <dd>

Limpeza de marca de seleção concluída.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**recurso de MPNOTIFY de \_ verificação \_ \_ bloqueado**
</dt> <dd>

Limpar preverificação detectou recurso bloqueado.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_ameaça mpnotify \_ detectada**
</dt> <dd>

Nova ameaça detectada no sistema.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_ameaça mpnotify \_ modificada**
</dt> <dd>

Informações de ameaças modificadas. Por exemplo, um novo recurso foi adicionado.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**limpeza de ameaça de MPNOTIFY \_ \_ \_ bem-sucedida**
</dt> <dd>

Ação de limpeza bem-sucedida para uma ameaça.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**\_ \_ falha ao limpar ameaça mpnotify \_**
</dt> <dd>

Falha na ação de limpeza para uma ameaça. **ERRO \_ O código de erro MP \_ THREAT \_ NOT \_ FOUND** indica que a ameaça não foi encontrada (e não foi uma falha de limpeza).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY \_ THREAT \_ ABANDONED**
</dt> <dd>

Nenhuma correção ocorreu antes de o serviço ser interrompido.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ EVENT \_ START**
</dt> <dd>

Uma ação de limpeza foi iniciada.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**EVENTO MPNOTIFY \_ THREAT \_ CLEAN \_ \_ CONCLUÍDO**
</dt> <dd>

Uma ação de limpeza foi encerrada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ START**
</dt> <dd>

Atualização de assinatura iniciada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ START**
</dt> <dd>

Pesquise atualizações iniciadas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ COMPLETE**
</dt> <dd>

Pesquise atualizações concluídas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY \_ SIGUPDATE \_ SOFTWARE \_ UPDATE \_ AVAILABLE**
</dt> <dd>

Atualização de software disponível.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ START**
</dt> <dd>

Download iniciado.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ PROGRESS**
</dt> <dd>

Download em andamento. Os dados de retorno de chamada contêm progresso.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ COMPLETE**
</dt> <dd>

Download concluído.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ START**
</dt> <dd>

Instalação iniciada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ PROGRESS**
</dt> <dd>

Instalação em andamento. Os dados de retorno de chamada contêm progresso.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ INSTALL \_ COMPLETE**
</dt> <dd>

Instalação concluída.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY \_ SIGUPDATE \_ REBOOT \_ REQUIRED**
</dt> <dd>

A atualização requer reinicialização.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**SOLICITAÇÃO MPNOTIFY \_ SIGUPDATE \_ \_ PROCESSADA**
</dt> <dd>

O serviço processou uma solicitação de atualização de assinatura. Falha ou êxito é indicado por **hResult** nos dados de retorno de chamada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ CONCLUÍDO**
</dt> <dd>

Atualização concluída. **S \_ O** status FALSE indica que nenhuma atualização foi necessária.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY \_ SAMPLE \_ START**
</dt> <dd>

Envio de exemplo iniciado.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY \_ SAMPLE \_ COMPLETE**
</dt> <dd>

Envio de exemplo concluído.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY \_ SAMPLE \_ ITEM \_ START**
</dt> <dd>

Envio de item de exemplo específico iniciado. O índice de item de exemplo está disponível [**em MPSAMPLE \_ DATA.**](mpsample-data.md)

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**ITEM DE EXEMPLO MPNOTIFY \_ \_ \_ BEM-SUCEDIDO**
</dt> <dd>

Envio de item de exemplo específico bem-sucedido.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**FALHA NO ITEM DE EXEMPLO MPNOTIFY \_ \_ \_**
</dt> <dd>

Falha no envio de item de exemplo específico. O código de erro está disponível em [**DADOS MPCALLBACK. \_**](mpcallback-data.md)

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**DADOS RESERVADOS DO \_ MPNOTIFY \_**
</dt> <dd>

Dados reservados internos.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ ADICIONADO**
</dt> <dd>

Uma assinatura fastpath adicionou ou desabilitou uma assinatura.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ REMOVIDO**
</dt> <dd>

Uma assinatura FastPath foi removida.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ PRIVATE**
</dt> <dd>

Notificações privadas da NIS. Nenhum parceiro deve se registrar para isso.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY \_ HEALTH \_ CHANGE**
</dt> <dd>

O serviço AM entrou em um novo estado.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY \_ HEALTH \_ RECOVERY**
</dt> <dd>

O serviço AM foi recuperado de um estado.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY \_ HEALTH \_ START**
</dt> <dd>

O serviço AM inicializou a saúde do sistema.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY \_ ENDOFLIFE \_ CHANGE**
</dt> <dd>

As datas de expiração "Fim da Vida Útil" para o serviço AM foram alteradas.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ DATA**
</dt> <dd>

O serviço AM encontrou malware que pode ter causado alteração de configurações críticas no computador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**DADOS \_ MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**DADOS MPSAMPLE \_**](mpsample-data.md)
</dt> </dl>

 

 





