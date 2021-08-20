---
description: Descreve os códigos de erro 1000-1299 definidos no arquivo de título WinError.h e destina-se a desenvolvedores.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Códigos de erro do sistema (1000-1299) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: dfda2e29a6b75acd683842509229f3bc52d7e8d3599855b01d8376f5a7daf2ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076330"
---
# <a name="system-error-codes-1000-1299"></a>Códigos de erro do sistema (1000-1299)

> [!NOTE]
> Essas informações são destinadas a desenvolvedores que depuram erros do sistema. Para outros erros, como problemas com Windows Atualização, há uma lista de recursos na [página Códigos de](system-error-codes.md) erro.

A lista a seguir descreve [os códigos de](system-error-codes.md) erro do sistema para erros de 1000 a 1299. Eles são retornados pela [**função GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a [**função FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com o **sinalizador FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ESTOURO \_ DE PILHA \_ DE ERROS**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Recursão muito profunda; a pilha estourou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**MENSAGEM \_ INVÁLIDA \_ DE ERRO**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



A janela não pode agir na mensagem enviada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**O \_ ERRO NÃO PODE SER \_ \_ CONCLUÍDO**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Não é possível concluir essa função.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**SINALIZADORES \_ \_ INVÁLIDOS DE ERRO**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Sinalizadores inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERRO \_ VOLUME NÃO REGISTRADO \_**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



O volume não contém um sistema de arquivos reconhecido. Verifique se todos os drivers necessários do sistema de arquivos estão carregados e se o volume não está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ARQUIVO \_ DE \_ ERRO INVÁLIDO**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



O volume de um arquivo foi alterado externamente para que o arquivo aberto não seja mais válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**MODO \_ DE TELA INTEIRA DE \_ ERRO**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



A operação solicitada não pode ser executada no modo de tela inteira.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERRO \_ NENHUM \_ TOKEN**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Foi feita uma tentativa de referenciar um token que não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERRO \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



O banco de dados do Registro de configuração está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERRO \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



A chave do Registro de configuração é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERRO \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Não foi possível abrir a chave do Registro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERRO \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (0x3F4)
</dt> <dt>



Não foi possível ler a chave do Registro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERRO \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



Não foi possível escrever a chave do Registro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**REGISTRO \_ DE ERRO \_ RECUPERADO**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Um dos arquivos no banco de dados do Registro precisava ser recuperado com o uso de um log ou cópia alternativa. A recuperação foi bem-sucedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**REGISTRO \_ DE \_ ERRO CORROMPIDO**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



O registro está corrompido. A estrutura de um dos arquivos que contém dados do Registro está corrompida ou a imagem de memória do sistema do arquivo está corrompida ou o arquivo não pôde ser recuperado porque a cópia ou o log alternativo estava ausente ou corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**FALHA \_ NA \_ E/S DO REGISTRO \_ DE ERRO**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Uma operação de E/S iniciada pelo Registro falhou irrecuperavelmente. O Registro não pôde ler, gravar ou liberar um dos arquivos que contêm a imagem do sistema do Registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERRO \_ NÃO ARQUIVO DO \_ \_ REGISTRO**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



O sistema tentou carregar ou restaurar um arquivo no Registro, mas o arquivo especificado não está em um formato de arquivo do Registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**CHAVE \_ DE \_ ERRO EXCLUÍDA**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Operação ilegal tentada em uma chave do Registro que foi marcada para exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERRO \_ SEM ESPAÇO DE \_ \_ LOG**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



O sistema não pôde alocar o espaço necessário em um log do Registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**A \_ CHAVE DE ERRO TEM \_ \_ FILHOS**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



Não é possível criar um link simbólico em uma chave do Registro que já tenha sub-chaves ou valores.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**O \_ FILHO DE ERRO DEVE SER \_ \_ \_ VOLÁTIL**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Não é possível criar uma sub-chave estável sob uma chave pai volátil.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERRO \_ NOTIFY \_ ENUM \_ DIR**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Uma solicitação de alteração de notificação está sendo concluída e as informações não estão sendo retornadas no buffer do chamador. O chamador agora precisa enumerar os arquivos para encontrar as alterações.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**SERVIÇOS \_ DEPENDENTES \_ DE ERRO EM \_ EXECUÇÃO**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Um controle de parada foi enviado a um serviço do quais outros serviços em execução dependem.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERRO \_ CONTROLE DE SERVIÇO \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



O controle solicitado não é válido para esse serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**TEMPO DE TEMPO DE \_ \_ \_ SOLICITAÇÃO DO SERVIÇO DE ERRO**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



O serviço não respondeu à solicitação de início ou de controle em um tempo oportuno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**SERVIÇO \_ DE ERRO SEM \_ \_ THREAD**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Não foi possível criar um thread para o serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**BANCO DE \_ DADOS DO SERVIÇO DE ERRO \_ \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



O banco de dados de serviço está bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**SERVIÇO \_ DE ERRO JÁ EM \_ \_ EXECUÇÃO**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Uma instância do serviço já está em execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERRO \_ CONTA DE SERVIÇO \_ \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



O nome da conta é inválido ou não existe ou a senha é inválida para o nome da conta especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**serviço de erro \_ \_ desabilitado**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Não é possível iniciar o serviço porque ele está desabilitado ou porque não há dispositivos habilitados associados a ele.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_dependência circular de erro \_**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



A dependência de serviço circular foi especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**o serviço de erro não \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



O serviço especificado não existe como um serviço instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**o \_ serviço de erro \_ não pode \_ aceitar \_ Ctrl**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



O serviço não pode aceitar mensagens de controle no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**serviço de erro \_ \_ não \_ ativo**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



O serviço não foi iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERRO \_ falha \_ ao \_ conectar o controlador de serviço \_**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



O processo de serviço não pôde se conectar ao controlador de serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_exceção \_ de erro no \_ serviço**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Ocorreu uma exceção no serviço ao manipular a solicitação de controle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**\_o banco de dados de erro \_ \_ não \_ existe**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



O banco de dados especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**\_ \_ erro específico do serviço de erro \_**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



O serviço retornou um código de erro específico do serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**processo de erro \_ \_ anulado**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



O processo foi finalizado inesperadamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**\_ \_ falha na dependência do serviço de erro \_**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



Falha ao iniciar o serviço ou grupo de dependência.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**\_ \_ falha no logon do serviço de erro \_**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



O serviço não foi iniciado devido a uma falha de logon.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**\_falha ao \_ iniciar o serviço de erro \_**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



Depois de iniciar, o serviço foi suspenso em um estado de início pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERRO \_ de \_ bloqueio de serviço inválido \_**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



O bloqueio do banco de dados do serviço especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_serviço \_ de erro marcado \_ para \_ exclusão**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



O serviço especificado foi marcado para exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**o \_ serviço de erro \_ existe**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



O serviço especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERRO \_ já \_ em execução \_ LKG**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



O sistema está em execução no momento com a última configuração válida conhecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dependência de serviço de erro \_ \_ \_ excluída**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



O serviço de dependência não existe ou foi marcado para exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERRO de \_ inicialização \_ já \_ aceita**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



A inicialização atual já foi aceita para uso como o último conjunto de controle mais conhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**serviço de erro \_ \_ nunca \_ iniciado**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



Nenhuma tentativa de iniciar o serviço foi feita desde a última inicialização.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERRO \_ de \_ nome de serviço duplicado \_**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



O nome já está em uso como um nome de serviço ou um nome de exibição de serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERRO \_ de \_ conta de serviço diferente \_**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



A conta especificada para esse serviço é diferente da conta especificada para outros serviços em execução no mesmo processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERRO \_ não é possível \_ detectar \_ falha do driver \_**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



As ações de falha só podem ser definidas para serviços Win32, não para drivers.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERRO \_ não é possível \_ detectar a \_ \_ anulação do processo**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Esse serviço é executado no mesmo processo que o Gerenciador de controle de serviço. Portanto, o Gerenciador de controle de serviço não poderá tomar medidas se o processo desse serviço for encerrado inesperadamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERRO \_ sem \_ programa de recuperação \_**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



Nenhum programa de recuperação foi configurado para este serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**\_serviço \_ de erro não está \_ no \_ exe**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



O programa executável em que esse serviço está configurado para ser executado não implementa o serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERRO \_ não é um \_ serviço de inicialização segura \_**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



este serviço não pode ser iniciado no modo de Cofre.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERRO ao \_ fim \_ da \_ mídia**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



A extremidade física da fita foi atingida.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**marca de caixa de erro \_ \_ detectada**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



Um acesso à fita atingiu uma marca de um.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERRO no \_ início \_ da \_ mídia**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



O início da fita ou de uma partição foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERRO \_ setmark \_ detectado**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



Um acesso à fita atingiu o final de um conjunto de arquivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERRO \_ nenhum \_ dado \_ detectado**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



Não há mais dados na fita.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**\_falha na partição de erro \_**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



Não foi possível particionar a fita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERRO \_ de \_ comprimento de bloco inválido \_**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Ao acessar uma nova fita de uma partição multivolume, o tamanho atual do bloco está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**dispositivo de erro \_ \_ não \_ particionado**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Não foi possível encontrar informações de partição de fita ao carregar uma fita.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERRO \_ não é possível \_ \_ Bloquear \_ mídia**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Não é possível bloquear o mecanismo de ejeção de mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERRO \_ não é possível \_ \_ descarregar a \_ mídia**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Não é possível descarregar a mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**mídia de erro \_ \_ alterada**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



A mídia na unidade pode ter sido alterada.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**redefinição de barramento de erro \_ \_**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



O barramento de e/s foi redefinido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERRO \_ sem \_ mídia \_ na \_ unidade**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Nenhuma mídia na unidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERRO \_ sem \_ \_ tradução Unicode**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



Não existe mapeamento para o caractere Unicode na página de código de vários bytes de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**\_ \_ falha na inicialização da DLL de erro \_**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Falha em uma rotina de inicialização da biblioteca de vínculo dinâmico (DLL).


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERRO \_ de desligamento \_ em \_ andamento**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



Um desligamento do sistema está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERRO \_ nenhum \_ desligamento \_ em \_ andamento**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



Não é possível anular o desligamento do sistema porque nenhum desligamento estava em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**\_dispositivo de e/s de erro \_**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



Não foi possível executar a solicitação devido a um erro de dispositivo de E/S.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERRO de \_ serial \_ sem \_ dispositivo**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



Nenhum dispositivo serial foi inicializado com êxito. O driver serial será descarregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERRO de \_ IRQ \_ ocupado**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



Não é possível abrir um dispositivo que estava compartilhando uma solicitação de interrupção (IRQ) com outros dispositivos. Pelo menos um outro dispositivo que usa esse IRQ já foi aberto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERRO \_ mais \_ gravações**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Uma operação de e/s serial foi concluída por outra gravação na porta serial. O \_ contador serial \_ XOFF do IOCTL \_ atingiu zero.)


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_tempo limite do contador de erros \_**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Uma operação de e/s serial foi concluída porque o período de tempo limite expirou. O contador de IOCTL \_ serial \_ XOFF \_ não alcançou zero.)


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**marca de ID do disquete de erro \_ \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



