---
title: Códigos de erro do cliente (Winbio \_ err.h)
description: Códigos de erro definidos no arquivo de \_ título Winbio err.h.
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
ms.openlocfilehash: bcb8450b85eaa6c49b66a3a86789c126cc04b9a661a7e4c5074784f8cba6bf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993836"
---
# <a name="client-error-codes"></a>Códigos de erro do cliente

Os códigos de erro a seguir são definidos no arquivo de \_ título Winbio err.h.



| Constante/valor                                                                                                                                                                                                                                                                                         | Descrição                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ E \_ FATOR SEM SUPORTE \_ 0X80098001**</dt> <dt></dt> </dl>                              | Não há suporte para o fator biométrico especificado.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E \_ UNIDADE \_ INVÁLIDA**</dt> <dt>0X80098002</dt> </dl>                                                | O número da ID da unidade não corresponde a um dispositivo biométrico válido.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ \_ ID DESCONHECIDA**</dt> <dt>0x80098003</dt> </dl>                                                      | O exemplo biométrico não é igual a nenhuma identidade conhecida.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ CANCELED**</dt> <dt>0x80098004</dt> </dl>                                                             | A operação biométrica foi cancelada antes de ser concluída.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ NO \_ MATCH**</dt> <dt>0X80098005</dt> </dl>                                                            | O exemplo biométrico não é igual à identidade ou sub-fator especificado.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ E \_ CAPTURE \_ ABORTED**</dt> <dt>0x80098006</dt> </dl>                                       | Não foi possível capturar uma amostra biométrica porque a operação de captura foi anulada.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ E \_ REGISTRO EM ANDAMENTO \_ \_ 0X80098007**</dt> <dt></dt> </dl>                 | Não foi possível iniciar uma transação de registro porque outro registro já está em andamento.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ CAPTURA \_ RUIM**</dt> <dt>0X80098008</dt> </dl>                                                   | O exemplo capturado não pode ser usado para operações biométricas posteriores.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ CÓDIGO DE CONTROLE INVÁLIDO \_ \_ 0X80098009**</dt> <dt></dt> </dl>                       | A unidade biométrica não dá suporte ao código de controle de unidade especificado.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ COLETA DE DADOS E EM ANDAMENTO \_ \_ \_ \_ 0X8009800B**</dt> <dt></dt> </dl> | Uma operação de coleta de dados pendente já está em andamento.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ FORMATO DE DADOS \_ SEM \_**</dt> SUPORTE <dt>0X8009800C</dt> </dl>              | O driver do sensor biométrico não dá suporte ao formato de dados solicitado.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E TIPO DE DADOS SEM SUPORTE \_ \_ \_ 0X8009800D**</dt> <dt></dt> </dl>                    | O driver do sensor biométrico não dá suporte ao tipo de dados solicitado.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ FINALIDADE \_ SEM**</dt> <dt>SUPORTE 0X8009800E</dt> </dl>                           | O driver do sensor biométrico não dá suporte à finalidade de dados solicitada.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ ESTADO DO DISPOSITIVO \_ \_ INVÁLIDO**</dt> <dt>0X8009800F</dt> </dl>                       | A unidade biométrica não está no estado adequado para executar a operação especificada.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ E \_ DISPOSITIVO \_ OCUPADO**</dt> <dt>0X80098010</dt> </dl>                                                   | A operação não pôde ser executada porque o dispositivo de sensor estava ocupado.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NÃO PODE CRIAR \_ \_ 0X80098011**</dt> <dt></dt> </dl>                       | O adaptador de armazenamento não pôde criar um novo banco de dados.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NÃO PODE ABRIR \_ \_ 0X80098012**</dt> <dt></dt> </dl>                             | O adaptador de armazenamento não pôde abrir um banco de dados existente.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NÃO PODE FECHAR \_ \_ 0X80098013**</dt> <dt></dt> </dl>                          | O adaptador de armazenamento não pôde fechar um banco de dados.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ O BANCO \_ DE DADOS E NÃO PODE \_ \_ APAGAR**</dt> <dt>0X80098014</dt> </dl>                          | O adaptador de armazenamento não pôde apagar um banco de dados.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NÃO PODE ENCONTRAR \_ \_ 0X80098015**</dt> <dt></dt> </dl>                             | O adaptador de armazenamento não conseguiu encontrar um banco de dados.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ E \_ DATABASE JÁ EXISTE \_ \_ 0X80098016**</dt> <dt></dt> </dl>              | O adaptador de armazenamento não pôde criar um banco de dados porque o banco de dados especificado já existe.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ FULL**</dt> <dt>0x80098018</dt> </dl>                                             | O adaptador de armazenamento não pôde adicionar um registro ao banco de dados porque o banco de dados está cheio.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ LOCKED**</dt> <dt>0x80098019</dt> </dl>                                       | O banco de dados está bloqueado e seu conteúdo está inacessível.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CORRUPTED**</dt> <dt>0X8009801A</dt> </dl>                              | O conteúdo do banco de dados ficou corrompido e está inacessível.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NÃO TEM ESSE \_ \_ \_ REGISTRO**</dt> <dt>0X8009801B</dt> </dl>             | Nenhum registro foi excluído porque a identidade e o sub-fator especificados não estão presentes no banco de dados.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E \_ \_ DUPLICAR REGISTRO**</dt> <dt>0X8009801C</dt> </dl>                        | A identidade e o sub-fator especificados já estão inscritos no banco de dados.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE READ ERROR \_ \_ 0X8009801D**</dt> <dt></dt> </dl>                          | Ocorreu um erro ao tentar ler do banco de dados.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE WRITE ERROR \_ \_ 0X8009801E**</dt> <dt></dt> </dl>                       | Ocorreu um erro ao tentar gravar no banco de dados.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO RESULTS \_ \_ 0X8009801F**</dt> <dt></dt> </dl>                          | Nenhum registro no banco de dados corresponderam à consulta.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ BANCO DE DADOS E \_ \_ NÃO HÁ MAIS \_ \_ REGISTROS**</dt> <dt>0X80098020</dt> </dl>          | Todos os registros da consulta de banco de dados mais recente foram recuperados.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Uma operação de banco de dados encontrou inesperadamente o final do arquivo.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ E \_ DATABASE BAD INDEX VECTOR \_ \_ \_ 0x80098022**</dt> <dt></dt> </dl>       | Falha em uma operação de banco de dados devido a um vetor de índice malformado.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E \_ \_ BSP**</dt> <dt>incorreto 0x80098024</dt> </dl>                                             | A unidade biométrica não pertence ao provedor de serviços especificado.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E \_ POOL \_ DE \_ SENSOR**</dt> <dt>INCORRETO 0X80098025</dt> </dl>                    | A unidade biométrica não pertence ao pool de sensor especificado.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ NO CAPTURE DATA \_ \_ 0X80098026**</dt> <dt></dt> </dl>                                      | O buffer de captura do adaptador de sensor está vazio.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ MODO \_ DE \_ SENSOR**</dt> INVÁLIDO <dt>0X80098027</dt> </dl>                          | O adaptador de sensor não dá suporte ao modo de sensor especificado na configuração.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ E \_ LOCK \_ VIOLATION**</dt> <dt>0X8009802A</dt> </dl>                                          | A operação solicitada não pode ser executada devido a um conflito de bloqueio.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ \_ DUPLICAR MODELO**</dt> <dt>0X8009802B</dt> </dl>                              | Os dados em um modelo biométrico corresponde aos de outro modelo já no banco de dados.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ INVALID \_ OPERATION**</dt> <dt>0X8009802C</dt> </dl>                                 | A operação solicitada não é válida para o estado atual da sessão ou da unidade biométrica.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ E \_ SESSION \_ BUSY**</dt> <dt>0X8009802D</dt> </dl>                                                | A sessão não pode iniciar uma nova operação porque outra operação já está em andamento.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ DISABLED**</dt> <dt>0x80098030</dt> </dl>                             | As configurações de política do sistema desabilitam o provedor de credenciais biométricas.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ NO CREDENTIAL \_ 0X80098031**</dt> <dt></dt> </dl>             | A credencial solicitada não foi encontrada.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ DISABLED**</dt> <dt>0x80098032</dt> </dl>                                                             | As configurações de política do sistema desabilitam o serviço biométrico.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ FALHA \_ DE \_ CONFIGURAÇÃO**</dt> <dt>E 0X80098033</dt> </dl>                     | Não foi possível configurar a unidade biométrica.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ SENSOR E \_ \_ INDISPONÍVEL**</dt> <dt>0x80098034</dt> </dl>                              | Não é possível criar um pool privado porque uma ou mais unidades biométricas não estão disponíveis.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ E \_ SAS \_ HABILITADO para**</dt> <dt>0x80098035</dt> </dl>                                                   | Uma sequência de atenção segura (CTRL-ALT-DELETE) é necessária para logon.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ FALHA \_ \_ DO**</dt> <dt>DISPOSITIVO E 0X80098036</dt> </dl>                                          | Um sensor biométrico falhou.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ E FAST \_ \_ OPÇÃO DE USUÁRIO \_ \_ DESABILITADA**</dt> <dt>0x80098037</dt> </dl>       | >a alternação rápida de usuário está desabilitada.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ NOT \_ ACTIVE \_ CONSOLE**</dt> <dt>0X80098038</dt> </dl>                             | O pool de sensor do sistema não pode ser aberto nas sessões de cliente do Servidor de Terminal.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ E \_ EVENT \_ MONITOR \_ ACTIVE**</dt> <dt>0x80098039</dt> </dl>                      | Já existe um monitor de eventos ativo associado à sessão especificada.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ TIPO DE PROPRIEDADE INVÁLIDO \_ \_ 0X8009803A**</dt> <dt></dt> </dl>                    | O valor especificado não é um tipo de propriedade válido.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ ID DE PROPRIEDADE INVÁLIDA**</dt> <dt>0X8009803B</dt> </dl>                          | O valor especificado não é uma ID de propriedade válida.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E \_ PROPRIEDADES \_ SEM SUPORTE**</dt> <dt>0X8009803C</dt> </dl>                        | A unidade biométrica não dá suporte à propriedade especificada.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ FALHA \_ DE \_ INTEGRIDADE \_ DO**</dt> ADAPTADOR E <dt>0X8009803D</dt> </dl>        | O adaptador não passou na verificação de integridade.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ MORE \_ DATA**</dt> <dt>0X00090001</dt> </dl>                                                         | Outro exemplo é necessário para o modelo de registro atual.<br/>                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ err.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





