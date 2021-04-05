---
title: Códigos de erro do cliente (WinBio \_ Err. h)
description: Códigos de erro definidos no \_ arquivo de cabeçalho WinBio Err. h.
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 000723612a2f7f9f5575fc767924d4d6c697468a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009672"
---
# <a name="client-error-codes"></a>Códigos de erro do cliente

Os códigos de erro a seguir são definidos no \_ arquivo de cabeçalho WinBio Err. h.



| Constante/valor                                                                                                                                                                                                                                                                                         | Descrição                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ 0x80098001 de \_ \_ fator E sem suporte**</dt> <dt></dt> </dl>                              | Não há suporte para o fator biométrico especificado.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E 0x80098002 de \_ \_ unidade inválido**</dt> <dt></dt> </dl>                                                | O número de ID de unidade não corresponde a um dispositivo biométrico válido.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ \_ ID**</dt> <dt>0x80098003</dt> desconhecida </dl>                                                      | O exemplo biométrico não corresponde a nenhuma identidade conhecida.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ cancelado**</dt> <dt>0x80098004</dt> </dl>                                                             | A operação biométrica foi cancelada antes de ser concluída.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ sem \_ correspondência**</dt> <dt>0x80098005</dt> </dl>                                                            | O exemplo biométrico não corresponde à identidade ou ao subfator especificado.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ E & 0x80098006 de \_ captura \_ anulada**</dt> <dt></dt> </dl>                                       | Um exemplo biométrico não pôde ser capturado porque a operação de captura foi anulada.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ \_Registro E \_ em \_ andamento**</dt> <dt>0x80098007</dt> </dl>                 | Uma transação de registro não pôde ser iniciada porque outro registro já está em andamento.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E 0x80098008 de \_ \_ captura inadequada**</dt> <dt></dt> </dl>                                                   | O exemplo capturado não pode ser usado para outras operações biométricas.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ código de controle inválido**</dt> <dt>0x80098009</dt> </dl>                       | A unidade biométrica não dá suporte ao código de controle de unidade especificado.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ \_ \_ Coleta de dados E \_ em \_ andamento**</dt> <dt>0x8009800B</dt> </dl> | Uma operação de coleta de dados pendente já está em andamento.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ formato de dados sem suporte**</dt> <dt>0x8009800C</dt> </dl>              | O driver do sensor biométrico não oferece suporte ao formato de dados solicitado.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ tipo de dados sem suporte**</dt> <dt>0x8009800D</dt> </dl>                    | O driver do sensor biométrico não oferece suporte ao tipo de dados solicitado.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E 0x8009800E de \_ \_ finalidade sem suporte**</dt> <dt></dt> </dl>                           | O driver do sensor biométrico não oferece suporte à finalidade de dados solicitada.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ estado de dispositivo inválido**</dt> <dt>0x8009800F</dt> </dl>                       | A unidade biométrica não está no estado adequado para executar a operação especificada.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ E \_ dispositivo \_ ocupado**</dt> <dt>0x80098010</dt> </dl>                                                   | A operação não pôde ser executada porque o dispositivo de sensor estava ocupado.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ E o \_ banco de dados não \_ consegue \_ criar**</dt> <dt>0x80098011</dt> </dl>                       | O adaptador de armazenamento não pôde criar um novo banco de dados.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ O \_ banco de dados E não \_ \_ abre**</dt> <dt>0x80098012</dt> </dl>                             | O adaptador de armazenamento não pôde abrir um banco de dados existente.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E o \_ banco de dados não \_ consegue \_ fechar**</dt> <dt>0x80098013</dt> </dl>                          | O adaptador de armazenamento não pôde fechar um banco de dados.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ O \_ banco de dados E não \_ consegue \_ apagar**</dt> <dt>0x80098014</dt> </dl>                          | O adaptador de armazenamento não conseguiu apagar um banco de dados.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ O \_ banco de dados E não \_ consegue \_ Localizar**</dt> <dt>0x80098015</dt> </dl>                             | O adaptador de armazenamento não conseguiu localizar um banco de dados.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ O \_ banco de dados \_ já \_ existe**</dt> <dt>0x80098016</dt> </dl>              | O adaptador de armazenamento não pôde criar um banco de dados porque o banco de dados especificado já existe.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ \_Banco de dados \_ completo do E**</dt> <dt>0x80098018</dt> </dl>                                             | O adaptador de armazenamento não pôde adicionar um registro ao banco de dados porque o banco de dados está cheio.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ banco de dados \_ bloqueado**</dt> <dt>0x80098019</dt> </dl>                                       | O banco de dados está bloqueado e seu conteúdo está inacessível.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ \_Banco de dados 0x8009801A \_ corrompido**</dt> <dt></dt> </dl>                              | O conteúdo do banco de dados ficou corrompido e está inacessível.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ \_Banco de dados \_ sem \_ tal \_ registro**</dt> <dt>0x8009801B</dt> </dl>             | Nenhum registro foi excluído porque a identidade e o subfatos especificados não estão presentes no banco de dados.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E 0x8009801C de \_ \_ registro duplicados**</dt> <dt></dt> </dl>                        | A identidade e o subfator especificados já estão registrados no banco de dados.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E 0x8009801D de \_ \_ \_ erro de leitura do banco de dados**</dt> <dt></dt> </dl>                          | Ocorreu um erro ao tentar ler do banco de dados.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ E & 0x8009801E de \_ \_ \_ erro de gravação do banco de dados**</dt> <dt></dt> </dl>                       | Ocorreu um erro ao tentar gravar no banco de dados.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ \_Banco de dados \_ sem \_ resultados**</dt> <dt>0x8009801F</dt> </dl>                          | Nenhum registro no banco de dados correspondeu à consulta.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ \_Banco de dados E \_ não há \_ mais \_ registros**</dt> <dt>0x80098020</dt> </dl>          | Todos os registros da consulta de banco de dados mais recente foram recuperados.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ banco de dados \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Uma operação de banco de dados encontrou inesperadamente o final do arquivo.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ \_Banco de dados 0x80098022 \_ \_ \_ vetor de índice inadequado**</dt> <dt></dt> </dl>       | Falha em uma operação de banco de dados devido a um vetor de índice malformado.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E \_ 0x80098024 \_ BSP incorreto**</dt> <dt></dt> </dl>                                             | A unidade biométrica não pertence ao provedor de serviços especificado.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ pool de sensor incorreto**</dt> <dt>0x80098025</dt> </dl>                    | A unidade biométrica não pertence ao pool de sensores especificado.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ nenhum \_ \_**</dt> <dt>0x80098026</dt> de dados de captura </dl>                                      | O buffer de captura do adaptador do sensor está vazio.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ modo de sensor inválido**</dt> <dt>0x80098027</dt> </dl>                          | O adaptador do sensor não oferece suporte ao modo de sensor especificado na configuração.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ E \_ & \_**</dt> <dt>0x8009802A</dt> de violação de bloqueio </dl>                                          | A operação solicitada não pode ser executada devido a um conflito de bloqueio.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E 0x8009802B de \_ \_ modelo duplicados**</dt> <dt></dt> </dl>                              | Os dados em um modelo biométrico correspondem aos de outro modelo que já está no banco de dado.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ \_ operação inválida**</dt> <dt>0x8009802C</dt> </dl>                                 | A operação solicitada não é válida para o estado atual da sessão ou da unidade biométrica.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ 0x8009802D de \_ sessão E \_ ocupada**</dt> <dt></dt> </dl>                                                | A sessão não pode iniciar uma nova operação porque outra operação já está em andamento.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ cred \_ Prov \_ desabilitou**</dt> <dt>0x80098030</dt> </dl>                             | As configurações de política do sistema desabilitaram o provedor de credenciais biométricas.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ cred \_ Prov \_ sem \_ credencial**</dt> <dt>0x80098031</dt> </dl>             | A credencial solicitada não foi encontrada.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ desabilitado**</dt> <dt>0x80098032</dt> </dl>                                                             | As configurações de política do sistema desabilitaram o serviço biométrico.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ \_ \_ Falha na configuração do E**</dt> <dt>0x80098033</dt> </dl>                     | Não foi possível configurar a unidade biométrica.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ \_Sensor E \_ indisponível**</dt> <dt>0x80098034</dt> </dl>                              | Não é possível criar um pool privado porque uma ou mais unidades biométricas não estão disponíveis.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ E \_ SAS \_ habilitados**</dt> <dt>0x80098035</dt> </dl>                                                   | Uma sequência de atenção segura (CTRL-ALT-DELETE) é necessária para o logon.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ 0x80098036 \_ de \_ falha do dispositivo**</dt> <dt></dt> </dl>                                          | Um sensor biométrico falhou.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ \_ \_ Comutador de usuário rápido 0x80098037 \_ \_ desabilitado**</dt> <dt></dt> </dl>       | >a troca rápida de usuário está desabilitada.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ não 0x80098038 de \_ \_ console ativo**</dt> <dt></dt> </dl>                             | O pool do sensor do sistema não pode ser aberto de Terminal Server sessões de cliente.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ \_Monitor de evento E \_ \_ ativo**</dt> <dt>0x80098039</dt> </dl>                      | Já existe um monitor de eventos ativo associado à sessão especificada.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ tipo de propriedade inválido**</dt> <dt>0x8009803A</dt> </dl>                    | O valor especificado não é um tipo de propriedade válido.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ ID de propriedade inválida**</dt> <dt>0x8009803B</dt> </dl>                          | O valor especificado não é uma ID de propriedade válida.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E 0x8009803C de \_ \_ Propriedade sem suporte**</dt> <dt></dt> </dl>                        | A unidade biométrica não oferece suporte à propriedade especificada.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ \_Falha de \_ integridade \_ do adaptador E**</dt> <dt>0x8009803D</dt> </dl>        | O adaptador não passou na verificação de integridade.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ \_ \_ Mais**</dt> <dt>0x00090001</dt> de dados </dl>                                                         | Outra amostra é necessária para o modelo de registro atual.<br/>                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Err. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