Nenhuma marca de endereço de ID encontrada no disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERRO de \_ cilindro de disquete \_ incorreto \_**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Incompatibilidade entre o campo ID de setor de disquete e o endereço de rastreamento do controlador de disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**\_ \_ erro desconhecido no disquete de erros \_**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



O controlador de disquete relatou um erro que não é reconhecido pelo driver de disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**\_ \_ registros inválidos de disquete de erros \_**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



O controlador de disquete retornou resultados inconsistentes em seus registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**\_ \_ falha ao recalibrar disco de erro \_**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Ao acessar o disco rígido, uma operação de recalibração falhou, mesmo após novas tentativas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**\_ \_ falha na operação de disco de erro \_**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Ao acessar o disco rígido, uma operação de disco falhou mesmo após novas tentativas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERRO \_ \_ ao redefinir disco \_ com falha**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Ao acessar o disco rígido, uma redefinição de controlador de disco era necessária, mas mesmo que falhou.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**\_estouro de eom de erro \_**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Foi encontrado o final físico da fita.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERRO \_ \_ insuficiente \_ na \_ memória do servidor**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



não há armazenamento suficiente de servidor disponível para processar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERRO \_ possível \_ deadlock**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



Foi detectada uma possível condição de deadlock.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_alinhamento mapeado de erro \_**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



