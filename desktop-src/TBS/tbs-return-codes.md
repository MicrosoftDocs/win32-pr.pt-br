---
title: Códigos de retorno TBS (TBS. h)
description: O TBS usa os códigos a seguir para indicar o resultado de uma chamada de função.
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369637"
---
# <a name="tbs-return-codes"></a>Códigos de retorno TBS

O TBS usa os códigos a seguir para indicar o resultado de uma chamada de função.



| Constante/valor                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TBS \_ ÊXITO**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | A função foi bem-sucedida.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TBS \_ \_ \_ Erro interno E**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Ocorreu um erro interno de software.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TBS \_ E \_ \_ parâmetro inadequado**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Um ou mais valores de parâmetro não são válidos.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TBS \_ E \_ \_ \_ ponteiro de saída inválido**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Um ponteiro de saída especificado é inadequado.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TBS \_ E \_ \_ contexto inválido**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | O identificador de contexto especificado não se refere a um contexto válido.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TBS \_ E \_ \_ buffer insuficiente**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | O buffer de saída especificado é muito pequeno.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TBS \_ E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Ocorreu um erro ao se comunicar com o TPM.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TBS \_ E \_ \_ \_ parâmetro de contexto inválido**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | Um parâmetro de contexto inválido foi passado ao tentar criar um contexto TBS.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt> </dl>                | O serviço TBS não está em execução e não pôde ser iniciado.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TBS \_ E \_ \_ muitos \_ \_ contextos de TBS**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | Não foi possível criar um novo contexto porque há muitos contextos abertos.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TBS \_ E \_ \_ muitos \_ recursos**</dt> <dt>2150121482 (0x8028400A)</dt> </dl>                   | Não foi possível criar um novo recurso virtual porque há muitos recursos virtuais abertos.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TBS \_ \_Início de serviço E \_ \_ pendente**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | O serviço TBS foi iniciado, mas ainda não está em execução.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TBS \_ \_ \_ Não \_ há suporte para E PPI**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | Não há suporte para a interface de presença física.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TBS \_ \_Comando E \_ cancelado**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | O comando foi cancelado.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TBS \_ E \_ buffer \_ muito \_ grande**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | O buffer de entrada ou saída é muito grande.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TBS \_ E \_ TPM \_ não \_ encontrado**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | Um dispositivo de segurança de Trusted Platform Module (TPM) compatível não pode ser encontrado neste computador.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TBS \_ E \_ serviço \_ desabilitado**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | O serviço TBS foi desabilitado.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TBS \_ E \_ nenhum \_ \_ LOG de eventos**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | O log de eventos TBS não está disponível.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TBS \_ E \_ acesso \_ negado**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | O chamador não tem os direitos apropriados para executar a operação solicitada.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TBS \_ E \_ provisionamento \_ não \_ permitido**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | A ação de provisionamento do TPM não é permitida pelos sinalizadores especificados.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TBS \_ \_Função E \_ PPI \_ sem suporte**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | A interface de presença física deste firmware não oferece suporte ao método solicitado.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TBS \_ E \_ OWNERAUTH \_ não \_ encontrados**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | O valor de OwnerAuth do TPM solicitado não foi encontrado.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TBS \_ E \_ provisionamento \_ incompleto**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | O provisionamento do TPM não foi concluído. Para obter mais informações sobre como concluir o provisionamento, chame o método WMI do [**\_ TPM do Win32**](/windows/desktop/SecProv/win32-tpm) para provisionar o TPM (' Provision ') e verifique as informações retornadas.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>TBS. h</dt> </dl> |



 

