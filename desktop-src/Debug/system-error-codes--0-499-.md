---
description: Descreve os códigos de erro 0-499 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Códigos de erro do sistema (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826432"
---
# <a name="system-error-codes-0-499"></a>Códigos de erro do sistema (0-499)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 0 a 499). Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**êxito do erro \_**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



A operação foi concluída com sucesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**função de erro \_ inválida \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Função incorreta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**arquivo de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



O sistema não pode encontrar o arquivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**caminho de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



O sistema não pode localizar o caminho especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERRO \_ em \_ muitos \_ \_ arquivos abertos**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



O sistema não pode abrir o arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERRO de \_ acesso \_ negado**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



O acesso foi negado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**\_identificador inválido do erro \_**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



O manipulador é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**Arena de erro em \_ \_ Trash**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Os blocos de controle de armazenamento foram destruídos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Não há recursos de memória suficientes disponíveis para processar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERRO \_ de \_ bloco inválido**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



O endereço do bloco de controle de armazenamento é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERRO \_ de \_ ambiente insatisfatório**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



O ambiente está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERRO \_ de \_ formato inadequado**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Foi feita uma tentativa de carregar um programa com um formato incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERRO \_ de \_ acesso inválido**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



O código de acesso é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERRO de \_ dados inválidos \_**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Os dados são inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERRO \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Não há armazenamento suficiente disponível para concluir esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERRO \_ de \_ unidade inválida**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



O sistema não pode localizar a unidade especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERRO \_ no \_ diretório atual**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



O diretório não pode ser removido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERRO \_ não no \_ mesmo \_ dispositivo**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



O sistema não pode mover o arquivo para uma unidade de disco diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRO \_ não há \_ mais \_ arquivos**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Não há mais arquivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERRO \_ de \_ proteção contra gravação**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



A mídia está protegida contra gravação.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERRO \_ de \_ unidade inadequada**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



O sistema não pode localizar o dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERRO \_ não \_ está pronto**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



O dispositivo não está pronto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERRO \_ de \_ comando insatisfatório**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



O dispositivo não reconhece o comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**ERRO de \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Erro de dados (verificação de redundância cíclica).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERRO \_ de \_ comprimento insatisfatório**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



O programa emitiu um comando, mas o comprimento do comando está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERRO de \_ busca**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



A unidade não pode localizar uma área ou trilha específica no disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERRO \_ não \_ \_ disco dos**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



O disco ou disquete especificado não pode ser acessado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**setor de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



A unidade não pode localizar o setor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERRO \_ sem \_ \_ papel**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



A impressora está sem papel.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**\_falha de gravação de erro \_**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



O sistema não pode gravar no dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**\_falha de leitura de erro \_**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



O sistema não pode ler do dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**\_falha de Gen de erro \_**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Um dispositivo conectado ao sistema não está funcionando.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_violação de compartilhamento de erro \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



O processo não pode acessar o arquivo porque ele está sendo usado por outro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_violação de bloqueio de erro \_**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



O processo não pode acessar o arquivo porque outro processo bloqueou uma parte dele.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERRO \_ de \_ disco incorreto**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



O disquete errado está na unidade. Insira %2 (número de série do volume: %3) na unidade %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**o \_ buffer de compartilhamento de erro \_ \_ foi excedido**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Muitos arquivos abertos para compartilhamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**identificador de erro \_ \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Fim do arquivo atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERRO de \_ identificador de \_ disco \_ cheio**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



O disco está cheio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRO \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



A solicitação não terá suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERRO \_ REM \_ não \_ lista**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



O Windows não pode localizar o caminho de rede. Verifique se o caminho de rede está correto e se o computador de destino não está ocupado ou desligado. Se o Windows ainda não conseguir localizar o caminho de rede, entre em contato com o administrador da rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**\_nome do Dup de erro \_**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



Você não estava conectado porque existe um nome duplicado na rede. Se estiver ingressando em um domínio, vá para sistema no painel de controle para alterar o nome do computador e tente novamente. Se estiver ingressando em um grupo de trabalho, escolha outro nome de grupo de trabalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERRO \_ de \_ netpath insatisfatório**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



O caminho da rede não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERRO de \_ rede \_ ocupado**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



A rede está ocupada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**\_desenvolvimento de \_ erro \_ inexistente**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



O dispositivo ou recurso de rede especificado não está mais disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERRO em excesso de \_ \_ \_ cmds**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



O limite de comandos do BIOS de rede foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERRO \_ \_ HDW ADAP \_**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Ocorreu um erro de hardware do adaptador de rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERRO \_ \_ resp net inadequado \_**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



O servidor especificado não pode executar a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERRO \_ UNEXP \_ net \_ Err**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Ocorreu um erro de rede inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERRO \_ de \_ REM \_ .**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



O adaptador remoto não é compatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERRO \_ PRINTQ \_ completo**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



A fila de impressora está cheia.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERRO \_ nenhum \_ espaço de spool \_**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



O espaço para armazenar o arquivo que está aguardando para ser impresso não está disponível no servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERRO ao \_ Imprimir \_ cancelado**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



O arquivo aguardando para ser impresso foi excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERRO \_ NetName \_ excluído**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



O nome da rede especificado não está mais disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERRO \_ de \_ acesso à rede \_ negado**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Acesso à rede negado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERRO \_ \_ tipo de desenvolvimento insatisfatório \_**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



O tipo de recurso de rede não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERRO \_ de \_ nome de rede insatisfatório \_**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



O nome de rede não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERRO \_ em \_ muitos \_ nomes**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



O limite de nome para a placa do adaptador de rede do computador local foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERRO em excesso de \_ \_ \_ sess**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



O limite de sessão do BIOS de rede foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERRO ao \_ compartilhar em \_ pausa**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



O servidor remoto foi pausado ou está em processo de ser iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**Req. de erro \_ \_ não \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



Não é possível fazer mais conexões com este computador remoto no momento porque já existem tantas conexões quantas o computador pode aceitar.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERRO \_ REDIR em \_ pausa**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



A impressora ou o dispositivo de disco especificado foi pausado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**o \_ arquivo de erro \_ existe**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



O arquivo existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERRO \_ não é possível \_ fazer**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Não é possível criar o diretório ou arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERRO \_ falha \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Falha em INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERRO \_ fora \_ de \_ estruturas**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



O armazenamento para processar esta solicitação não está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERRO \_ já \_ atribuído**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



O nome do dispositivo local já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**\_senha inválida do erro \_**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



A senha da rede especificada não está correta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**\_parâmetro inválido de erro \_**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



O parâmetro está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERRO \_ de \_ falha de gravação de rede \_**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Ocorreu uma falha de gravação na rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERRO \_ sem \_ \_ Slots proc**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



O sistema não pode iniciar outro processo no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERRO em excesso de \_ \_ \_ semáforos**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Não é possível criar outro semáforo do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERRO \_ excl \_ sem \_ \_ Propriedade já pertencente**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



O semáforo exclusivo pertence a outro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**o erro \_ sem \_ está \_ definido**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



O semáforo está definido e não pode ser fechado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERRO \_ número \_ excessivo \_ de \_ solicitações sem**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



O semáforo não pode ser definido novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERRO \_ inválido \_ no \_ tempo de interrupção \_**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Não é possível solicitar semáforos exclusivos no tempo de interrupção.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERRO \_ sem \_ proprietário \_ morreu**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



A propriedade anterior deste semáforo foi encerrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERRO \_ sem \_ limite de usuário \_**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Insira o disquete para a unidade %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERRO \_ ao \_ alterar disco**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



O programa foi interrompido porque um disquete alternativo não foi inserido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**unidade de erro \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



O disco está em uso ou está bloqueado por outro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERRO \_ de \_ pipe interrompido**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



O pipe foi encerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**\_ \_ falha ao abrir erro**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



O sistema não pode abrir o dispositivo ou o arquivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_estouro de buffer de erro \_**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



O nome do arquivo é muito longo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERRO de \_ disco \_ cheio**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



Espaço insuficiente no disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERRO \_ não \_ há \_ mais \_ identificadores de pesquisa**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Não há mais identificadores de arquivo internos disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERRO \_ de \_ identificador de destino inválido \_**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



O identificador de arquivo interno de destino está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**Categoria de erro \_ inválida \_**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



A chamada de IOCTL feita pelo programa de aplicativo não está correta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERRO \_ ao \_ verificar \_ opção inválida**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



O valor do parâmetro de opção verify-on-Write não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERRO \_ de \_ nível de driver insatisfatório \_**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



O sistema não oferece suporte ao comando solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**chamada de erro \_ \_ não \_ implementada**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Esta função não tem suporte neste sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERRO \_ sem \_ tempo limite**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



O período de tempo limite de semáforo expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRO \_ de \_ buffer insuficiente**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



A área de dados passada para uma chamada do sistema é muito pequena.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**\_nome inválido do erro \_**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



A sintaxe FileName, nome do diretório ou rótulo do volume está incorreta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERRO \_ de \_ nível inválido**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



O nível de chamada do sistema não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERRO \_ sem \_ rótulo de volume \_**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



O disco não tem nenhum rótulo de volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERRO \_ mod \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



O módulo especificado não pôde ser encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**PROC. de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



Não foi possível encontrar o procedimento especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERRO ao \_ aguardar \_ nenhum \_ filho**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Não há nenhum processo filho a aguardar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERRO \_ filho \_ não \_ concluído**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



O aplicativo %1 não pode ser executado no modo Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_identificador de \_ acesso \_ direto de erro**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Tentativa de usar um identificador de arquivo para uma partição de disco aberta para uma operação diferente de e/s de disco bruto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERRO \_ de \_ busca negativa**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Foi feita uma tentativa de mover o ponteiro do arquivo antes do início do arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERRO ao \_ buscar \_ no \_ dispositivo**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



O ponteiro do arquivo não pode ser definido no dispositivo ou arquivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERRO \_ é \_ destino de junção \_**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Um comando JOIN ou SUBST não pode ser usado para uma unidade que contém unidades Unidas anteriormente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERRO \_ \_ associado**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Foi feita uma tentativa de usar um comando JOIN ou SUBST em uma unidade que já foi unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERRO \_ é \_ subst**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Foi feita uma tentativa de usar um comando JOIN ou SUBST em uma unidade que já foi substituída.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERRO \_ não \_ ingressado**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



O sistema tentou excluir a junção de uma unidade que não está unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERRO \_ não \_ subst**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



O sistema tentou excluir a substituição de uma unidade que não está substituída.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERRO ao \_ ingressar \_ no \_ ingresso**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



O sistema tentou unir uma unidade a um diretório em uma unidade unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERRO \_ subst \_ para \_ subst**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



O sistema tentou substituir uma unidade por um diretório em uma unidade substituída.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERRO ao \_ ingressar \_ no \_ subst**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



O sistema tentou unir uma unidade a um diretório em uma unidade substituída.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERRO \_ subst \_ para \_ unir**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



O sistema tentou SUBST uma unidade para um diretório em uma unidade unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**unidade de erro \_ ocupada \_**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



O sistema não pode executar um JOIN ou SUBST no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERRO na \_ mesma \_ unidade**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



O sistema não pode unir ou substituir uma unidade para ou para um diretório na mesma unidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERRO \_ dir \_ não \_ raiz**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



O diretório não é um subdiretório do diretório raiz.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERRO de \_ dir \_ não \_ vazio**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



O diretório não está vazio.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERRO \_ é \_ um \_ caminho subst**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



O caminho especificado está sendo usado em um substituto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERRO \_ é \_ um \_ caminho de junção**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Não há recursos suficientes disponíveis para processar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**caminho de erro \_ \_ ocupado**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



O caminho especificado não pode ser usado neste momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERRO \_ é \_ \_ destino subst**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Foi feita uma tentativa de unir ou substituir uma unidade para a qual um diretório na unidade é o destino de um substituto anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_rastreamento do sistema de erro \_**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



As informações de rastreamento do sistema não foram especificadas no arquivo de CONFIG.SYS, ou o rastreamento não é permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**contagem de eventos de erro \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



O número de eventos de semáforo especificados para DosMuxSemWait não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERRO em excesso de \_ \_ \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait não foi executado; muitos semáforos já estão definidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERRO \_ de \_ formato de lista inválido \_**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



A lista DosMuxSemWait não está correta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**rótulo de erro \_ \_ muito \_ longo**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



O rótulo do volume inserido excede o limite de caracteres do rótulo do sistema de arquivos de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERRO em excesso de \_ \_ \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



Não é possível criar outro thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**sinal de erro \_ \_ recusado**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



O processo de destinatário recusou o sinal.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERRO \_ Descartado**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



O segmento já foi descartado e não pode ser bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERRO \_ não \_ bloqueado**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



O segmento já está desbloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERRO \_ de \_ THREADID de endereço inadequado \_**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



O endereço da ID do thread não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROS de \_ argumentos inválidos \_**
</dt> <dd> <dl> <dt>

160 (0xA0)
</dt> <dt>



Um ou mais argumentos não estão corretos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERRO \_ nome de caminho insatisfatório \_**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



O caminho especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**sinal de erro \_ \_ pendente**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Já existe um sinal pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERRO \_ Max \_ THRDS \_ atingido**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



Não é possível criar mais threads no sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_falha no bloqueio de erro \_**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Não é possível bloquear uma região de um arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERRO \_ ocupado**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



O recurso solicitado está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**\_ \_ suporte ao dispositivo \_ de erro em \_ andamento**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



A detecção de suporte de comando do dispositivo está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERRO de \_ cancelamento de \_ violação**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Uma solicitação de bloqueio não estava pendente para a região de cancelamento fornecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERRO \_ de \_ bloqueios atômicos \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



O sistema de arquivos não dá suporte a alterações atômicas para o tipo de bloqueio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**\_número de \_ segmento \_ inválido do erro**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



O sistema detectou um número de segmento que não estava correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERRO \_ \_ ORDINAL inválido**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**o erro \_ já \_ existe**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



Não é possível criar um arquivo quando ele já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERRO \_ \_ número de sinalizador inválido \_**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



O sinalizador passado não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERRO \_ sem \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



O nome do semáforo do sistema especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**erro \_ inválido ao \_ Iniciar \_ CODESEG**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERRO \_ \_ STACKSEG inválido**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERRO \_ de \_ ModuleType inválido**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERRO \_ de \_ assinatura exe inválida \_**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



Não é possível executar %1 no modo Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERRO \_ exe \_ marcado como \_ inválido**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERRO \_ de \_ formato exe insatisfatório \_**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 não é um aplicativo Win32 válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**\_Dados iterados de erro \_ \_ excedem \_ 64K**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERRO \_ \_ MINALLOCSIZE inválido**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERRO \_ DYNLINK \_ de \_ \_ anel inválido**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



O sistema operacional não pode executar este programa de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERRO \_ IOPL \_ não \_ habilitado**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



O sistema operacional não está configurado atualmente para executar este aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERRO \_ \_ SEGDPL inválido**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**O erro \_ AUTODATASEG \_ excede \_ 64K**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



O sistema operacional não pode executar este programa de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**O erro \_ RING2SEG \_ deve \_ ser \_ móvel**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



O segmento de código não pode ser maior ou igual a 64K.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERRO \_ realocação \_ Chain \_ XEEDS \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERRO \_ INFLOOP \_ na \_ cadeia de realocação \_**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



O sistema operacional não pode executar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERRO \_ ENVVAR \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



O sistema não pôde encontrar a opção de ambiente que foi inserida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERRO \_ nenhum \_ sinal \_ enviado**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Nenhum processo na subárvore de comandos tem um manipulador de sinais.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERRO \_ de \_ intervalo de EXCED de nome \_**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



O nome do arquivo ou a extensão é muito longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERRO \_ \_ de pilha RING2 \_ em \_ uso**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



A pilha de anéis 2 está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**metaexpansão de erro \_ \_ \_ muito \_ longa**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



Os caracteres de nome de arquivo global, \* ou?, foram inseridos incorretamente ou foram especificados muitos caracteres de nome de arquivo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**\_número de \_ sinal \_ inválido do erro**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



O sinal que está sendo Postado não está correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERRO de \_ thread \_ 1 \_ inativo**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Não é possível definir o manipulador de sinais.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERRO \_ bloqueado**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



O segmento está bloqueado e não pode ser realocado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERRO \_ de \_ muitos \_ módulos**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Muitos módulos de vínculo dinâmico estão anexados a este programa ou módulo de vínculo dinâmico.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_aninhamento de erro \_ não \_ permitido**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



Não é possível aninhar chamadas para LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERRO \_ de \_ tipo de computador exe \_ \_ incompatível**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Esta versão do %1 não é compatível com a versão do Windows que você está executando. Verifique as informações do sistema do seu computador e entre em contato com o fornecedor do software.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERRO \_ exe \_ não \_ pode \_ Modificar \_ binário assinado**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



O arquivo de imagem %1 está assinado; não é possível modificá-lo.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERRO \_ exe \_ não \_ pode \_ Modificar \_ binário assinado forte \_**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



O arquivo de imagem %1 tem uma assinatura forte, não é possível modificar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**arquivo de erro \_ \_ com check- \_ out**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



O check-out deste arquivo foi feito ou bloqueado para edição por outro usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**\_check-out de erro \_ necessário**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



É necessário fazer check-out do arquivo antes de salvar as alterações.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERRO \_ de \_ tipo de arquivo insatisfatório \_**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



O tipo de arquivo que está sendo salvo ou recuperado foi bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**arquivo de erro \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



O tamanho do arquivo excede o limite permitido e não pode ser salvo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**autenticação de formulários de erro \_ \_ \_ necessária**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Acesso negado. Antes de abrir os arquivos neste local, você deve primeiro adicionar o site à sua lista de sites confiáveis, navegar até o site e selecionar a opção para fazer logon automaticamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**vírus de erro \_ \_ infectado**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



A operação não foi concluída com êxito porque o arquivo contém um vírus ou software potencialmente indesejado.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**vírus de erro \_ \_ excluído**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Esse arquivo contém um vírus ou software potencialmente indesejado e não pode ser aberto. Devido à natureza deste vírus ou software potencialmente indesejado, o arquivo foi removido deste local.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**\_local do pipe de erros \_**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



O pipe é local.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERRO \_ de \_ pipe insatisfatório**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



O estado do pipe é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**PIPE de erro \_ \_ ocupado**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Todas as instâncias de pipe estão ocupadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERRO \_ sem \_ dados**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



O pipe está sendo fechado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**PIPE de erro \_ \_ não \_ conectado**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Nenhum processo está na outra extremidade do pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRO de \_ mais \_ dados**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



Mais dados disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERRO \_ vc \_ desconectado**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



A sessão foi cancelada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERRO \_ \_ nome ea \_ inválido**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



O nome do atributo estendido especificado era inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERRO \_ de \_ lista de ea \_ inconsistente**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Os atributos estendidos são inconsistentes.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_tempo limite de espera**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



A operação de espera expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRO \_ não há \_ mais \_ itens**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Não existem mais dados disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERRO \_ não é possível \_ copiar**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



As funções de cópia não podem ser usadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**diretório de erros \_**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



O nome do diretório é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERRO \_ EAS \_ \_ desencaixado**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Os atributos estendidos não couberam no buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERRO \_ de \_ arquivo ea \_ corrompido**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



O arquivo de atributo estendido no sistema de arquivos montado está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERRO \_ de \_ tabela de ea \_ cheia**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



O arquivo da tabela de atributos estendidos está cheio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERRO \_ de \_ identificador ea inválido \_**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



O identificador de atributo estendido especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERRO \_ EAS \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



O sistema de arquivos montado não oferece suporte a atributos estendidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERRO \_ não \_ proprietário**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Tentativa de liberar mutex não pertencente ao chamador.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERRO \_ em \_ muitas \_ postagens**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Foram feitas muitas postagens em um semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERRO \_ de \_ cópia parcial**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Somente parte de uma solicitação de ReadProcessMemory ou WriteProcessMemory foi concluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERRO \_ oplock \_ não \_ concedido**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



A solicitação oplock foi negada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERRO \_ de \_ protocolo oplock inválido \_**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Uma confirmação de oplock inválida foi recebida pelo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**disco de erro \_ \_ muito \_ fragmentado**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



O volume está muito fragmentado para concluir esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERRO ao \_ excluir \_ pendente**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



O arquivo não pode ser aberto porque está em processo de exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERRO \_ incompatível \_ com \_ a \_ \_ configuração de \_ registro de nome curto global \_**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



As configurações de nome curto não podem ser alteradas neste volume devido à configuração do registro global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_nomes curtos \_ \_ de erro não \_ habilitados \_ no \_ volume**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Os nomes curtos não estão habilitados neste volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**o \_ fluxo de segurança do erro \_ \_ está \_ inconsistente**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



O fluxo de segurança para o volume especificado está em um estado inconsistente. Execute CHKDSK no volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERRO \_ de \_ intervalo de bloqueio inválido \_**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Uma operação de bloqueio de arquivo solicitada não pode ser processada devido a um intervalo de bytes inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**o \_ SUBsistema de imagem de erro \_ \_ não \_ está presente**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



O subsistema necessário para dar suporte ao tipo de imagem não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID de notificação de erro \_ \_ \_ já \_ definido**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



O arquivo especificado já tem um GUID de notificação associado a ele.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERRO \_ de \_ manipulador de exceção inválido \_**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Uma rotina de manipulador de exceção inválida foi detectada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERRO de \_ duplicação de \_ privilégios**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Foram especificados privilégios duplicados para o token.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERRO \_ nenhum \_ intervalo \_ processado**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Nenhum intervalo para a operação especificada pôde ser processado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERRO \_ não \_ permitido \_ no \_ arquivo do sistema \_**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



A operação não é permitida em um arquivo interno do sistema de arquivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**recursos de disco de erro \_ \_ \_ esgotados**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Os recursos físicos deste disco foram esgotados.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**\_token inválido do erro \_**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



O token que representa os dados é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**recurso de dispositivo de erro \_ \_ \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



O dispositivo não oferece suporte ao recurso de comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERRO \_ Mr \_ mid \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



O sistema não pode encontrar o texto da mensagem para o número de mensagem 0x %1 no arquivo de mensagem para %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**escopo de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



O escopo especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERRO de \_ escopo INdefinido \_**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



A política de acesso central especificada não está definida no computador de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**\_limite inválido de erro \_**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



A política de acesso central Obtida de Active Directory é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**dispositivo de erro \_ \_ inacessível**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



O dispositivo está inacessível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**dispositivo de erro \_ \_ sem \_ recursos**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



O dispositivo de destino tem recursos insuficientes para concluir a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**\_erro de \_ checksum de dados de erro \_**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Ocorreu um erro de soma de verificação de integridade de dados. Os dados no fluxo de arquivos estão corrompidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERRO de \_ operação de ea de kernel INTERmisturada \_ \_ \_**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Foi feita uma tentativa de modificar um KERNEL e um EA (atributo estendido normal) na mesma operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**corte de nível de arquivo de erro \_ \_ \_ \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



O dispositivo não dá suporte ao corte em nível de arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_violação de \_ alinhamento de deslocamento de erro \_**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



O comando especificou um deslocamento de dados que não se alinha à granularidade/alinhamento do dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERRO \_ \_ de campo \_ inválido \_ na \_ lista de parâmetros**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



O comando especificou um campo inválido em sua lista de parâmetros.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_operação \_ de erro em \_ andamento**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



Uma operação está em andamento no momento com o dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERRO \_ de \_ caminho de dispositivo insatisfatório \_**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Foi feita uma tentativa de enviar o comando por meio de um caminho inválido para o dispositivo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERRO \_ em \_ muitos \_ descritores**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



O comando especificou um número de descritores que excederam o máximo com suporte do dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**dados de limpeza de erro \_ \_ \_ desabilitados**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



A limpeza está desabilitada no arquivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERRO \_ não \_ \_ armazenamento redundante**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



O dispositivo de armazenamento não fornece redundância.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_arquivo residente de erro \_ \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Não há suporte para uma operação em um arquivo residente.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERRO \_ arquivo compactado \_ \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



Não há suporte para uma operação em um arquivo compactado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_ \_ não \_ há suporte para o diretório de erros**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Não há suporte para uma operação em um diretório.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERRO \_ não \_ lido \_ da \_ cópia**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Não foi possível ler a cópia especificada dos dados solicitados.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERRO \_ falha na \_ \_ reinicialização de ação**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



Nenhuma ação foi executada porque uma reinicialização do sistema é necessária.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**\_falha no \_ desligamento do erro**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



Falha na operação de desligamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERRO \_ falha ao \_ reiniciar**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Falha na operação de reinicialização.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERRO \_ máximo de \_ sessões \_ atingido**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



O número máximo de sessões foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**modo de thread de erro \_ \_ \_ já \_ em segundo plano**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



O thread já está no modo de processamento em segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**modo de thread de erro \_ \_ \_ não \_ em segundo plano**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



O thread não está no modo de processamento em segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**modo de processo de erro \_ \_ \_ já \_ em segundo plano**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



O processo já está no modo de processamento em segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**modo de processo de erro \_ \_ \_ não \_ em segundo plano**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



O processo não está no modo de processamento em segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**\_endereço inválido do erro \_**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Tentativa de acessar endereço inválido.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>WinError. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