O endereço base ou o deslocamento do arquivo especificado não tem o alinhamento adequado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERRO \_ definir o \_ estado de energia \_ \_ vetado**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Uma tentativa de alterar o estado de energia do sistema foi vetada por outro aplicativo ou driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERRO \_ ao definir o \_ estado de energia \_ \_**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



O BIOS do sistema falhou ao tentar alterar o estado de energia do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERRO \_ de \_ muitos \_ links**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



Foi feita uma tentativa de criar mais links em um arquivo do que o sistema de arquivos dá suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERRO \_ de \_ versão antiga do Win \_**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



O programa especificado requer uma versão mais recente do Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**\_ \_ sistema operacional incorreto do aplicativo de erro \_**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



O programa especificado não é um programa do Windows ou do MS-DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERRO \_ DE APLICATIVO DE INSTÂNCIA \_ \_ ÚNICA**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Não é possível iniciar mais de uma instância do programa especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERRO \_ APLICATIVO RMODE \_**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



O programa especificado foi escrito para uma versão anterior do Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERRO \_ \_ DLL INVÁLIDA**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Um dos arquivos de biblioteca necessários para executar esse aplicativo está danificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERRO \_ SEM \_ ASSOCIAÇÃO**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Nenhum aplicativo está associado ao arquivo especificado para essa operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERRO \_ DE DDE \_ FALHA**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Ocorreu um erro ao enviar o comando para o aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_DLL DE ERRO \_ NÃO \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Um dos arquivos de biblioteca necessários para executar esse aplicativo não pode ser encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERRO \_ SEM \_ MAIS \_ ALÇAS DE \_ USUÁRIO**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



