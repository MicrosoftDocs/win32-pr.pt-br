---
description: Descreve os códigos de erro 1000-1299 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Códigos de erro do sistema (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500966"
---
# <a name="system-error-codes-1000-1299"></a>Códigos de erro do sistema (1000-1299)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 1000 a 1299. Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_estouro de pilha de erros \_**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Recursão muito profunda; a pilha estourou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**mensagem de erro \_ inválida \_**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



A janela não pode atuar na mensagem enviada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERRO \_ \_ não pode \_ ser concluído**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Não é possível concluir esta função.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**\_Sinalizadores inválidos de erro \_**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Sinalizadores inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERRO de \_ volume não reconhecido \_**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



O volume não contém um sistema de arquivos reconhecido. Certifique-se de que todos os drivers de sistema de arquivos necessários estejam carregados e que o volume não esteja corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**arquivo de erro \_ \_ inválido**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



O volume de um arquivo foi alterado externamente para que o arquivo aberto não seja mais válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERRO no \_ modo de tela inteira \_**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



A operação solicitada não pode ser executada no modo de tela inteira.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERRO \_ sem \_ token**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Foi feita uma tentativa de fazer referência a um token que não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERRO \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



O banco de dados do registro de configuração está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERRO \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



A chave do registro de configuração é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERRO \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Não foi possível abrir a chave do registro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERRO ao \_ DEStrilha**
</dt> <dd> <dl> <dt>

1012 (0x3F4)
</dt> <dt>



Não foi possível ler a chave do registro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERRO \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



A chave do registro de configuração não pôde ser gravada.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**registro de erro \_ \_ recuperado**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Um dos arquivos no banco de dados do registro precisava ser recuperado pelo uso de um log ou cópia alternativa. A recuperação foi bem-sucedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**registro de erro \_ \_ corrompido**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



O registro está corrompido. A estrutura de um dos arquivos que contêm dados do registro está corrompida ou a imagem de memória do sistema do arquivo está corrompida ou o arquivo não pôde ser recuperado porque a cópia ou o log alternativo estava ausente ou corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**\_ \_ falha na e/s do registro de erro \_**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Uma operação de e/s iniciada pelo registro falhou irrecuperável. O registro não pôde ler, ou gravar ou liberar, um dos arquivos que contêm a imagem do registro do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERRO \_ não \_ arquivo de registro \_**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



O sistema tentou carregar ou restaurar um arquivo no registro, mas o arquivo especificado não está em um formato de arquivo de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**chave de erro \_ \_ excluída**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Tentativa de operação ilegal em uma chave do registro que foi marcada para exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERRO \_ nenhum \_ espaço de log \_**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



O sistema não pôde alocar o espaço necessário em um log do registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**a \_ chave de erro \_ tem \_ filhos**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



Não é possível criar um link simbólico em uma chave do registro que já tenha subchaves ou valores.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**o \_ filho do erro \_ deve \_ ser \_ volátil**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Não é possível criar uma subchave estável em uma chave pai volátil.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERRO ao \_ notificar o \_ diretório de enumeração \_**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Uma solicitação de notificação de alteração está sendo concluída e as informações não estão sendo retornadas no buffer do chamador. O chamador agora precisa enumerar os arquivos para localizar as alterações.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_serviços dependentes de erro \_ \_ em execução**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Um controle de parada foi enviado a um serviço no qual outros serviços em execução dependem.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERRO \_ de \_ controle de serviço inválido \_**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



O controle solicitado não é válido para este serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_ \_ tempo limite de solicitação de serviço de erro \_**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



O serviço não respondeu à solicitação de início ou de controle em um tempo oportuno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**serviço de erro \_ \_ sem \_ thread**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Não foi possível criar um thread para o serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**banco de dados do serviço de erro \_ \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



O banco de dados de serviço está bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**serviço de erro \_ \_ já \_ em execução**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Uma instância do serviço já está em execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERRO \_ de \_ conta de serviço inválida \_**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



O nome da conta é inválido ou não existe, ou a senha é inválida para o nome de conta especificado.


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



Este serviço não pode ser iniciado no modo de segurança.


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

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERRO \_ de \_ aplicativo de instância única \_**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Não é possível iniciar mais de uma instância do programa especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERRO \_ de \_ aplicativo RMODE**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



O programa especificado foi escrito para uma versão anterior do Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**DLL de erro \_ inválido \_**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Um dos arquivos de biblioteca necessários para executar este aplicativo está danificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERRO \_ sem \_ Associação**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Nenhum aplicativo está associado ao arquivo especificado para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERRO de \_ DDE \_ falhou**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Ocorreu um erro ao enviar o comando para o aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**DLL de erro \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Um dos arquivos de biblioteca necessários para executar este aplicativo não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERRO \_ não \_ há \_ mais \_ identificadores de usuário**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



O processo atual usou toda a sua concessão de sistema de identificadores para objetos do Windows Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**sincronização de mensagens de erro \_ \_ \_ somente**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



A mensagem pode ser usada somente com operações síncronas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_elemento fonte de erro \_ \_ vazio**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



O elemento de origem indicado não tem mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**elemento de destino do erro \_ \_ \_ completo**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



O elemento de destino indicado já contém mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERRO \_ de \_ endereço de elemento inválido \_**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



O elemento indicado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**a \_ revista de erro \_ não \_ está presente**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



O elemento indicado faz parte de uma revista que não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**reinicialização do dispositivo de erro \_ \_ \_ necessária**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



O dispositivo indicado requer reinicialização devido a erros de hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**o \_ dispositivo de erro \_ requer \_ limpeza**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



O dispositivo indicou que a limpeza é necessária antes que outras operações sejam tentadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERRO \_ de \_ porta do dispositivo \_ aberta**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



O dispositivo indicou que sua porta está aberta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**dispositivo de erro \_ \_ não \_ conectado**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



O dispositivo não está conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERRO \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Elemento não encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERRO \_ sem \_ correspondência**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Não houve correspondência para a chave especificada no índice.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**conjunto de erros \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



O conjunto de propriedades especificado não existe no objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ponto de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



O ponto passado para GetMouseMovePoints não está no buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERRO \_ nenhum \_ serviço de rastreamento \_**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



O serviço de acompanhamento (estação de trabalho) não está em execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERRO \_ sem \_ ID de volume \_**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



A ID do volume não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERRO \_ não é possível \_ \_ Remover \_ substituído**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Não é possível remover o arquivo a ser substituído.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERRO \_ não é possível \_ \_ mover a \_ substituição**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Não é possível mover o arquivo de substituição para o arquivo a ser substituído. O arquivo a ser substituído manteve seu nome original.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERRO \_ não é possível \_ \_ mover a \_ substituição \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Não é possível mover o arquivo de substituição para o arquivo a ser substituído. O arquivo a ser substituído foi renomeado usando o nome do backup.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ exclusão do diário \_ de erros em \_ andamento**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



O diário de alterações de volume está sendo excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**o \_ diário de erros \_ não está \_ ativo**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



O diário de alterações de volume não está ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_arquivo potencial de erro \_ \_ encontrado**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



Um arquivo foi encontrado, mas ele pode não ser o arquivo correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**entrada de diário de erros \_ \_ \_ excluída**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



A entrada do diário foi excluída do diário.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**o \_ desligamento de erro \_ está \_ agendado**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Um desligamento do sistema já foi agendado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERRO ao \_ desligar \_ os usuários \_ conectados \_**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



Não é possível iniciar o desligamento do sistema porque há outros usuários conectados ao computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERRO \_ de \_ dispositivo insatisfatório**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



O nome do dispositivo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**conexão de erro não \_ \_ disp.**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



O dispositivo não está conectado no momento, mas é uma conexão lembrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**dispositivo de erro \_ \_ já \_ lembrado**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



O nome do dispositivo local tem uma conexão lembrada com outro recurso de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERRO \_ sem \_ \_ caminho de rede ou \_ inadequado \_**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



O caminho de rede foi digitado incorretamente, não existe ou o provedor de rede não está disponível no momento. Tente digitar novamente o caminho ou contate o administrador da rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERRO \_ de \_ provedor insatisfatório**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



O nome do provedor de rede especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERRO \_ não é possível \_ abrir o \_ perfil**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Não é possível abrir o perfil de conexão de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERRO \_ de \_ perfil insatisfatório**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



O perfil de conexão de rede está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERRO \_ não \_ contêiner**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Não é possível enumerar um não-contêiner.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**erro \_ estendido de erro \_**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Ocorreu um erro estendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERRO \_ \_ nome_do_grupo inválido**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



O formato do nome do grupo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERRO \_ de \_ ComputerName inválido**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



O formato do nome do computador especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERRO \_ de \_ EventName inválido**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



O formato do nome do evento especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERRO \_ de \_ nome_do_domínio inválido**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



O formato do nome de domínio especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERRO \_ de \_ ServiceName inválido**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



O formato do nome do serviço especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERRO \_ \_ NetName inválido**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



O formato do nome de rede especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERRO \_ de \_ ShareName inválido**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



O formato do nome de compartilhamento especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERRO \_ \_ passwordname inválido**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



O formato da senha especificada é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**mensagem de erro \_ inválida \_**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



O formato do nome da mensagem especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERRO \_ \_ MESSAGEDEST inválido**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



O formato do destino da mensagem especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_conflito de \_ credenciais de sessão de erro \_**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



Não são permitidas várias conexões com um servidor ou recurso compartilhado pelo mesmo usuário, usando mais de um nome de usuário. Desconecte todas as conexões anteriores ao servidor ou recurso compartilhado e tente novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_limite de sessão remota de erro \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



Foi feita uma tentativa de estabelecer uma sessão para um servidor de rede, mas já existem muitas sessões estabelecidas com esse servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERRO de \_ Dup de \_ domínio**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



O nome de domínio ou grupo de trabalho já está em uso por outro computador na rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERRO \_ sem \_ rede**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



A rede não está presente ou não foi iniciada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERRO \_ cancelado**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



A operação foi cancelada pelo usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERRO \_ de \_ arquivo mapeado pelo usuário \_**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



A operação solicitada não pode ser executada em um arquivo com uma seção mapeada pelo usuário aberta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**conexão de erro \_ \_ recusada**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



O computador remoto recusou a conexão de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**desconexão normal de erro \_ \_**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



A conexão de rede foi fechada normalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**Endereço de erro \_ \_ já \_ associado**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



O ponto de extremidade de transporte de rede já tem um endereço associado a ele.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**Endereço de erro \_ \_ não \_ associado**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Um endereço ainda não foi associado ao ponto de extremidade de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**conexão de erro \_ \_ inválida**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Uma operação foi tentada em uma conexão de rede inexistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**conexão de erro \_ \_ ativa**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Uma operação inválida foi tentada em uma conexão de rede ativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERRO de \_ rede \_ inacessível**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



O local de rede não pode ser acessado. Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**HOST de erro \_ \_ inacessível**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



O local de rede não pode ser acessado. Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**Protocolo de erro \_ \_ inacessível**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



O local de rede não pode ser acessado. Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.


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



Não há suporte para esta operação em um computador que esteja executando o Windows Server 2003 para Small Business Server.


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



O sistema remoto não está disponível. Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.


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

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**DOWNGRADE de erro \_ \_ detectado**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



O sistema não pode contatar um controlador de domínio para atender à solicitação de autenticação. Tente novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**computador de erro \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



O computador está bloqueado e não pode ser desligado sem a opção Force.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**retorno de chamada de erro de \_ \_ \_ dados inválidos fornecidos \_**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Um retorno de chamada definido pelo aplicativo fornecia dados inválidos quando chamado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERRO ao \_ sincronizar a \_ atualização em primeiro plano \_ \_ necessária**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



A estrutura de diretiva de grupo deve chamar a extensão na atualização da política de primeiro plano síncrona.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**Driver de erro \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



O carregamento deste driver foi bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERRO \_ \_ de importação inválida \_ de \_ não \_ dll**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Uma DLL (biblioteca de vínculo dinâmico) referenciou um módulo que não era uma DLL nem a imagem executável do processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERRO ao \_ acessar o \_ \_ webblade desabilitado**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



O Windows não pode abrir este programa porque ele foi desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERRO ao \_ acessar a \_ \_ adulteração da webblade desabilitada \_**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



O Windows não pode abrir este programa porque o sistema de imposição de licença foi violado ou se tornou corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**\_falha na recuperação de erro \_**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Falha na recuperação de uma transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERRO \_ já \_ Fiber**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



O thread atual já foi convertido em uma fibra.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERRO \_ já \_ thread**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



O thread atual já foi convertido de uma fibra.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_estouro de \_ buffer de pilha de erros \_**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



O sistema detectou uma saturação de um buffer baseado em pilha neste aplicativo. Essa saturação pode potencialmente permitir que um usuário mal-intencionado assuma o controle desse aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**cota de parâmetro de erro \_ \_ \_ excedida**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Os dados presentes em um dos parâmetros são mais do que a função pode operar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERRO do \_ depurador \_ inativo**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Falha ao tentar fazer uma operação em um objeto de depuração porque o objeto está sendo excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**\_ \_ falha ao carregar o atraso do erro \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Falha ao tentar atrasar a carga de um. dll ou obter um endereço de função em um DELAYED. dll.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERRO \_ VDM não \_ permitido**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 é um aplicativo de 16 bits. Você não tem permissões para executar aplicativos de 16 bits. Verifique suas permissões com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**erro não \_ identificado \_**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Existem informações insuficientes para identificar a causa da falha.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERRO \_ \_ parâmetro CRUNTIME \_ inválido**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



O parâmetro passado para uma função de tempo de execução C está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERRO \_ além de \_ VDL**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



A operação ocorreu além do comprimento de dados válido do arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERRO de \_ tipo de Sid de serviço INcompatível \_ \_ \_**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



A inicialização do serviço falhou porque um ou mais serviços no mesmo processo têm uma configuração de tipo de SID de serviço incompatível. Um serviço com o tipo de SID de serviço restrito só pode coexistir no mesmo processo com outros serviços com um tipo de SID restrito. Se o tipo de SID de serviço para esse serviço tiver acabado de ser configurado, o processo de hospedagem deverá ser reiniciado para iniciar esse serviço.

No Windows Server 2003 e no Windows XP, um serviço irrestrito não pode coexistir no mesmo processo com outros serviços. O serviço com o tipo de SID de serviço irrestrito deve ser movido para um processo proprietário a fim de iniciar esse serviço.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**processo de driver de erro \_ \_ \_ encerrado**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



O processo que hospeda o driver para este dispositivo foi encerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_limite de implementação de erro \_**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Uma operação tentou exceder um limite definido para implementação.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**o \_ processo de erro \_ está \_ protegido**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



O processo de destino ou o thread de destino que contém o processo é um processo protegido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**notificação do serviço de erro \_ \_ notificando atraso do \_ cliente \_**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



O cliente de notificação de serviço está ultrapassando muito atrás do estado atual dos serviços no computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**cota de disco de erro \_ \_ \_ excedida**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



A operação de arquivo solicitada falhou porque a cota de armazenamento foi excedida. Para liberar espaço em disco, mova arquivos para um local diferente ou exclua arquivos desnecessários. Para obter mais informações, contate o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**conteúdo de erro \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



A operação de arquivo solicitada falhou porque a política de armazenamento bloqueia esse tipo de arquivo. Para obter mais informações, contate o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERRO de \_ privilégio de serviço INcompatível \_ \_**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Um privilégio que o serviço requer para funcionar corretamente não existe na configuração da conta de serviço. Você pode usar o snap-in do MMC (console de gerenciamento Microsoft) de serviços e o snap-in MMC de configurações de segurança local (secpol. msc) para exibir a configuração do serviço e a configuração da conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**\_falha do aplicativo de erro \_**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Um thread envolvido nesta operação parece não estar respondendo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**rótulo de erro \_ inválido \_**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Indica que uma determinada ID de segurança não pode ser atribuída como o rótulo de um objeto.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