O processo atual usou todas as suas provisões do sistema de alças para objetos do Gerenciador de Janelas.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**SOMENTE \_ SINCRONIZAÇÃO \_ DE MENSAGEM DE \_ ERRO**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



A mensagem só pode ser usada com operações síncronas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ELEMENTO \_ ERROR SOURCE \_ \_ EMPTY**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



O elemento de origem indicado não tem nenhuma mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ELEMENTO \_ ERROR DESTINATION \_ \_ FULL**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



O elemento de destino indicado já contém mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ENDEREÇO \_ DO ELEMENTO ERROR ILLEGAL \_ \_**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



O elemento indicado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR \_ MAGAZINE \_ NÃO \_ PRESENTE**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



O elemento indicado faz parte de uma revisa que não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**REINICIALIZAÇÃO \_ DE DISPOSITIVO DE ERRO \_ \_ NECESSÁRIA**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



O dispositivo indicado requer reinicialização devido a erros de hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**O DISPOSITIVO \_ DE \_ ERRO REQUER \_ LIMPEZA**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



O dispositivo indicou que a limpeza é necessária antes que outras operações sejam tentadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERRO \_ PORTA DO DISPOSITIVO \_ \_ ABERTA**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



O dispositivo indicou que sua porta está aberta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**DISPOSITIVO \_ DE ERRO NÃO \_ \_ CONECTADO**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



O dispositivo não está conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERRO \_ NÃO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Elemento não encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR \_ NO \_ MATCH**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Não houve nenhuma combinação para a chave especificada no índice.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**CONJUNTO \_ DE ERROS NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



O conjunto de propriedades especificado não existe no objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**PONTO \_ DE ERRO NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



O ponto passado para GetMouseMovePoints não está no buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERRO \_ SEM SERVIÇO DE \_ \_ ACOMPANHAMENTO**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



O serviço de acompanhamento (estação de trabalho) não está em execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERRO \_ NENHUMA \_ \_ ID DE VOLUME**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



Não foi possível encontrar a ID do volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERRO \_ NÃO É POSSÍVEL REMOVER \_ \_ \_ SUBSTITUÍDO**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Não é possível remover o arquivo a ser substituído.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERRO \_ NÃO É POSSÍVEL MOVER A \_ \_ \_ SUBSTITUIÇÃO**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Não é possível mover o arquivo de substituição para o arquivo a ser substituído. O arquivo a ser substituído retido seu nome original.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERRO \_ NÃO É POSSÍVEL MOVER A SUBSTITUIÇÃO \_ \_ \_ \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Não é possível mover o arquivo de substituição para o arquivo a ser substituído. O arquivo a ser substituído foi renomeado usando o nome do backup.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**EXCLUSÃO \_ DE DIÁRIO DE ERRO EM \_ \_ \_ ANDAMENTO**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



O diário de alteração de volume está sendo excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**DIÁRIO \_ DE ERRO NÃO \_ \_ ATIVO**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



O diário de alteração de volume não está ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ARQUIVO \_ POTENCIAL DE ERRO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



Um arquivo foi encontrado, mas pode não ser o arquivo correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ENTRADA \_ DE DIÁRIO DE ERRO \_ \_ EXCLUÍDA**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



A entrada de diário foi excluída do diário.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**O \_ DESLIGAMENTO DE ERRO ESTÁ \_ \_ AGENDADO**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Um desligamento do sistema já foi agendado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**USUÁRIOS \_ DE DESLIGAMENTO DE ERRO \_ \_ \_ CONECTADOS**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



O desligamento do sistema não pode ser iniciado porque há outros usuários conectados ao computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERRO \_ DE DISPOSITIVO \_ RUIM**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



O nome do dispositivo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**\_ \_ INDISPONIBILIDADE DE CONEXÃO DE ERRO**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



O dispositivo não está conectado no momento, mas é uma conexão lembrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**DISPOSITIVO \_ DE ERRO JÁ \_ \_ LEMBRADO**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



O nome do dispositivo local tem uma conexão lembrada com outro recurso de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERRO \_ SEM NET OU CAMINHO \_ \_ \_ \_ RUIM**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



O caminho de rede foi digitado incorretamente, não existe ou o provedor de rede não está disponível no momento. Tente reatipar o caminho ou entre em contato com o administrador de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**PROVEDOR \_ DE ERRO \_ RUIM**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



O nome do provedor de rede especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERRO \_ NÃO É POSSÍVEL ABRIR O \_ \_ PERFIL**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Não é possível abrir o perfil de conexão de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**PERFIL \_ DE ERRO \_ RUIM**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



O perfil de conexão de rede está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERRO \_ NÃO \_ CONTÊINER**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Não é possível enumerar um não retentor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERRO \_ ESTENDIDO \_ ERRO**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Ocorreu um erro estendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERRO \_ \_ GROUPNAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



O formato do nome do grupo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERRO \_ \_ COMPUTERNAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



O formato do nome do computador especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERRO \_ \_ EVENTNAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



O formato do nome do evento especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERRO \_ \_ DOMAINNAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



O formato do nome de domínio especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERRO \_ \_ SERVICENAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



O formato do nome do serviço especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERRO \_ \_ NETNAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



O formato do nome de rede especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERRO \_ \_ SHARENAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



O formato do nome do compartilhamento especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERRO \_ \_ PASSWORDNAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



O formato da senha especificada é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERRO \_ \_ MESSAGENAME INVÁLIDO**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



O formato do nome da mensagem especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERRO \_ \_ MESSAGEDEST INVÁLIDO**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



O formato do destino da mensagem especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**CONFLITO \_ DE \_ CREDENCIAL DE SESSÃO DE \_ ERRO**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



Várias conexões com um servidor ou recurso compartilhado pelo mesmo usuário, usando mais de um nome de usuário, não são permitidas. Desconecte todas as conexões anteriores com o servidor ou o recurso compartilhado e tente novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERRO \_ LIMITE DE SESSÃO REMOTA \_ \_ \_ EXCEDIDO**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



Foi feita uma tentativa de estabelecer uma sessão com um servidor de rede, mas já há muitas sessões estabelecidas para esse servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR \_ DUP \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



O grupo de trabalho ou o nome de domínio já está em uso por outro computador na rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERRO \_ SEM \_ REDE**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



A rede não está presente ou não foi iniciada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERRO \_ CANCELADO**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



A operação foi cancelada pelo usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ARQUIVO \_ \_ MAPEADO PELO USUÁRIO DE \_ ERRO**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



A operação solicitada não pode ser executada em um arquivo com uma seção mapeada pelo usuário aberta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**CONEXÃO \_ DE \_ ERRO RECUSADA**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



O computador remoto recusou a conexão de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERRO \_ DE DESCONEXÃO \_ NORMALMENTE**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



A conexão de rede foi fechada normalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ENDEREÇO \_ DE ERRO JÁ \_ \_ ASSOCIADO**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



O ponto de extremidade de transporte de rede já tem um endereço associado a ele.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ENDEREÇO \_ DE ERRO NÃO \_ \_ ASSOCIADO**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Um endereço ainda não foi associado ao ponto de extremidade de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**CONEXÃO \_ DE \_ ERRO INVÁLIDA**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Foi tentada uma operação em uma conexão de rede inexistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**CONEXÃO \_ DE \_ ERRO ATIVA**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Foi tentada uma operação inválida em uma conexão de rede ativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**REDE \_ DE \_ ERRO INACESSÍVEL**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



O local da rede não pode ser alcançado. Para obter informações sobre a solução de problemas de rede, consulte Windows Ajuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**HOST \_ DE \_ ERRO INACESSÍVEL**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



O local da rede não pode ser alcançado. Para obter informações sobre a solução de problemas de rede, consulte Windows Ajuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**PROTOCOLO \_ DE \_ ERRO INACESSÍVEL**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



O local de rede não pode ser acessado. para obter informações sobre solução de problemas de rede, consulte Windows ajuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**porta de erro \_ \_ inacessível**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



Nenhum serviço está operando no ponto de extremidade de rede de destino no sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**solicitação de erro \_ \_ anulada**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



A solicitação foi anulada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERRO de \_ conexão \_ anulada**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



A conexão de rede foi anulada pelo sistema local.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERRO de \_ repetição**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



Não foi possível concluir a operação. Uma nova tentativa deve ser executada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_limite de \_ contagem de conexão de erro \_**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



Não foi possível estabelecer uma conexão com o servidor porque o limite do número de conexões simultâneas para esta conta foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERRO \_ de \_ restrição de tempo de logon \_**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Tentando fazer logon durante uma hora não autorizada do dia para esta conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERRO \_ de \_ restrição de WKSTA de logon \_**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



A conta não está autorizada a fazer logon nesta estação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERRO \_ de \_ endereço incorreto**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



O endereço de rede não pôde ser usado para a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERRO \_ já \_ registrado**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



O serviço já está registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**serviço de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



O serviço especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERRO \_ não \_ autenticado**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



A operação que está sendo solicitada não foi executada porque o usuário não foi autenticado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERRO \_ não \_ conectado \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



A operação que está sendo solicitada não foi executada porque o usuário não fez logon na rede. O serviço especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERRO de \_ continuação**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Continue com o trabalho em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERRO \_ já \_ inicializado**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



Foi feita uma tentativa de executar uma operação de inicialização quando a inicialização já foi concluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERRO \_ não há \_ mais \_ dispositivos**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



Não há mais dispositivos locais.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERRO \_ sem \_ esse \_ site**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



O site especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERRO \_ o \_ controlador de domínio \_ existe**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Já existe um controlador de domínio com o nome especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERRO \_ somente \_ se \_ conectado**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Esta operação só tem suporte quando você está conectado ao servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERRO ao \_ substituir \_ noChanges**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



A estrutura de diretiva de grupo deve chamar a extensão mesmo se não houver nenhuma alteração.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERRO \_ de \_ perfil de usuário insatisfatório \_**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



O usuário especificado não tem um perfil válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERRO \_ sem \_ suporte \_ no \_ SBS**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



não há suporte para esta operação em um computador que executa o Windows server 2003 para Small Business server.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERRO \_ \_ de desligamento \_ do servidor em \_ andamento**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



A máquina do servidor está sendo desligada.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERRO ao \_ hospedar \_**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



O sistema remoto não está disponível. para obter informações sobre solução de problemas de rede, consulte Windows ajuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERRO de \_ Sid de não \_ conta \_**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



O identificador de segurança fornecido não é de um domínio de conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERRO \_ não \_ Sid de domínio \_**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



O identificador de segurança fornecido não tem um componente de domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**bloco de erro \_ APPHELP \_**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



Caixa de diálogo AppHelp cancelada, impedindo o início do aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERRO \_ \_ de acesso desabilitado \_ pela \_ política**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Este programa está bloqueado pela política de grupo. Para obter mais informações, contate o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERRO \_ reg \_ de \_ consumo NAT**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Um programa tentou usar um valor de registro inválido. Normalmente causado por um registro não inicializado. Esse erro é específico do Itanium.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERRO \_ CSCSHARE \_ offline**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



O compartilhamento está offline no momento ou não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**\_falha de PKINIT de erro \_**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



O protocolo Kerberos encontrou um erro ao validar o certificado KDC durante o logon de cartão inteligente. Há mais informações no log de eventos do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERRO \_ \_ falha no subsistema de cartão inteligente \_**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



O protocolo Kerberos encontrou um erro ao tentar utilizar o subsistema de cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**\_DOWNGRADE DE \_ ERRO DETECTADO**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



O sistema não pode entrar em contato com um controlador de domínio para fazer o serviço da solicitação de autenticação. Tente novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**MÁQUINA \_ DE ERRO \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



O computador está bloqueado e não pode ser desligado sem a opção force.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**RETORNO \_ DE CHAMADA DE ERRO FORNECIDO DADOS \_ \_ \_ INVÁLIDOS**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Um retorno de chamada definido pelo aplicativo deu dados inválidos quando chamado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ATUALIZAÇÃO \_ DE PRIMEIRO PLANO DE \_ \_ \_ SINCRONIZAÇÃO DE ERRO NECESSÁRIA**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



A estrutura de política de grupo deve chamar a extensão na atualização da política de primeiro plano síncrona.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**DRIVER \_ DE \_ ERRO BLOQUEADO**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Esse driver foi impedido de carregar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERRO \_ \_ IMPORTAÇÃO \_ INVÁLIDA DE NÃO \_ \_ DLL**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Uma DLL (biblioteca de vínculo dinâmico) referenciava um módulo que não era uma DLL nem uma imagem executável do processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ACESSO \_ A \_ ERRO \_ DESABILITADO WEBBLADE**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows não pode abrir esse programa, pois ele foi desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ACESSO \_ A \_ ERRO \_ DESABILITADO ADULTERAÇÃO DO WEBBLADE \_**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows pode abrir esse programa porque o sistema de imposição de licença foi adulterado ou corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**FALHA \_ NA \_ RECUPERAÇÃO DE ERRO**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Falha na recuperação de uma transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERRO \_ JÁ \_ FIBRA**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



O thread atual já foi convertido em uma fibra.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERRO \_ JÁ \_ THREAD**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



O thread atual já foi convertido de uma fibra.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ESTOURO \_ DE BUFFER DE PILHA DE \_ \_ ERROS**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



O sistema detectou um estouro de um buffer baseado em pilha neste aplicativo. Essa superação pode permitir que um usuário mal-intencionado tenha controle sobre esse aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**COTA \_ DE PARÂMETRO DE ERRO \_ \_ EXCEDIDA**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Os dados presentes em um dos parâmetros são mais do que a função pode operar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERRO \_ INATIVO DO \_ DEPURADOR**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Falha ao tentar fazer uma operação em um objeto de depuração porque o objeto está no processo de exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**FALHA NA \_ CARGA DE ATRASO DE \_ \_ ERRO**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Falha ao tentar carregar um .dll ou obter um endereço de função em um .dll carregado com atraso.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERRO \_ VDM \_ NÃO PERMITIDO**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 é um aplicativo de 16 bits. Você não tem permissões para executar aplicativos de 16 bits. Verifique suas permissões com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERRO \_ NÃO \_ IDENTIFICADO**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Existem informações insuficientes para identificar a causa da falha.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERRO \_ PARÂMETRO \_ CRUNTIME \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



O parâmetro passado para uma função de runtime C está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERRO \_ ALÉM \_ DA VDL**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



A operação ocorreu além do comprimento de dados válido do arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERRO \_ TIPO DE SID DE SERVIÇO \_ \_ \_ INCOMPATÍVEL**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



Falha no início do serviço, pois um ou mais serviços no mesmo processo têm uma configuração de tipo de SID de serviço incompatível. Um serviço com tipo de SID de serviço restrito só pode coexistir no mesmo processo com outros serviços com um tipo de SID restrito. Se o tipo de SID de serviço para esse serviço tiver sido configurado, o processo de hospedagem deverá ser reiniciado para iniciar esse serviço.

No Windows Server 2003 e Windows XP, um serviço irrestrito não pode coexistir no mesmo processo com outros serviços. O serviço com o tipo de SID de serviço irrestrito deve ser movido para um processo de propriedade para iniciar esse serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**PROCESSO \_ DE DRIVER DE ERRO \_ \_ ENCERRADO**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



O processo que hospeda o driver para este dispositivo foi encerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**LIMITE DE \_ IMPLEMENTAÇÃO \_ DE ERRO**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Uma operação tentou exceder um limite definido pela implementação.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**O \_ PROCESSO DE ERRO É \_ \_ PROTEGIDO**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



O processo de destino ou o processo que contém o thread de destino é um processo protegido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**NOTIFICAÇÃO \_ DE ATRASO DO CLIENTE DO SERVIÇO DE \_ \_ \_ ERRO**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



O cliente de notificação de serviço está muito atrasado para trás do estado atual dos serviços no computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**COTA \_ DE DISCO DE ERRO \_ \_ EXCEDIDA**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



A operação de arquivo solicitada falhou porque a cota de armazenamento foi excedida. Para liberar espaço em disco, mova os arquivos para um local diferente ou exclua arquivos desnecessários. Para obter mais informações, entre em contato com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**CONTEÚDO \_ DO \_ ERRO BLOQUEADO**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



A operação de arquivo solicitada falhou porque a política de armazenamento bloqueia esse tipo de arquivo. Para obter mais informações, entre em contato com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERRO \_ PRIVILÉGIO DE SERVIÇO \_ \_ INCOMPATÍVEL**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Um privilégio que o serviço requer para funcionar corretamente não existe na configuração da conta de serviço. Você pode usar o snap-in do MMC (Services Console de Gerenciamento Microsoft) (services.msc) e o snap-in do MMC (secpol.msc) de Segurança Configurações Local para exibir a configuração do serviço e a configuração da conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**TRAVA \_ DO APLICATIVO DE \_ ERRO**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Um thread envolvido nesta operação parece não responder.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERRO \_ RÓTULO \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Indica que uma ID de segurança específica não pode ser atribuída como o rótulo de um objeto .


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




